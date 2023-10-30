# FastAPI

## FastAPI とは

- Python の標準である型ヒントに基づいて Python 3.6 以降で API を構築するための、  
  モダンで、高速(高パフォーマンス)な、Web フレームワーク

## FastAPI の特徴

- Node.js や Go 言語に匹敵する高速なアプリケーションを開発できる。(Starlette と Pydantic を掛け合わせている)
- Python フレームワークの中では最も高速。
- 少ないコード量で実装できる
- 軽量
- バグが少ない
- 直感的に操作できる
- 構造が簡単で、学習コストが低い(Flask の影響を受けている)
- 拡張性が高く REST と GraphQL 両方の開発に対応している。RDB だけではなく NoSQL の開発にもデフォルトで対応している
- デフォルトで API ドキュメントを出力できる。OpenAPI にも対応
- Python に型定義を含められる
- 非同期通信を簡単に実装できる

## ライブラリのインストール

> pip3 install fastapi

> pip3 install uvicorn

## GETAPI とサーバー立ち上げ

### main.py

```
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
async def index():
  return {"message": "Hello World"}
```

### サーバー立ち上げ

> uvicorn sql_app.main:app --reload

### レスポンス確認

http://127.0.0.1:8000

### Swagger UI

http://127.0.0.1:8000/docs

### Redoc

http://127.0.0.1:8000/redoc

### Python の ORM

#### SQLAlchemy

### streamlit 起動

> streamlit run app.py
