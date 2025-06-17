# Tech Stack Preferences Component

## Purpose
Defines personalized technology choices that serve as intelligent defaults for project creation and development workflows.

## Core Technology Preferences

### Python Ecosystem
- **Package Management**: `uv` (modern, fast Python package installer)
- **Data Validation**: `pydantic` (type-safe data models and validation)
- **AI/ML Frameworks**: `langgraph` (agent orchestration and workflows)
- **API Development**: `fastapi` (high-performance async API framework)
- **Code Quality**: `ruff` (fast linting and formatting)

### Kotlin Ecosystem  
- **Framework**: `micronaut` (lightweight, fast-startup microservices)
- **Build Tool**: `gradle.kts` (Kotlin DSL)
- **Testing**: `kotest` + `junit5` (comprehensive testing stack)
- **Code Quality**: `ktlint` via `spotless` (consistent formatting)

### Node.js Ecosystem
- **Runtime**: `bun` or `node.js` (prefer bun for performance)
- **Framework**: `fastify` (high-performance web framework)
- **Type Safety**: `typescript` with strict configuration
- **Build Tool**: `vite` (fast development and building)

### Frontend Preferences
- **Build Tool**: `vite` (fast development and building)
- **Framework**: `react` with hooks patterns
- **State Management**: `zustand` (lightweight state)
- **Styling**: `tailwindcss` (utility-first CSS)
- **API Client**: `@tanstack/react-query` (server state)

## Technology Selection Patterns

### By Project Type
- **API-First**: Python (`uv` + `fastapi` + `pydantic`)
- **Agent/AI**: Python (`fastapi` + `langgraph` + `pydantic`)
- **Microservices**: Kotlin (`micronaut` + `gradle.kts`)
- **Full-Stack Web**: React (`vite` + `tailwindcss`) + Python backend

## Template Variables
- `{{PYTHON_PACKAGE_MANAGER}}` → "uv"
- `{{PYTHON_API_FRAMEWORK}}` → "fastapi"
- `{{PYTHON_VALIDATION_LIBRARY}}` → "pydantic"
- `{{PYTHON_AGENT_FRAMEWORK}}` → "langgraph"
- `{{KOTLIN_FRAMEWORK}}` → "micronaut"
- `{{FRONTEND_BUILD_TOOL}}` → "vite"
- `{{FRONTEND_FRAMEWORK}}` → "react"
- `{{STYLING_FRAMEWORK}}` → "tailwindcss"

## Integration Points
- Provides intelligent defaults for create_new_project
- Informs development agent technology choices
- Guides architecture decisions
- Ensures consistency across projects

## Quality Standards
- Modern tooling with strong type safety
- Performance-focused library choices
- Excellent documentation and OpenAPI support
- Comprehensive testing capabilities