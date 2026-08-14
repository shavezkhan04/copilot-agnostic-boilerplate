# Project Workspace

Professional, technology-agnostic project structure for modern software delivery.

## Naming Conventions

- Directories and files use kebab-case.
- System components, modules, and service classes use PascalCase.
- Environment variables use uppercase snake_case.
- Keep identifiers descriptive and consistent across the project.

## Repository Layout

```text
project-root/
├── .env
├── .env.example
├── .gitignore
├── README.md
├── docs/
│   └── .gitkeep
├── src/
│   ├── config/
│   │   └── .gitkeep
│   ├── core/
│   │   └── .gitkeep
│   ├── entrypoints/
│   │   └── .gitkeep
│   └── infrastructure/
│       └── .gitkeep
└── tests/
    ├── integration/
    │   └── .gitkeep
    └── unit/
        └── .gitkeep
```

## Prerequisites

Before starting work, ensure the following are available:

- Git
- A local runtime or interpreter compatible with your project
- An environment manager or secret vault for local configuration
- A database or service dependency defined in `.env` if required

## Local Setup

1. Clone the repository.
2. Copy `.env.example` to `.env` for local secrets.
3. Update placeholders with valid local values.
4. Install dependencies for the selected stack.
5. Start the application or service with your chosen runtime command.

## Local Boot Templates

### Example: Application bootstrap

```bash
cp .env.example .env
# update values in .env before starting
npm install
npm run dev
```

### Example: Python service bootstrap

```bash
cp .env.example .env
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

### Example: Containerized local boot

```bash
cp .env.example .env
docker compose up --build
```

## Environment Configuration

Use `.env` only for local development values. Keep production secrets in a managed secret store or deployment environment. The example file documents the expected keys:

- `APP_ENV`
- `APP_DEBUG`
- `API_KEY`
- `DATABASE_URL`
- `REDIS_URL`
- `LOG_LEVEL`

## Notes

This workspace intentionally avoids framework-specific assumptions so it can be adapted for backend services, CLI tools, APIs, or full-stack platforms without changing the structure itself.
