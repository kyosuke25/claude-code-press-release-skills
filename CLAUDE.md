# プレスリリース管理

## 利用可能なスキル

| コマンド | 説明 |
|----------|------|
| `/press-release` | PRの新規作成・レビュー |

## 基本ワークフロー

1. `/press-release` を実行
2. 「新規作成」または「レビュー」を選択
3. 情報をヒアリング → Markdownでドラフト作成
4. pandocでWord変換
5. 画像挿入・微修正はWordで実施

## ルール構成

| ファイル | 内容 | セットアップ |
|---------|------|:------------:|
| `rules/press-release-format.md` | 構成・文体ルール | 不要 |
| `rules/folder-structure.md` | フォルダ構成 | 要 |
| `rules/file-naming.md` | ファイル命名規則 | 要 |
| `rules/company-info.md` | 会社情報・定型文 | 要 |

## セットアップ（初回のみ）

`.example` ファイルをコピーして編集：

```bash
cd rules
cp folder-structure.md.example folder-structure.md
cp file-naming.md.example file-naming.md
cp company-info.md.example company-info.md
```

各ファイルを自社のルールに合わせて編集。
