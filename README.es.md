# Just Enough Stack

[English](README.md) | [한국어](README.ko.md) | [中文](README.zh.md) | [日本語](README.ja.md) | Español | [Tiếng Việt](README.vi.md) | [Português](README.pt.md)

Un starter full-stack ligero para aplicaciones pequeñas, construido con FastAPI, Vue 3 y SQLite.
Incluye una base funcional con autenticación, control de permisos por roles y un ejemplo CRUD de tareas.

## Características

- Backend FastAPI con autenticación JWT
- Frontend con Vue 3 + TypeScript
- Control de acceso basado en roles con varios niveles de usuario
- Ejemplo CRUD de tareas con estado y prioridad
- Entorno de desarrollo local basado en SQLite
- Script de arranque para desarrollo con un solo comando

## Stack tecnológico

- Backend: FastAPI, SQLAlchemy, Pydantic, JWT
- Frontend: Vue 3, TypeScript, Vite, Element Plus, Pinia
- Database: SQLite
- Tooling: uv, npm

## Inicio rápido

```bash
git clone https://github.com/yongfenggu/just-enough-stack.git
cd just-enough-stack
python3 start-dev.py
```

El script de inicio hará lo siguiente automáticamente:

- comprobar las herramientas necesarias
- instalar dependencias de backend y frontend cuando haga falta
- crear `web/.env` a partir de `web/.env.example` si no existe
- iniciar los servicios de backend y frontend
- abrir el frontend en tu navegador

## Requisitos

- Python 3.12+
- Node.js 18+
- npm
- [uv](https://astral.sh/uv)

## Inicio manual

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

## URLs por defecto

- Frontend: `http://localhost:3000`
- Backend API: `http://localhost:8000`
- API Docs: `http://localhost:8000/docs`

## Estructura del proyecto

```text
just-enough-stack/
├── app/           # FastAPI example app
├── je_stack/      # reusable backend package
├── web/           # Vue 3 frontend
├── start-dev.py   # cross-platform startup script
└── README.*.md    # localized READMEs
```

## Documentación

- [English README](README.md)
- [中文说明](README.zh.md)
- [Migration Complete Notes](MIGRATION_COMPLETE.md)
- [Backend Migration Notes](app/MIGRATION.md)

## License

MIT
