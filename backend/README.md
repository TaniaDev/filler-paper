# Backend

This project uses Spring Boot 4.1.0, Java 21 and Maven Wrapper.

## Development server

To start the local development server on Linux or macOS, run:

```bash
./mvnw spring-boot:run
```

On Windows using PowerShell, run:

```powershell
.\mvnw.cmd spring-boot:run
```

Once the application is running, the API will be available at `http://localhost:8080/`.

Unlike the Angular development server, the backend does not automatically restart after source code changes unless an automatic restart tool, such as Spring Boot DevTools, is configured.

## Code scaffolding

Spring Boot does not include a code scaffolding command equivalent to Angular CLI's `ng generate`.

Classes such as controllers, services, repositories and domain objects are created manually under `src/main/java`, following the project's package structure.

## Building

To build the project, run:

```bash
./mvnw clean package
```

This will compile the source code, execute the tests and store the build artifacts in the `target/` directory.

On Windows using PowerShell:

```powershell
.\mvnw.cmd clean package
```

## Running unit tests

To execute the test suite, run:

```bash
./mvnw test
```

On Windows using PowerShell:

```powershell
.\mvnw.cmd test
```

## Running integration tests

To execute the complete Maven verification lifecycle, run:

```bash
./mvnw verify
```

A separate integration-test configuration has not been added yet. When integration tests are introduced, their setup and conventions should be documented in this section.

## Additional Resources

For more information about the technologies used by the backend, see:

- [Spring Boot Reference Documentation](https://docs.spring.io/spring-boot/4.1.0/reference/)
- [Spring Web MVC](https://docs.spring.io/spring-framework/reference/web/webmvc.html)
- [Spring Data JPA](https://docs.spring.io/spring-data/jpa/reference/)
- [Bean Validation](https://docs.spring.io/spring-boot/4.1.0/reference/io/validation.html)
- [Apache Maven Documentation](https://maven.apache.org/guides/)

### Reference Documentation

For further reference, please consider the following sections:

- [Spring Boot Maven Plugin Reference Guide](https://docs.spring.io/spring-boot/4.1.0/maven-plugin)
- [Create an OCI image](https://docs.spring.io/spring-boot/4.1.0/maven-plugin/build-image.html)
- [Spring Web](https://docs.spring.io/spring-boot/4.1.0/reference/web/servlet.html)
- [Validation](https://docs.spring.io/spring-boot/4.1.0/reference/io/validation.html)

### Guides

The following guides illustrate how to use some features concretely:

- [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
- [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
- [Building REST services with Spring](https://spring.io/guides/tutorials/rest/)
- [Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)
- [Validation](https://spring.io/guides/gs/validating-form-input/)

### Maven Parent overrides

Due to Maven's design, elements are inherited from the parent POM to the project POM.
While most of the inheritance is fine, it also inherits unwanted elements like `<license>` and `<developers>` from the parent.
To prevent this, the project POM contains empty overrides for these elements.
If you manually switch to a different parent and actually want the inheritance, you need to remove those overrides.
