# プロジェクト概要

AI家計簿アプリの市場調査シミュレーション。
LLMでペルソナ（架空の消費者）を生成し、施策に対する反応をシミュレーションし、集計・分析する。

# 技術スタック

- Python 3.11+
- Azure OpenAI API (`gpt-4o-mini`) — `.env` でエンドポイント・デプロイ名・APIキーを管理
- pandas, matplotlib, japanize-matplotlib

# セットアップ

- 初回実行時、必要な依存パッケージがインストールされていなければ自動でインストールする
- 必要パッケージ: openai, pandas, matplotlib, japanize-matplotlib, python-dotenv

# 環境変数

- `.env` ファイルから環境変数を読み込む（`python-dotenv`使用）
- `.env.example` をコピーして `.env` を作成し、各値を設定する
- `.env` が存在しない場合はエラーメッセージで作成手順を案内する

# ルール

- PoCなので、スピードと読みやすさを重視。保守運用性の考慮は一旦不要
- 出力ファイルは `output/` に保存する
- JSONは `ensure_ascii=False, indent=2` で日本語をそのまま保存
- matplotlibのグラフは `japanize_matplotlib` をimportして日本語表示する
- スクリプトはシンプルに。1ファイル1機能。スクリプトはそのまま上書き編集してよい
- レポートファイル（report_*.md）はバージョン付き（report_v1.md, report_v2.md...）で出力し、過去の記録を残す
- LLMへのプロンプトはスクリプト内にインラインで記述してよい
- エラー時は原因がわかるメッセージを出力する
- 不要なコメントや過剰なドキュメントは書かない
- ペルソナ生成数のデフォルトは50人
