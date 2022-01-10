# Complete API - A Spring Boot 🍃 Demo
This application represents the backend of a fullstack application capable of performing CRUD methods on User objects.  Additional functionality will be added to consume a 3rd party API and connect to an Angular frontend - *to be built in class in Week 7: Angular*.

<br>

## Data Store 🛂
This app is connected to an **H2 database** which you can access (when running) at `http:localhost:5000/api/h2-console` with the following credentials:

  -  URL: `jdbc:h2:mem:db`
  -  Username: `sa`
  -  Password: `sa`

<br>

## Dockerization 🐳
To run this app, complete with SRE tools such as Prometheus & Grafana, do the following:

- Open a terminal within the root directory of the app: `CompleteAPI/...`
- run `docker compose up` > this will run 3 containers: 

  1. The Spring Boot app will be running at `http://localhost:5000/api`
  2. Prometheus will collect data from Spring Boot Actuator via Micrometer and is running at `http://localhost:9090`
  3. The metrics generated by Prometheus on port 9090 is fed to Grafana running at `http://localhost:3000`
