# サンデーモーニング

[English](README.en.md)

ニュースや保存記事を持ち寄り、AI司会と一週間を振り返るスキルです。曜日ごとにニュースを紹介し、選んだ話題の論点を一緒に決め、御意見番形式で対話します。最後に「今週のあっぱれ」を選びます。

## インストール

このリポジトリをクローンし、使いたい環境のスキルフォルダにコピーします。

```bash
git clone https://github.com/takuto-san/sunday-morning.git
cd sunday-morning
```

**Codex**（すべてのプロジェクトで利用）：

```bash
mkdir -p ~/.agents/skills
cp -R skills/sunday-morning ~/.agents/skills/
```

**Claude Code**（すべてのプロジェクトで利用）：

```bash
mkdir -p ~/.claude/skills
cp -R skills/sunday-morning ~/.claude/skills/
```

プロジェクト単位なら、それぞれプロジェクト内の `.agents/skills/` または `.claude/skills/` にコピーしてください。既に同名のスキルがある場合は内容を確認してから置き換えてください。新しいセッションで利用できます。

## 使い方

インストール後、新しいセッションで実行します。

- **Claude Code**：`/sunday-morning` と入力します。後ろに対象週や素材を添えることもできます。
- **Codex**：`/skills` を開いて `sunday-morning` を選びます。`$sunday-morning` でも明示的に呼び出せます。Codexでは `/sunday-morning` は独自のスラッシュコマンドとして登録されません。

対象週と、ニュース一覧や保存記事のリンクを渡してください。ニュース用と対話用に別の素材を使えます。未指定の場合は、開始時に確認します。

```text
対象週: 2026-01-05〜2026-01-11
ニュース:
- 2026-01-05（掲載日）｜記事のタイトル｜https://example.com/news
対話したい話題:
- 日付不明｜気になった投稿｜https://example.com/post
```

RSS、ブックマークのエクスポート、リンク集など、情報源は自由です。日付がある場合は公開日・保存日・一覧掲載日のいずれかを添えてください。番組名、言語、ジャンル、紹介件数も変更できます。

このスキルは進行の指示です。ニュースの自動取得や定期実行は含まず、利用できる情報源は各環境のツールや権限に依存します。投稿や公開は自動で行いません。
