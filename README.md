# Claude Code Press Release Skills

Claude Codeを使ったプレスリリース作成のためのスキル・ルールテンプレート

## 概要

このリポジトリは、Claude Codeでプレスリリースを効率的に作成・レビューするためのテンプレートです。

## ファイル構成

```
.claude/  (このリポジトリ)
├── README.md                    # このファイル
├── CLAUDE.md.example            # プロジェクト説明のテンプレート
├── skills/
│   └── press-release.md         # /press-release コマンド
├── rules/
│   ├── press-release-format.md  # 汎用ルール（そのまま使える）
│   └── company-info.md.example  # 会社情報テンプレート
└── templates/
    └── .gitkeep                 # Wordテンプレート用フォルダ
```

## セットアップ

### 1. クローン

プロジェクトの `.claude` フォルダとしてクローン：

```bash
cd your-project
git clone https://github.com/your-username/claude-code-press-release-skills.git .claude
```

### 2. 会社情報を設定

```bash
cd .claude
cp rules/company-info.md.example rules/company-info.md
```

`rules/company-info.md` を編集して、以下を入力：
- 会社名、所在地、代表者
- 問い合わせ先
- 会社概要の定型文

### 3. CLAUDE.mdを設定

```bash
cp CLAUDE.md.example CLAUDE.md
```

必要に応じて `CLAUDE.md` を編集。

### 4. （任意）Wordテンプレートを配置

既存のプレスリリースのWordファイルを `templates/press-release-template.docx` として配置すると、pandocでWord変換時にスタイルを継承できます。

### 5. pandocをインストール

```bash
# Windows (winget)
winget install --id JohnMacFarlane.Pandoc

# macOS (Homebrew)
brew install pandoc
```

## 使い方

Claude Codeで以下のコマンドを実行：

```
/press-release
```

### 機能

| モード | 説明 |
|--------|------|
| 新規作成 | 情報をヒアリングしてPRドラフトを生成 |
| レビュー | 既存PRをチェックして改善提案 |

### ワークフロー

1. `/press-release` を実行
2. 「新規作成」または「レビュー」を選択
3. 情報をヒアリング → Markdownでドラフト作成
4. pandocでWord変換
5. 画像挿入・微修正はWordで実施

## カスタマイズ

### ルールの変更

- `rules/press-release-format.md` - 構成・文体ルールを編集
- `rules/company-info.md` - 会社情報を編集

### スキルの変更

`skills/press-release.md` を編集して、ヒアリング項目やワークフローをカスタマイズできます。

## 必要なツール

- [Claude Code](https://claude.ai/code)
- [pandoc](https://pandoc.org/) - Markdown → Word変換用（任意）

## ライセンス

MIT License
