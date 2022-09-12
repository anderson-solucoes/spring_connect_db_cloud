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

* **Anderson Alves de Oliveira** - [Anderson](https://github.com/anderson-solucoes/spring_connect_db_cloud)