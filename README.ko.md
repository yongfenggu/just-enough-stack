# Just Enough Stack

[English](README.md) | 한국어 | [中文](README.zh.md) | [日本語](README.ja.md) | [Español](README.es.md) | [Tiếng Việt](README.vi.md) | [Português](README.pt.md)

FastAPI, Vue 3, SQLite를 기반으로 한 소규모 앱용 경량 풀스택 스타터입니다.
인증, 역할 기반 권한 제어, 그리고 작업 CRUD 예제를 바로 사용할 수 있는 형태로 제공합니다.

## 기능

- JWT 인증이 포함된 FastAPI 백엔드
- Vue 3 + TypeScript 프런트엔드
- 여러 사용자 역할을 지원하는 역할 기반 접근 제어
- 상태와 우선순위 필드를 갖춘 작업 CRUD 예제
- SQLite 기반 로컬 개발 환경
- 한 번에 실행하는 개발 시작 스크립트

## 기술 스택

- Backend: FastAPI, SQLAlchemy, Pydantic, JWT
- Frontend: Vue 3, TypeScript, Vite, Element Plus, Pinia
- Database: SQLite
- Tooling: uv, npm

## 빠른 시작

```bash
git clone https://github.com/yongfenggu/just-enough-stack.git
cd just-enough-stack
python3 start-dev.py
```

시작 스크립트는 다음을 자동으로 처리합니다:

- 필요한 도구 확인
- 필요 시 백엔드와 프런트엔드 의존성 설치
- `web/.env`가 없으면 `web/.env.example`에서 생성
- 백엔드와 프런트엔드 서비스 시작
- 브라우저에서 프런트엔드 자동 열기

## 요구 사항

- Python 3.12+
- Node.js 18+
- npm
- [uv](https://astral.sh/uv)

## 수동 실행

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

## 기본 주소

- Frontend: `http://localhost:3000`
- Backend API: `http://localhost:8000`
- API Docs: `http://localhost:8000/docs`

## 프로젝트 구조

```text
just-enough-stack/
├── app/           # FastAPI example app
├── je_stack/      # reusable backend package
├── web/           # Vue 3 frontend
├── start-dev.py   # cross-platform startup script
└── README.*.md    # localized READMEs
```

## 문서

- [English README](README.md)
- [中文说明](README.zh.md)
- [Migration Complete Notes](MIGRATION_COMPLETE.md)
- [Backend Migration Notes](app/MIGRATION.md)

## License

MIT
