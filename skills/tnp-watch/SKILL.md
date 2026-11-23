---
name: tnp-watch
description: Find something to watch on TnP (tnp24.com) and give a link that starts it in the TnP player. Use when the user asks what to watch, looks for a film/series/episode, wants a themed list («зроби добірку», «що подивитись»), or something similar to a title.
---

# Find and watch on TnP

Tools come from the `tnp` MCP server.

1. Unclear wish ("щось атмосферне", "як Інтерстеллар") → `make_catalog` with the user's own words, or
   `similar_titles` with an imdb id from `search_titles`.
2. A concrete title → `search_titles` (any language: uk/ru/en). Several matches → ask which one (year, type).
3. Give the user `watch_url` from the result. A series episode → `open_in_player` with `season` and `episode`.
4. Show at most 5–7 titles: title (original + Ukrainian), year, one line why it fits, link.

Answer in the user's language. Never invent links: only `watch_url` / `url` returned by the tools.
