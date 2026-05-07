# Just Enough Stack

English | [中文](README.zh.md)

A lightweight full-stack starter for small apps, built with FastAPI, Vue 3, and SQLite.
It gives you a working base with authentication, role-based permissions, and a task CRUD example.

## Features

- FastAPI backend with JWT authentication
- Vue 3 + TypeScript frontend
- Role-based access control with multiple user roles
- Task CRUD example with status and priority fields
- SQLite-based local development setup
- One-command dev startup script

## Tech Stack

- Backend: FastAPI, SQLAlchemy, Pydantic, JWT
- Frontend: Vue 3, TypeScript, Vite, Element Plus, Pinia
- Database: SQLite
- Tooling: uv, npm

## Quick Start

```bash
git clone https://github.com/yongfenggu/just-enough-stack.git
cd just-enough-stack
python3 start-dev.py
```

The startup script will:

- check required tools
- install backend and frontend dependencies when needed
- create `web/.env` from `web/.env.example` when missing
- start backend and frontend services
- open the frontend in your browser

## Requirements

- Python 3.12+
- Node.js 18+
- npm
- [uv](https://astral.sh/uv)

## Manual Start

Backend:

```bash
cd app
uv sync
uv run uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

Frontend:

```bash
cd web
npm install
npm run dev
```

## Default URLs

- Frontend: `http://localhost:3000`
- Backend API: `http://localhost:8000`
- API Docs: `http://localhost:8000/docs`

## Project Structure

```text
just-enough-stack/
├── app/           # FastAPI example app
├── je_stack/      # reusable backend package
├── web/           # Vue 3 frontend
├── start-dev.py   # cross-platform startup script
└── README.zh.md   # Chinese README
```

## Docs

- [中文说明](README.zh.md)
- [Migration Complete Notes](MIGRATION_COMPLETE.md)
- [Backend Migration Notes](app/MIGRATION.md)

## License

MIT
