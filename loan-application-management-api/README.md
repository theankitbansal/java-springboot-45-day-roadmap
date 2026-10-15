# Loan Application Management API

A learning capstone that grows throughout the 45-day roadmap. The initial scaffold is deliberately small; later milestones add persistence, validation, tests, security, monitoring, and containerization.

## Initial technology choices
- Java 8
- Spring Boot 2.7.18 (legacy, end-of-life; selected only to preserve Java 8 compatibility)
- Spring Web
- Spring Data JPA
- Bean Validation
- H2 for local development and tests
- Maven

For a new production application, choose a currently supported Spring Boot release and supported Java version instead of copying this legacy version choice.

## Planned API
| Method | Endpoint | Purpose |
|---|---|---|
| POST | /api/loan-applications | Create an application |
| GET | /api/loan-applications/{id} | Retrieve an application |
| GET | /api/loan-applications | List applications |
| PATCH | /api/loan-applications/{id}/status | Update status with transition validation |

## Initial domain fields
- id: generated identifier
- applicantReference: synthetic, non-sensitive reference only
- loanType: e.g. PERSONAL, HOME, AUTO
- requestedAmount: BigDecimal
- tenureMonths: positive integer within configured bounds
- status: e.g. SUBMITTED, UNDER_REVIEW, APPROVED, REJECTED
- createdAt and updatedAt: timestamps

## Suggested package structure
~~~text
src/main/java/com/example/loan/
  LoanApplicationApiApplication.java
  controller/
  dto/
  entity/
  exception/
  repository/
  service/
src/main/resources/
  application.properties
src/test/java/com/example/loan/
docs/
  DOMAIN-MODEL.md
~~~

## Development milestones
1. Start the application and verify the basic runtime.
2. Implement DTOs and request validation.
3. Implement create/read/list/status-update endpoints.
4. Add JPA persistence and test database configuration.
5. Add centralized error responses and domain transition rules.
6. Add unit and integration tests.
7. Add authentication/authorization, API documentation, logs, and health checks.
8. Add Docker instructions and a project walkthrough.

## Run locally
From this directory, once the scaffold is complete:

~~~bash
mvn spring-boot:run
~~~

Use synthetic records only. Never commit actual customer information, production database details, credentials, access tokens, or confidential banking logic.
