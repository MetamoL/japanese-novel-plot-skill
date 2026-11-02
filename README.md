# japanese-novel-plot-skill

AI に日本語の小説・Web小説を書かせる前に、一話・章・短編の筋と場面を設計させるAI エージェント用のスキルです。Claude Code・Codex など、`SKILL.md` を読むエージェントで使えます。

- AI の小説は、場面が出来事を並べるだけになり、転回が都合のよい偶然から生まれ、「悟って受け入れて」で閉じやすい。書く前に設計メモを作って、それを防ぐ
- 一話の問い（したいこと・阻むもの・終わりの変化・読者がこの話で得る満足・次を読む理由）、場面ごとの役割（対立・達成・交流・休息など）と変化、転回の出どころ、人物ごとの知識と誤解を決める
- 未決の設定は確定させず、作者への確認事項として返す

本文を書くスキル [japanese-novel-skill](https://github.com/MetamoL/japanese-novel-skill) と組み合わせて使えます。設計メモを作ってから、本文はそちらで書きます。

## 導入

**Claude Code**

```
/plugin marketplace add MetamoL/skills
/plugin install japanese-novel-plot-skill@metamol
```

**Codex・そのほかのエージェント**

```
npx skills add MetamoL/japanese-novel-plot-skill
```

入れるエージェントを選べます。どのプロジェクトでも使うときは `-g` を付けます。

**手で置く**ときは、このリポジトリをエージェントのスキルフォルダへ clone します（Claude Code は `~/.claude/skills/`、Codex は `~/.agents/skills/`）。

```
git clone https://github.com/MetamoL/japanese-novel-plot-skill ~/.claude/skills/japanese-novel-plot-skill
```

ほかのスキルは [MetamoL/skills](https://github.com/MetamoL/skills) にまとめています。

## English

An agent skill for Claude Code, Codex, and other agents that read `SKILL.md`: before an AI writes a chapter or short story in Japanese, it designs the plot and scenes. It decides what the protagonist wants and what blocks them, each scene's role (conflict, achievement, connection, rest), where each turn comes from, what every character knows or misunderstands, and what the reader gets from this chapter, so the draft does not become a list of events solved by coincidence and closed with an epiphany. Pairs with [japanese-novel-skill](https://github.com/MetamoL/japanese-novel-skill) for the prose itself.

The skill is written in Japanese and meant for Japanese fiction. Install with the commands above: the plugin for Claude Code, `npx skills add MetamoL/japanese-novel-plot-skill` for Codex and other agents, or clone this repository into your agent's skills folder.

## ライセンス

[LICENSE](LICENSE) のとおりです。自分の環境で使うこと・改変すること・作ったものの利用は自由です。再配布と転載はできません。
