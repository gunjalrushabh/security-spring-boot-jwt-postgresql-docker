# Security with Spring Boot, JWT, PostgreSQL and Docker

<b>Author:</b> <a href="https://github.com/jeffrey-spaan" target="_blank">Jeffrey Spaan</a><br>
<b>Created:</b> 2024-01-07<br>
<b>Last updated:</b> 2024-01-07

<div style="text-align: center;">

![security-spring-boot-jwt-postgresql-docker](https://github.com/jeffrey-spaan/security-spring-boot-keycloak-h2-docker/blob/main/images/security-spring-boot-jwt-postgresql-docker.png#center)

</div>

This repository serves as a demonstration on how to create a robust and scalable security application with <b>Spring Security and JWT</b>.<br>
Within this repository, the following technologies are applied:
- [![](https://img.shields.io/badge/Spring%20Boot-8A2BE2)]() [![](https://img.shields.io/badge/release-Dec%2021,%202023-blue)]() [![](https://img.shields.io/badge/version-3.2.1-blue)]()
- [![](https://img.shields.io/badge/JWT-8A2BE2)]() [![](https://img.shields.io/badge/release-Oct%2015,%202023-blue)]() [![](https://img.shields.io/badge/version-0.12.3-blue)]()
- [![](https://img.shields.io/badge/Docker-8A2BE2)]()
<br><br>

![01-spring-boot-icon](https://github.com/jeffrey-spaan/security-spring-boot-jwt-postgresql-docker/blob/main/images/01-spring-boot-icon.png)  ![02-jwt-icon](https://github.com/jeffrey-spaan/security-spring-boot-jwt-postgresql-docker/blob/main/images/02-jwt-icon.png)  ![03-docker-icon](https://github.com/jeffrey-spaan/security-spring-boot-jwt-postgresql-docker/blob/main/images/03-docker-icon.png)

## 1 Installation Prerequisites

- <a href="https://maven.apache.org/download.cgi" target="_blank">Maven</a>
- <a href="https://adoptium.net" target="_blank">Java 21</a> or higher
- <a href="https://www.docker.com/products/docker-desktop/" target="_blank">Docker Desktop</a>
- IDE (of your choice)
<br>

_**Note:** Make sure to disable any local PostgreSQL installation when running this application._

## 2 Project Installation

Open a new command line.

- Clone the repository:

```bash
git clone https://github.com/jeffrey-spaan/security-spring-boot-jwt-postgresql-docker.git
```

- Build the project using Maven:

```bash
mvn clean install
```

- Run the <strong>Spring Boot</strong> application:

```bash
mvn spring-boot:run
```

The application will start on port: ```http://localhost:8081```

## 3 Setup the PostgreSQL Database

1. Access PGAdmin via ```http://localhost:5050```
2. Set a master password for PGAdmin, for example ```root```
3. Within the _Quick Links_ section, click **Add New Server**

- General tab - Name: ```postgres```
- Connection tab - Host name/address: ```postgres```
- Connection tab - Username: ```username```
- Connection tab - Password: ```password```

![04-pgadmin-register-server](https://github.com/jeffrey-spaan/security-spring-boot-jwt-postgresql-docker/blob/main/images/04-pgadmin-register-server.png)

## 4 API Endpoints

To avoid as much manual work as possible, a Postman collection is provided for you to import within your Postman installation.<br>
This file can be found in ```src/main/resources/data/postman/import/collection-import.json```

![05-postman-collection](https://github.com/spring-boot-react-nextjs/security-spring-boot-jwt-postgresql-docker/blob/main/images/05-postman-collection.jpg)


<i>**NOTE:** Use the keys, provided to you in the terminal, to access the secured endpoints:</i>

![06-terminal-tokens](https://github.com/spring-boot-react-nextjs/security-spring-boot-jwt-postgresql-docker/blob/main/images/06-terminal-tokens.jpg)
