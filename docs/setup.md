# Setup e Dependências - Account Service

Este serviço é responsável pela criação e autenticação de contas. Ele funciona como um microsserviço persistente com banco de dados e versionamento via Flyway.

---

## Requisitos

- Java 17+
- Spring Boot
- PostgreSQL
- Flyway

---

## Dependências (pom.xml)

```xml
<dependency>
    <groupId>org.flywaydb</groupId>
    <artifactId>flyway-core</artifactId>
</dependency>
<dependency>
    <groupId>org.postgresql</groupId>
    <artifactId>postgresql</artifactId>
    <scope>runtime</scope>
</dependency>
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-web</artifactId>
</dependency>
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-validation</artifactId>
</dependency>
```

---

## Como compilar

```bash
mvn clean package
```

---

