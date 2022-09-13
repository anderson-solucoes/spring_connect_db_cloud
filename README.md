# Spring Boot project using AWS RDS and Secrets Manager

This is a sample project to demonstrate how to apply Amazon RDS, AWS Secrets Manager and AWS Secrets Manager JDBC Library to a Spring Boot project

## Pre-requisites

A RDS instance up and running. A secret (AWS Secrets Manager) which stores the RDS instance's credentials.

Make sure your AWS environment is correct so your application is able to retrieve the secret from AWS Secrets Manager

## Configuration

Change in [application.yml](src/main/resources/application.yml) rds-endpoint and secret-name (RDSSecretsDemo if use my CloudFormation template)

```yml
spring:
  datasource:
    url: jdbc-secretsmanager:<your-database ex:mysql/posgresql>://<rds-endpoint>:<port>/<database>
    username: <secret-name>
```

## Authors

* **Anderson Alves de Oliveira** - [Anderson]

![Captura de Tela 2022-09-12 às 19 36 42](https://user-images.githubusercontent.com/85138179/189779806-2c55f6aa-5e3c-4e51-8370-97580b3a5762.png)
