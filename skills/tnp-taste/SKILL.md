---
name: tnp-taste
description: Tune the user's personal TnP recommendations («Для вас») — likes, dislikes, favourite genres, moods, eras. Use when the user says what they love or hate, wants better or different recommendations, or asks why something is recommended.
---

# Tune «Для вас» on TnP

Tools come from the `tnp` MCP server. They change the inputs of TnP's own recommender; nothing is replaced.

1. Look first: `my_recommendations` (movie or series) and `taste_profile`.
2. Titles the user named → `search_titles` to get imdb ids → `preview_recommendations` to show what would change →
   after the user agrees, `rate_titles` (liked / disliked, ≤20 per call).
3. Broad taste ("більше фантастики, без жахів, 90-ті") → `taste_update` with option ids from `taste_profile.options`
   (`love` / `like` / `reject` / `clear`, `format`). Tell the user what changed. Wrong change → `taste_undo`.
4. Confirm before writing (rate_titles, taste_update). Then `my_recommendations` again so the user sees the effect.

Answer in the user's language.
