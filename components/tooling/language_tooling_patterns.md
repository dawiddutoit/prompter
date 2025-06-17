# Language Tooling Patterns Component

## Purpose
Provides language-specific tooling patterns and development setups for consistent project initialization across technology stacks.

## Tooling Matrix by Language

### Python Projects
- **Package Manager**: `uv` → Fast package management
- **Framework**: `fastapi` + `pydantic` → Type-safe APIs
- **Agent Framework**: `langgraph` → AI workflows
- **Code Quality**: `ruff` + `mypy` → Linting and type checking
- **Testing**: `pytest` → Comprehensive testing

### Kotlin Projects
- **Framework**: `micronaut` → Lightweight microservices
- **Build Tool**: `gradle.kts` → Type-safe builds
- **Code Quality**: `ktlint` via `spotless` → Consistent formatting
- **Testing**: `kotest` + `junit5` → Comprehensive testing stack

### Node.js Projects
- **Runtime**: `bun` → Fast JavaScript runtime
- **Framework**: `fastify` → High-performance APIs
- **Build Tool**: `vite` → Fast development
- **Code Quality**: `biome` → Fast linting and formatting
- **Testing**: `vitest` + `playwright` → Unit and E2E testing

### Frontend Projects
- **Build Tool**: `vite` → Fast development server
- **Framework**: `react` → Component-based UI
- **State**: `zustand` + `@tanstack/react-query` → Client and server state
- **Styling**: `tailwindcss` → Utility-first CSS
- **Testing**: `vitest` + `@testing-library/react` → Component testing

## Project Initialization Patterns

### Python/FastAPI
```bash
uv init {project_name}
uv add fastapi pydantic uvicorn
uv add --dev pytest ruff mypy
```

### Kotlin/Micronaut
```bash
mn create-app {project_name} --features=security-jwt,openapi
./gradlew build
```

### Node.js/Fastify
```bash
bun create fastify {project_name} --typescript
bun add fastify
bun add -d vitest playwright
```

### React/Vite
```bash
npm create vite@latest {project_name} -- --template react-ts
npm install tailwindcss zustand @tanstack/react-query
npm install -D vitest @testing-library/react
```

## Configuration Standards

### Development Environment
- **Python**: pyproject.toml with uv, ruff, and mypy configuration
- **Kotlin**: build.gradle.kts with spotless, ktlint, and version catalogs
- **Node.js**: package.json with TypeScript, biome, and testing tools
- **Frontend**: vite.config.ts with TypeScript and testing setup

### Container Patterns
- **Python**: Multi-stage builds with uv for fast dependency installation
- **Kotlin**: JVM base images with Gradle build optimization
- **Node.js**: Alpine images with bun for smaller footprint
- **Frontend**: Static hosting with nginx for production builds

## Quality Standards
- **Type Safety**: Full typing across all languages
- **Code Quality**: Consistent formatting and linting
- **Testing**: Comprehensive unit and integration testing
- **Documentation**: Auto-generated API docs where applicable
- **Performance**: Optimized tooling for fast development cycles

## Integration Points
- References tech_stack_preferences.md for default choices
- Provides structure templates for create_new_project
- Supports development agent tooling knowledge
- Guides architecture decisions for technology selection