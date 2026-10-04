# Pool Cards

Public daily NFL card feed for [Wayne's Family Pool](https://waynesfootballpool.com).

Sports Bot publishes six images under `latest/` and optional dated snapshots under `archive/YYYY-MM-DD/`. Upload every image first and `latest/manifest.json` last so readers never receive a manifest that references missing images.

## Manifest contract

- `schema`: `2`
- `date`: card date as `YYYY-MM-DD` in America/Chicago
- `generated_at`: ISO 8601 timestamp with offset
- `nfl_week`: NFL week number
- `cards`: six ordered entries

Each card entry contains:

- `id`: stable unique identifier
- `title`: reader-facing title
- `pick_type`: `straight_up` or `against_spread`
- `preview_file`: phone-sized WebP used in the carousel
- `full_file`: full-size image used when enlarged
- `width`, `height`: full-size dimensions
- `alt`: fresh accessible description

Legacy `file` remains accepted as a fallback, but new publications should provide both `preview_file` and `full_file`.

Model and expert cards are straight-up. The two spread cards are against the spread and must use `pick_type: "against_spread"`.

The repository is intentionally public and dedicated only to these cards. Do not publish credentials, private Pool data, or unrevealed family picks.
