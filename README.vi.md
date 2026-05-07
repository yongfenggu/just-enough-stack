# Just Enough Stack

[English](README.md) | [한국어](README.ko.md) | [中文](README.zh.md) | [日本語](README.ja.md) | [Español](README.es.md) | Tiếng Việt | [Português](README.pt.md)

Một bộ khởi đầu full-stack gọn nhẹ cho các ứng dụng nhỏ, được xây dựng với FastAPI, Vue 3 và SQLite.
Nó cung cấp sẵn xác thực, phân quyền theo vai trò và một ví dụ CRUD cho tác vụ để bạn bắt đầu nhanh hơn.

## Tính năng

- Backend FastAPI với xác thực JWT
- Frontend Vue 3 + TypeScript
- Kiểm soát truy cập theo vai trò với nhiều cấp người dùng
- Ví dụ CRUD cho tác vụ với trạng thái và độ ưu tiên
- Môi trường phát triển cục bộ dựa trên SQLite
- Script khởi động phát triển bằng một lệnh

## Công nghệ sử dụng

- Backend: FastAPI, SQLAlchemy, Pydantic, JWT
- Frontend: Vue 3, TypeScript, Vite, Element Plus, Pinia
- Database: SQLite
- Tooling: uv, npm

## Bắt đầu nhanh

```bash
git clone https://github.com/yongfenggu/just-enough-stack.git
cd just-enough-stack
python3 start-dev.py
```

Script khởi động sẽ tự động:

- kiểm tra các công cụ cần thiết
- cài đặt phụ thuộc cho backend và frontend khi cần
- tạo `web/.env` từ `web/.env.example` nếu còn thiếu
- khởi động dịch vụ backend và frontend
- mở frontend trong trình duyệt của bạn

## Yêu cầu

- Python 3.12+
- Node.js 18+
- npm
- [uv](https://astral.sh/uv)

## Khởi động thủ công

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

## URL mặc định

- Frontend: `http://localhost:3000`
- Backend API: `http://localhost:8000`
- API Docs: `http://localhost:8000/docs`

## Cấu trúc dự án

```text
just-enough-stack/
├── app/           # FastAPI example app
├── je_stack/      # reusable backend package
├── web/           # Vue 3 frontend
├── start-dev.py   # cross-platform startup script
└── README.*.md    # localized READMEs
```

## Tài liệu

- [English README](README.md)
- [中文说明](README.zh.md)
- [Migration Complete Notes](MIGRATION_COMPLETE.md)
- [Backend Migration Notes](app/MIGRATION.md)

## License

MIT
