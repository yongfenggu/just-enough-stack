<p align="center">
  <img src="docs/banner.svg" alt="Just Enough Stack" />
</p>

<p align="center">
  English | <a href="README.zh.md">中文</a> | <a href="README.ko.md">한국어</a> | <a href="README.ja.md">日本語</a> | <a href="README.es.md">Español</a>
</p>

<p align="center">
  <a href="https://github.com/yongfenggu/just-enough-stack/stargazers"><img src="https://img.shields.io/github/stars/yongfenggu/just-enough-stack" alt="GitHub Stars" /></a>
  <a href="LICENSE"><img src="https://img.shields.io/github/license/yongfenggu/just-enough-stack" alt="License: MIT" /></a>
</p>

A **lightweight full-stack scaffold** for building small apps quickly, based on **FastAPI + Vue3 + SQLite** with built-in authentication, RBAC, and CRUD examples.

## Quick Start

```bash
git clone https://github.com/yongfenggu/just-enough-stack.git
cd just-enough-stack
python start-dev.py
```

The script will automatically:
- Check dependencies (Python, Node.js, npm, uv)
- Install backend and frontend packages
- Start both servers
- Open http://localhost:3000 in your browser

### Requirements
- Python 3.12+
- Node.js 18+
- npm or yarn
- [uv](https://astral.sh/uv) - Python package manager

**Install uv:**
```bash
# macOS / Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# Windows
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"
```

## Tech Stack

### Backend
- **FastAPI** - Modern Python web framework
- **SQLAlchemy** - ORM
- **Pydantic** - Validation & API schema (SSOT)
- **JWT** - Authentication

### Frontend
- **Vue3 + TypeScript** - Type-safe UI framework
- **Vite** - Build tool
- **Element Plus** - UI components
- **Pinia** - State management

## Features

### Authentication & Authorization
- Register / Login (JWT)
- RBAC (Guest / User / Admin / Super Admin)
- User management

### CRUD Example (Task Manager)
- Create, read, update, delete
- Status tracking (Pending / In Progress / Done / Cancelled)
- Priority levels (Low / Medium / High)
- Pagination & filtering

### Developer Friendly
- RESTful API design
- Auto-generated API docs (Swagger)

### Manual Start (Optional)

**Backend:**
```bash
cd app
uv sync
uv run uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

**Frontend:**
```bash
cd web
npm install
npm run dev
```

### URLs
- Frontend: http://localhost:3000
- Backend API: http://localhost:8000
- API Docs: http://localhost:8000/docs

## API Response Format
```json
{
  "success": true,
  "message": "OK",
  "data": {}
}
```

## Development Guide

### Adding a New Feature
1. Backend: Define ORM → DAO → Pydantic Schema → API endpoint
2. Frontend: Write TypeScript types → API client → Store → Page

### Permission Control
```python
from src.middleware.auth import check_user_permission

@router.post("/tasks")
async def create_task(
    current_user = Depends(check_user_permission())
):
    pass  # logged-in users only
```

## Database
Tables are created automatically on first run. To reset:
```bash
rm backend/app.db
```

## License

MIT

## Contributing
[Issues](../../issues) and [PRs](../../pulls) are welcome!
