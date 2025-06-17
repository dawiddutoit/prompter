# Backend Development Component

## Purpose
Provides specialized backend development patterns, API design strategies, and server-side architecture expertise for Backend Developer agent role.

## Core Capabilities

### Backend Technology Stack

#### Preferred Technologies (from tech_stack_preferences.md)
- **Python**: `uv` + `fastapi` + `pydantic` + `langgraph` (for AI/agent projects)
- **Kotlin**: `micronaut` + `gradle.kts` + `openapi` (lightweight microservices)
- **Node.js**: `fastify` + `typescript` (high-performance APIs)

#### Additional Technology Options
- **Node.js**: Express, NestJS, serverless functions, microservices
- **Python**: Django, Flask, async patterns, data processing
- **Kotlin**: Spring Boot, enterprise patterns, JVM optimization
- **Go**: Gin, Echo, concurrent programming, system programming
- **Rust**: Actix, Axum, performance-critical applications, memory safety

### API Design and Development
- **RESTful APIs**: Resource design, HTTP methods, status codes, versioning
- **GraphQL**: Schema design, resolvers, federation, performance optimization
- **gRPC**: Protocol buffers, streaming, microservice communication
- **WebSockets**: Real-time communication, event-driven architecture
- **API Documentation**: OpenAPI/Swagger, API versioning, client SDK generation

### Database and Data Management
- **Relational Databases**: PostgreSQL, MySQL, schema design, migrations, indexing
- **NoSQL Databases**: MongoDB, Redis, DynamoDB, document design, caching
- **ORMs and Query Builders**: Prisma, TypeORM, Sequelize, Drizzle, query optimization
- **Data Modeling**: Entity relationships, normalization, performance considerations
- **Database Operations**: Migrations, backups, monitoring, scaling strategies

## Standard Backend Workflow

### API Development Process
1. **Requirements Analysis**: API specification, data models, performance requirements
2. **Architecture Design**: Service layer structure, database schema, integration patterns
3. **API Implementation**: Route handlers, middleware, validation, error handling
4. **Database Integration**: Schema creation, ORM setup, migration scripts
5. **Testing**: Unit tests, integration tests, API testing, load testing
6. **Security Implementation**: Authentication, authorization, input validation, security headers
7. **Performance Optimization**: Query optimization, caching, monitoring, scaling preparation

### Backend-Specific Quality Standards
- **Code Quality**: Type safety, error handling, logging, modular architecture
- **Performance**: Query optimization, caching strategies, efficient algorithms
- **Security**: Input validation, authentication, authorization, secure coding practices
- **Scalability**: Stateless design, horizontal scaling, resource management

## Architecture Patterns

### Microservices Patterns
- **Service Decomposition**: Domain-driven design, service boundaries, communication patterns
- **API Gateway**: Request routing, rate limiting, authentication, API composition
- **Service Mesh**: Inter-service communication, observability, traffic management
- **Event-Driven Architecture**: Message queues, event sourcing, saga patterns

### Data Patterns
- **Repository Pattern**: Data access abstraction, testability, database independence
- **CQRS**: Command query responsibility segregation, read/write optimization
- **Event Sourcing**: Event storage, state reconstruction, audit trails
- **Caching Strategies**: Redis, in-memory caching, cache invalidation, CDN integration

### Security Patterns
- **Authentication**: JWT, OAuth2, session management, multi-factor authentication
- **Authorization**: RBAC, ABAC, resource-based permissions, policy engines
- **Input Validation**: Schema validation, sanitization, parameterized queries
- **Security Headers**: CORS, CSP, HSTS, security middleware

## Technology-Specific Patterns

### Modern Python Patterns (Preferred)
- **Package Management**: `uv` for fast dependency management and project setup
- **Data Validation**: `pydantic` models for type-safe APIs and configuration
- **Agent Frameworks**: `langgraph` for building AI agents and workflows
- **API Framework**: `fastapi` + `uvicorn` for high-performance async APIs
- **Code Quality**: `ruff` (linting/formatting) + `mypy` (type checking)

### Node.js/Fastify Patterns (Preferred)
- **Framework**: Fastify for high-performance APIs with TypeScript support
- **Package Management**: `bun` or `npm` with modern tooling
- **Type Safety**: Full TypeScript integration with strict configuration
- **Testing**: `vitest` for fast unit testing

### Kotlin/Micronaut Patterns (Preferred)
- **Framework**: Micronaut for lightweight, fast-startup microservices
- **Build Tool**: Gradle with Kotlin DSL for type-safe builds
- **Language Features**: Explicit API mode, null safety, coroutines
- **API Documentation**: OpenAPI with automatic generation
- **Testing**: Kotest + JUnit 5 + Testcontainers for comprehensive testing

### Legacy Node.js/Express Patterns
- **Middleware**: Custom middleware, error handling, request processing pipelines
- **Async Patterns**: Promises, async/await, stream processing, event loops
- **Performance**: Clustering, worker threads, memory management, profiling
- **Package Management**: npm/yarn, dependency management, security auditing

### Database Integration
- **Connection Management**: Connection pooling, transaction handling, connection limits
- **Query Optimization**: Index usage, query analysis, performance monitoring
- **Migration Strategies**: Schema versioning, rollback procedures, zero-downtime deployments
- **Backup and Recovery**: Automated backups, disaster recovery, data integrity

## Integration Points
- Uses mcp_tools.md for backend project discovery and configuration management
- Works with document_creation.md for API documentation and architecture documentation
- Supports testing_strategies.md with backend-specific testing approaches
- Integrates with development_workflows.md for coding standards and deployment practices
- Uses agent_validation_checkpoints.md for API validation and integration testing
- References tooling/tech_stack_preferences.md for personalized technology defaults
- Incorporates tooling/python_modern_tooling.md for uv + pydantic + langgraph patterns
- Uses tooling/kotlin_modern_tooling.md for micronaut + gradle.kts patterns
- References tooling/language_tooling_patterns.md for language-specific development setups

## Backend Validation Standards
- **API Functionality**: Endpoint testing, response validation, error handling verification
- **Performance Metrics**: Response times, throughput, resource utilization
- **Security Validation**: Authentication testing, authorization verification, vulnerability scanning
- **Data Integrity**: Database constraints, transaction consistency, backup verification
- **Integration Testing**: Service communication, external API integration, end-to-end flows

## Quality Standards
- **Robust Architecture**: Scalable design, fault tolerance, monitoring and observability
- **Security-First**: Secure by design, input validation, authentication and authorization
- **Performance-Optimized**: Efficient queries, caching strategies, resource management
- **Maintainable Code**: Clear abstractions, comprehensive testing, detailed documentation