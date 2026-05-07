# Just Enough Stack

[English](README.md) | [한국어](README.ko.md) | [中文](README.zh.md) | [日本語](README.ja.md) | [Español](README.es.md) | [Tiếng Việt](README.vi.md) | Português

Um starter full-stack leve para aplicações pequenas, construído com FastAPI, Vue 3 e SQLite.
Ele oferece uma base funcional com autenticação, controle de permissões por papel e um exemplo CRUD de tarefas.

## Recursos

- Backend FastAPI com autenticação JWT
- Frontend em Vue 3 + TypeScript
- Controle de acesso baseado em papéis com vários níveis de usuário
- Exemplo CRUD de tarefas com status e prioridade
- Ambiente de desenvolvimento local baseado em SQLite
- Script de inicialização de desenvolvimento com um único comando

## Stack tecnológica

- Backend: FastAPI, SQLAlchemy, Pydantic, JWT
- Frontend: Vue 3, TypeScript, Vite, Element Plus, Pinia
- Database: SQLite
- Tooling: uv, npm

## Início rápido

```bash
git clone https://github.com/yongfenggu/just-enough-stack.git
cd just-enough-stack
python3 start-dev.py
```

O script de inicialização irá:

- verificar as ferramentas necessárias
- instalar dependências de backend e frontend quando necessário
- criar `web/.env` a partir de `web/.env.example` se estiver ausente
- iniciar os serviços de backend e frontend
- abrir o frontend no navegador

## Requisitos

- Python 3.12+
- Node.js 18+
- npm
- [uv](https://astral.sh/uv)

## Inicialização manual

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

## URLs padrão

- Frontend: `http://localhost:3000`
- Backend API: `http://localhost:8000`
- API Docs: `http://localhost:8000/docs`

## Estrutura do projeto

```text
just-enough-stack/
├── app/           # FastAPI example app
├── je_stack/      # reusable backend package
├── web/           # Vue 3 frontend
├── start-dev.py   # cross-platform startup script
└── README.*.md    # localized READMEs
```

## Documentação

- [English README](README.md)
- [中文说明](README.zh.md)
- [Migration Complete Notes](MIGRATION_COMPLETE.md)
- [Backend Migration Notes](app/MIGRATION.md)

## License

MIT
