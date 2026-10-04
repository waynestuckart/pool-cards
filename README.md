# Pool Cards

Public daily NFL card feed for [Wayne's Family Pool](https://waynesfootballpool.com).

Sports Bot publishes images under `latest/` and dated snapshots under `archive/YYYY-MM-DD/`. Upload card files first and `latest/manifest.json` last so readers never receive a manifest that references missing images.

## Manifest contract

- `schema`: `1`
- `date`: card date as `YYYY-MM-DD` in America/Chicago
- `generated_at`: ISO 8601 timestamp with offset
- `nfl_week`: NFL week number
- `cards`: ordered card entries containing `id`, `title`, `file`, `width`, `height`, and fresh `alt` text

Supported images are PNG or WebP. Stable IDs are `nfl_scores`, `nfl_model_picks`, `nfl_expert_picks`, and `nfl_standings`. Model and expert picks are straight-up winners, not against the spread.
