# Kotlin Modern Tooling Component

## Purpose
Defines modern Kotlin development patterns using Micronaut framework based on proven enterprise patterns.

## Modern Kotlin Stack

### Framework and Build Tools
- **Framework**: `micronaut` (lightweight, fast-startup microservices)
- **Build Tool**: `gradle.kts` (Kotlin DSL for type-safe builds)
- **Language**: Kotlin with explicit API mode
- **JVM**: Java 17+ toolchain

### Core Libraries
- **Micronaut Security**: JWT authentication and authorization
- **Micronaut Data**: Type-safe database access
- **Kotlin Logging**: Structured logging with MDC support
- **OpenTelemetry**: Observability and tracing
- **Jackson**: JSON serialization with Kotlin support

### Testing Stack
- **Kotest**: Native Kotlin testing framework
- **JUnit 5**: Java compatibility and enterprise integration
- **MockK**: Kotlin-friendly mocking
- **Testcontainers**: Integration testing with real dependencies

## Project Structure Pattern

```
project-name/
├── build.gradle.kts        # Kotlin DSL build configuration
├── gradle.properties
├── src/
│   ├── main/
│   │   ├── kotlin/
│   │   │   └── com/company/
│   │   │       ├── Application.kt
│   │   │       ├── controllers/
│   │   │       ├── services/
│   │   │       ├── models/
│   │   │       └── configuration/
│   │   └── resources/
│   │       ├── application.yml
│   │       └── logback.xml
│   └── test/
│       ├── kotlin/          # Kotest tests
│       └── java/            # JUnit 5 tests
└── docs/
```

## Development Workflow

### Project Setup
```bash
mn create-app project-name --features=security-jwt,data-jpa,openapi
./gradlew build
```

### Configuration Highlights
- **build.gradle.kts**: Version catalogs, explicit API, toolchains
- **Spotless**: ktlint integration for consistent formatting
- **Metalava**: API signature tracking for library development
- **Dokka**: API documentation generation

## Key Patterns from Identity Auth Library

### Build Configuration
- Version catalogs for dependency management
- Explicit API mode for clear public interfaces
- Spotless with ktlint for code formatting
- Multi-module structure for complex projects

### Micronaut Integration
- Security annotations for JWT validation
- AOP interceptors for cross-cutting concerns
- Configuration properties with validation
- Reactive programming with Reactor

### Testing Strategy
- Kotest for behavior-driven tests
- JUnit 5 for compatibility
- MockK for Kotlin-friendly mocking
- Integration tests with real dependencies

## Quality Standards
- **Type Safety**: Explicit API mode and null safety
- **Code Quality**: ktlint via spotless plugin
- **Documentation**: Dokka for API docs
- **Testing**: High coverage with Kotest and JUnit 5
- **Observability**: OpenTelemetry integration built-in

## Integration Points
- References tech_stack_preferences.md for framework selection
- Provides patterns for backend_development.md Kotlin sections
- Supports testing_strategies.md with Kotlin-specific approaches