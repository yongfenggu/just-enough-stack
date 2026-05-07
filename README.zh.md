# Just Enough Stack

[English](README.md) | 中文

一个面向小型应用的轻量全栈脚手架，基于 FastAPI、Vue 3 和 SQLite。
它提供了开箱即用的认证、权限控制，以及一个任务 CRUD 示例，方便你快速起步。

## 功能

- FastAPI 后端与 JWT 登录认证
- Vue 3 + TypeScript 前端
- 基于角色的权限控制
- 带状态和优先级字段的任务 CRUD 示例
- 基于 SQLite 的本地开发环境
- 一键启动开发脚本

## 技术栈

- 后端：FastAPI、SQLAlchemy、Pydantic、JWT
- 前端：Vue 3、TypeScript、Vite、Element Plus、Pinia
- 数据库：SQLite
- 工具链：uv、npm

## 快速开始

```bash
git clone https://github.com/yongfenggu/just-enough-stack.git
cd just-enough-stack
python3 start-dev.py
```

启动脚本会自动：

- 检查所需工具是否已安装
- 按需安装前后端依赖
- 在缺少 `web/.env` 时由 `web/.env.example` 自动生成
- 启动前后端服务
- 自动打开浏览器访问前端页面

## 环境要求

- Python 3.12+
- Node.js 18+
- npm
- [uv](https://astral.sh/uv)

## 手动启动

后端：

```bash
cd app
uv sync
uv run uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

前端：

```bash
cd web
npm install
npm run dev
```

## 默认地址

- 前端：`http://localhost:3000`
- 后端 API：`http://localhost:8000`
- API 文档：`http://localhost:8000/docs`

## 项目结构

```text
just-enough-stack/
├── app/           # FastAPI 示例应用
├── je_stack/      # 可复用后端包
├── web/           # Vue 3 前端
├── start-dev.py   # 跨平台启动脚本
└── README.zh.md   # 中文说明
```

## 文档

- [English README](README.md)
- [迁移完成说明](MIGRATION_COMPLETE.md)
- [后端迁移说明](app/MIGRATION.md)

## License

MIT
