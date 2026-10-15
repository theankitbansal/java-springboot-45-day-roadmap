# 45-Day Java + Spring Boot Roadmap

| Day | Topic | Practical outcome |
|---:|---|---|
| 1 | Java setup, program structure, variables, data types, operators, conditions, loops, methods, OOP overview | Run and explain small Java programs |
| 2 | Strings, immutability, StringBuilder, equals vs == | Implement and test string utilities |
| 3 | Collections: List, Set, Map, Queue, iteration | Choose collections for realistic use cases |
| 4 | Exceptions, checked vs unchecked, custom exceptions, try-with-resources | Build clear error handling |
| 5 | Java 8 lambdas, functional interfaces, method references | Replace simple anonymous classes |
| 6 | Stream API: filter, map, sorted, collect, reduce, grouping | Transform lists of loan records |
| 7 | Threads, Runnable, synchronization, ExecutorService, race conditions | Explain safe concurrent work |
| 8 | Generics, Comparable/Comparator, equals/hashCode, HashMap internals | Build type-safe data structures |
| 9 | JVM, stack/heap, garbage collection, class loading, memory troubleshooting | Explain runtime behaviour |
| 10 | JDBC, connections, PreparedStatement, ResultSet, resource cleanup | Perform parameterized database operations |
| 11 | SQL basics: SELECT, WHERE, JOIN, GROUP BY, NULL | Query a small loan database |
| 12 | Advanced SQL, indexes, transactions, execution plans | Analyse and improve a query |
| 13 | Maven, project structure, dependencies, Git workflow | Build and version a Java project |
| 14 | JDBC CRUD mini-project | Complete a small persistence workflow |
| 15 | Spring IoC, dependency injection, beans, application context | Explain how Spring wires objects |
| 16 | Spring annotations, constructor injection, component scanning | Build a service layer |
| 17 | Spring Boot starters, auto-configuration, configuration | Start and configure a Boot app |
| 18 | REST, HTTP methods, status codes, resource design | Design a clean API contract |
| 19 | DTOs, validation, mapping, request/response models | Validate API input |
| 20 | Centralized exception handling with ControllerAdvice | Return consistent error responses |
| 21 | In-memory CRUD REST API | Implement endpoints without a database |
| 22 | JPA/Hibernate entities, IDs, lifecycle, mapping basics | Map Java objects to tables |
| 23 | Spring Data JPA repositories and database configuration | Persist data using a repository |
| 24 | Entity relationships and fetch types | Model related entities safely |
| 25 | JPQL/native queries, pagination, sorting, N+1 problem | Query efficiently |
| 26 | Transactional, rollback, propagation, isolation | Explain transaction boundaries |
| 27 | Database performance, indexes, query tuning | Identify likely bottlenecks |
| 28 | Integration tests and rollback testing | Test persistence behaviour |
| 29 | JUnit 5 and Mockito | Write unit tests for service logic |
| 30 | Spring integration tests, MockMvc, test slices | Test API behaviour |
| 31 | Spring Security basics, authentication vs authorization | Protect API routes |
| 32 | JWT and OAuth 2.0 concepts | Explain token-based authentication |
| 33 | Logging, profiles, externalized configuration, secrets | Configure safely across environments |
| 34 | REST best practices, idempotency, OpenAPI/Swagger | Document a reliable API |
| 35 | Actuator, health checks, connection pools, slow SQL | Diagnose operational issues |
| 36 | Microservice boundaries, service ownership, trade-offs | Explain when microservices help |
| 37 | REST communication between services, client timeouts | Make service calls deliberately |
| 38 | API Gateway, service discovery, load balancing | Describe common infrastructure |
| 39 | Kafka fundamentals, topics, partitions, consumer groups | Explain asynchronous event flow |
| 40 | Resilience: timeouts, retries, backoff, circuit breakers | Avoid unsafe retry behaviour |
| 41 | Docker images, containers, Dockerfile | Containerize the capstone |
| 42 | CI/CD concepts, Kubernetes basics, probes and health checks | Explain delivery and deployment |
| 43 | Finish capstone, tests, docs, validation and error handling | Review project quality |
| 44 | Mock interview and coding practice | Explain design decisions and solve problems |
| 45 | Final revision and project walkthrough | Present the project end-to-end |

## Daily completion checklist
- [ ] Read the lesson and official references.
- [ ] Explain core ideas in your own words.
- [ ] Run and modify the example code.
- [ ] Complete the coding exercise.
- [ ] Answer conceptual and interview questions.
- [ ] Review mistakes and complete a retest if needed.
- [ ] Confirm understanding before marking the day complete.

## Capstone milestones
1. Create the project and define the domain model.
2. Implement create/read/list/status-update endpoints.
3. Add validation and centralized error responses.
4. Connect a relational database using JPA.
5. Add service and integration tests.
6. Add security and API documentation.
7. Add logging, health checks, Docker, and final documentation.

The project is introduced early and improved throughout the roadmap.
