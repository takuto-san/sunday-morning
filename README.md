# サンデーモーニング

<img src="skills/sunday-morning/assets/commentator.png" alt="野球解説者を描いたドット絵のプロジェクトアイコン" width="160">

[English](README.en.md)

一週間のニュースをAI司会と番組形式で振り返るスキルです。ニュースを簡潔に紹介し、選んだ話題の論点を一緒に決めて対話します。

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

対象週と情報源を指定できます。ニュース収集を依頼した場合は、別途インストールした last30days スキルを呼び出して、国内外の政治・経済・社会・科学技術などを調べます。通常の話題調査には `--days=7` を使います。必要な情報が不足する場合は、開始時に質問します。

```text
対象週: 2026-01-05〜2026-01-11
ニュース:
- 2026-01-05（掲載日）｜記事のタイトル｜https://example.com/news
対話したい話題:
- 日付不明｜気になった投稿｜https://example.com/post
```

RSS、ブックマークのエクスポート、リンク集など、情報源は自由です。日付がある場合は公開日・保存日・一覧掲載日のいずれかを添えてください。番組名、言語、ジャンル、紹介件数も変更できます。

ニュース収集には [last30days](https://github.com/mvanhorn/last30days-skill) のインストールと、その実行条件が必要です。情報源の利用可否は環境や権限に依存します。定期実行や投稿・公開は自動で行いません。
