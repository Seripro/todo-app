# Todo アプリ

## 概要

このリポジトリは、シンプルな Todo 管理アプリの実装例です。フロントエンドは **React + Vite**（TypeScript）で構築し、バックエンドは **Hono** と **Firebase Firestore エミュレータ** を組み合わせた REST API でデータ永続化を行います。ユーザーはタスクの作成、完了・未完了の切り替え、削除を行うことができ、操作はリアルタイムに一覧へ反映されます。

## 主な機能

- タスク（タイトル）の追加
- タスクの完了状態（チェックボックス）切り替え
- タスクの削除
- タスク一覧の取得・表示（作成日時の降順）
- 完了タスクと未完了タスクを UI 上で区別

## 使用技術

### フロントエンド

- **React 19** + **TypeScript**
- **Vite**（開発サーバー・ビルドツール）

### バックエンド

- **Hono**
- **Firebase Admin SDK**（Firestore エミュレータ）
- **Node.js**（TypeScript）

## セットアップ手順

### 1. リポジトリをクローン

```bash
git clone https://github.com/Seripro/todo-app.git
cd todo-app
```

### 2. バックエンドのセットアップ

```bash
cd backend
npm install        # 依存関係のインストール
npm run dev          # 開発モードでサーバー起動（http://localhost:3000）
```

#### Firestore エミュレータの起動（ローカル開発用）

バックエンドはローカルの Firestore エミュレータに接続します。別ターミナルで以下を実行してください。

```bash
npx firebase-tools emulators:start --only firestore --project demo-todo-app
```

### 3. フロントエンドのセットアップ

```bash
cd ../frontend
npm install        # 依存関係のインストール
npm run dev          # Vite 開発サーバー起動（http://localhost:5173）
```
