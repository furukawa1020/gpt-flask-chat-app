# GPT Chat App

## 概要
このリポジトリは、OpenAIのGPTモデルを利用したチャットアプリケーションのサンプルです。Flaskをバックエンドに採用し、Back4Appなどのクラウドサービスとの連携も想定しています。ユーザーはWebブラウザから自然言語で質問や会話ができ、AIが応答します。

## ディレクトリ構成

- `gpt-chat-app/`：メインのチャットアプリケーション
  - `app.py`：FlaskによるWebサーバーのメインスクリプト。ユーザーの入力を受け取り、GPT APIにリクエストを送信し、応答を返します。
  - `Procfile`：Heroku等のPaaSでアプリをデプロイするための起動設定ファイル。
  - `requirements.txt`：必要なPythonパッケージ一覧（Flask, openai など）。
  - `static/style.css`：アプリの見た目を整えるCSSファイル。
  - `templates/index.html`：チャット画面のHTMLテンプレート。ユーザー入力欄とAI応答欄を含みます。

- `gpt-chat-app copy/`：`gpt-chat-app`のバックアップまたは別バージョン。構成は同じです。

- `flask-back4app/`：Back4App連携用のサンプルや設定ファイル（詳細は未確認）。

## 各ファイルの詳細

### gpt-chat-app/app.py
FlaskでWebサーバーを立ち上げ、`/`ルートでチャット画面を表示。POSTリクエストでユーザーのメッセージを受け取り、OpenAI APIに送信し、応答を返す。

### gpt-chat-app/Procfile
Webサーバーの起動コマンド（例：`web: python app.py`）。Heroku等でのデプロイ時に使用。

### gpt-chat-app/requirements.txt
Flaskやopenaiなど、アプリに必要なPythonパッケージを列挙。

### gpt-chat-app/static/style.css
チャット画面のレイアウトや色など、UIの見た目を定義。

### gpt-chat-app/templates/index.html
チャット画面のHTML。ユーザー入力欄、送信ボタン、AI応答表示エリアを含む。

### gpt-chat-app copy/
`gpt-chat-app`と同じ構成。バックアップや別バージョンとして利用可能。

## 3行コミット文まとめ
- FlaskでGPTチャットWebアプリを実装
- Heroku用Procfileと依存パッケージを追加
- UI用HTML/CSSとAPI連携を構築

## 推奨リポジトリ名
**gpt-flask-chat-app**

---

ご質問や機能追加のご要望があれば、`app.py`を編集して拡張できます。
