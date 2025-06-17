# Python Modern Tooling Component

## Purpose
Defines modern Python development patterns using uv, pydantic, and langgraph for next-generation Python projects.

## Modern Python Stack

### Package Management with uv
- **Installation**: Fast, reliable package management
- **Commands**: `uv init`, `uv add`, `uv sync`
- **Benefits**: Faster than pip/poetry, automatic virtual environments

### Core Libraries
- **Pydantic**: Type-safe data models with automatic validation
- **FastAPI**: High-performance async API framework with auto-documentation
- **LangGraph**: Agent workflow orchestration and state management
- **Ruff**: Fast linting and code formatting
- **Mypy**: Static type checking

## Project Structure Pattern

```
project-name/
├── pyproject.toml          # uv configuration
├── uv.lock                 # Lock file
├── src/
│   └── project_name/
│       ├── main.py         # FastAPI app
│       ├── models/         # Pydantic models
│       ├── agents/         # LangGraph agents
│       └── services/       # Business logic
├── tests/
└── docs/
```

## Development Workflow

### Project Setup
```bash
uv init project-name
uv add fastapi pydantic langgraph uvicorn
uv add --dev pytest ruff mypy
```

### Configuration Highlights
- **pyproject.toml**: uv dependencies, ruff rules, mypy settings
- **Type Safety**: Full mypy compliance with pydantic models
- **Testing**: pytest with async support
- **Code Quality**: ruff for linting and formatting

## Integration Patterns
- **API + Validation**: FastAPI endpoints with pydantic request/response models
- **Agent Workflows**: LangGraph StateGraph for multi-step agent processes
- **Type Safety**: Full typing with mypy validation
- **Container Ready**: Dockerfile optimized for uv

## Integration Points
- References tech_stack_preferences.md for library defaults
- Supports backend_development.md Python sections
- Provides patterns for testing_strategies.md

## Quality Standards
- Type safety with mypy strict mode
- Comprehensive ruff linting rules
- Pydantic validation for all data structures
- Async/await patterns throughout