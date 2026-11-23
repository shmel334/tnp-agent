# TnP plugin for AI agents

Connect your AI agent to [TnP](https://tnp24.com): find films and series, open them in the TnP player,
build themed lists and tune your «Для вас» recommendations. Works on your own Claude / ChatGPT subscription.

## Claude Code

```
claude plugin install tnp --marketplace shmel334/tnp-agent
```

Claude Code asks for your TnP token: tnp24.com → «АІ» → «API-ключ або свій сервер».

Using claude.ai with a Claude subscription? Add TnP there once (tnp24.com → «АІ» → «Claude»):
it then appears in Claude Desktop, mobile and Claude Code automatically. This plugin adds the skills on top.

## Codex

```
codex mcp add tnp --url <your personal address from tnp24.com → «АІ» → «Codex»>
```

## What the agent can do

| Tool | What |
|---|---|
| `search_titles`, `similar_titles`, `make_catalog` | find a title, similar ones, a themed list from a free description |
| `open_in_player` | link that starts a title or episode in the TnP player |
| `my_recommendations` | your personal «Для вас» row |
| `rate_titles`, `preview_recommendations` | likes / dislikes that steer recommendations, with a preview |
| `taste_profile`, `taste_update`, `taste_undo` | favourite genres, moods, eras — with undo |
| `device_guide` | how to watch on a TV, phone, computer, set-top box or VR |
| `report_feedback` | tell TnP what fit or did not — it learns from it |
