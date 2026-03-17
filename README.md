# 意図の変換ツール｜ALCHEMIST MASTER®

願望を3つの抽象度レベルの「意図」へ錬成するWebアプリです。

---

## 公開手順（Vercelを使った無料デプロイ）

### STEP 1｜GitHubにアップロード

1. [github.com](https://github.com) でアカウント作成（無料）
2. 「New repository」でリポジトリを作成（例：`intention-converter`）
3. このフォルダの全ファイルをアップロード

### STEP 2｜Vercelにデプロイ

1. [vercel.com](https://vercel.com) でアカウント作成（GitHubでログイン可）
2. 「Add New Project」→ GitHubのリポジトリを選択
3. 「Deploy」をクリック（設定は変更不要）

### STEP 3｜APIキーを設定（重要）

1. Vercelのプロジェクトページ →「Settings」→「Environment Variables」
2. 以下を追加：
   - **Name**: `ANTHROPIC_API_KEY`
   - **Value**: AnthropicのAPIキー（[console.anthropic.com](https://console.anthropic.com) で取得）
3. 「Save」→ 「Deployments」から「Redeploy」

### STEP 4｜公開完了！

`https://あなたのプロジェクト名.vercel.app` でアクセスできます。
独自ドメイン（例：`ito-henkan.jp`）も無料で設定できます。

---

## ファイル構成

```
intention-app/
├── api/
│   └── convert.js        ← サーバー側（APIキーを安全に保管）
├── src/
│   ├── App.jsx            ← メインのUIコンポーネント
│   └── main.jsx           ← エントリーポイント
├── index.html             ← HTMLテンプレート
├── package.json           ← 依存関係
├── vite.config.js         ← ビルド設定
└── vercel.json            ← Vercel設定
```

---

## ローカルで動かす場合

```bash
# 依存パッケージのインストール
npm install

# .env.localファイルを作成してAPIキーを設定
echo "ANTHROPIC_API_KEY=your_api_key_here" > .env.local

# 開発サーバー起動
npm run dev
```

---

## 注意事項

- APIキーは絶対にフロントエンドのコードに直接書かないでください
- `api/convert.js` がサーバー側でAPIキーを安全に管理します
- Vercelの無料プランで十分運用可能です

---

量子波動LABO【アルケミスト】｜現代の錬金術師：アルケミストマスター®
