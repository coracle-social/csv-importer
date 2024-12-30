# Nostr CSV Uploader

A nostr micro-app which allows the user to sign and publish events in bulk via CSV.

Use it at [csv.coracle.social](https://csv.coracle.social).

## Preparing your file

CSVs should have "kind", "content", "created_at", and "tags" headings. All headings are required, and must be in order, but `content`, `tags`, and `created_at` may be blank.

- `kind` must be an integer matching the desired event kind
- `content` must be a string to be placed in the event content
- `created_at` must be an integer representing the number of _seconds_ since the unix epoch. Leave this blank and the app will fill it in to the current time.
- `tags` may be blank, or it may be a comma-separated list of tag parameters. Each cell to the right may be an additional tag. Be sure to quote your tags to avoid confusing the CSV parser.
