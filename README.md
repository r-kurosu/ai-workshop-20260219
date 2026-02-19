# AI駆動開発ワークショップ

## セットアップ（所要時間：5分）

```bash
# 0. Claude Code をインストール（初回のみ）
curl -fsSL https://claude.ai/install.sh | bash
source ~/.bashrc

# インストール確認
claude --version
```
起動時にanthoropicのサブスクプラン認証があるので指示に従う。

上記でうまくいかない場合は、npm版（```npm install -g @anthropic-ai/claude-code```、Node.js 18+必要）でインストール


```bash
# 1. リポジトリをクローン
git clone https://github.com/r-kurosu/ai-workshop-20260219.git
cd ai-workshop-20260219

# 2. 環境変数ファイルを作成
cp .env.example .env
```

`.env` を開いて、以下の値を設定してください（当日案内します）：

```
AZURE_OPENAI_API_KEY=（当日案内）
AZURE_OPENAI_ENDPOINT=（当日案内）
AZURE_OPENAI_DEPLOYMENT=gpt-4o-mini
AZURE_OPENAI_API_VERSION=2024-08-01-preview
```

```bash
# 3. Claude Codeでセットアップ確認
claude "セットアップして"
```

## ハンズオンの進め方

各ステップで、Claude Codeに以下のように指示してください：

```bash
# Step 1: ペルソナ生成
claude "prompts/step1_persona.md を読んで、その通りに実装・実行して"

# Step 2: 施策シミュレーション
claude "prompts/step2_survey.md を読んで、その通りに実装・実行して"

# Step 3: 集計・分析
claude "prompts/step3_analyze.md を読んで、その通りに実装・実行して"

# Step 3-2: 自由分析（チャレンジ）
claude "prompts/step3-2_free_analyze.md を読んで、その通りに実装・実行して"
```
