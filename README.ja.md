# Just Enough Stack

[English](README.md) | [한국어](README.ko.md) | [中文](README.zh.md) | 日本語 | [Español](README.es.md) | [Tiếng Việt](README.vi.md) | [Português](README.pt.md)

FastAPI、Vue 3、SQLite をベースにした、小規模アプリ向けの軽量フルスタック・スターターです。
認証、ロールベースの権限制御、そしてタスク CRUD のサンプルをすぐに使える形で提供します。

## 特徴

- JWT 認証付きの FastAPI バックエンド
- Vue 3 + TypeScript フロントエンド
- 複数ロールに対応したロールベースアクセス制御
- ステータスと優先度を備えたタスク CRUD サンプル
- SQLite ベースのローカル開発環境
- ワンコマンドの開発起動スクリプト

## 技術スタック

- Backend: FastAPI, SQLAlchemy, Pydantic, JWT
- Frontend: Vue 3, TypeScript, Vite, Element Plus, Pinia
- Database: SQLite
- Tooling: uv, npm

## クイックスタート

```bash
git clone https://github.com/yongfenggu/just-enough-stack.git
cd just-enough-stack
python3 start-dev.py
```

起動スクリプトは次の処理を自動で行います:

- 必要なツールの確認
- 必要に応じたバックエンドとフロントエンド依存関係のインストール
- `web/.env` が無い場合に `web/.env.example` から生成
- バックエンドとフロントエンドの起動
- ブラウザでフロントエンドを自動的に開く

## 要件

- Python 3.12+
- Node.js 18+
- npm
- [uv](https://astral.sh/uv)

## 手動起動

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

## デフォルト URL

- Frontend: `http://localhost:3000`
- Backend API: `http://localhost:8000`
- API Docs: `http://localhost:8000/docs`

## プロジェクト構成

```text
just-enough-stack/
├── app/           # FastAPI example app
├── je_stack/      # reusable backend package
├── web/           # Vue 3 frontend
├── start-dev.py   # cross-platform startup script
└── README.*.md    # localized READMEs
```

## ドキュメント

- [English README](README.md)
- [中文说明](README.zh.md)
- [Migration Complete Notes](MIGRATION_COMPLETE.md)
- [Backend Migration Notes](app/MIGRATION.md)

## License

MIT
