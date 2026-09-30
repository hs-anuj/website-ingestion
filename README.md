# Acme Support Lab (GitHub Pages)

Synthetic public help-centre pages for **authorized crawler / content-ingestion testing**.
Edit a page, push, wait for Pages to rebuild, then re-run your ingest job against this site.

## Live URL

After Pages is enabled on `main`:

`https://hs-anuj.github.io/website-ingestion/`

## Page map

| Path | Purpose |
|------|---------|
| `/` | Home / discovery |
| `/faq/refunds/` | Normal policy page |
| `/faq/shipping/` | Second normal page |
| `/faq/hidden-notes/` | Hidden / commented text |
| `/faq/pii-sample/` | Synthetic personal data (fake only) |
| `/faq/with-links/` | Mix of public and internal-looking links |
| `/faq/accordion/` | Expandable sections |
| `/go-external/` | Redirect to another domain |
| `/go-internal/` | Redirect within this site |
| `/.well-known/site-verification.txt` | Placeholder for ownership-file checks |
| `/robots.txt` | Robots rules |

## Ownership file (optional)

Put any verification token your tool issues into:

`.well-known/site-verification.txt`

Then commit and push.

## Edit loop

```bash
cd ~/website-ingest-security-lab
# edit HTML under faq/
git add -A
git commit -m "Update lab content"
git push
```

## Safety

- All “PII” on this site is fake (`example.com`, `+1-555-0100`).
- Do not use third-party production sites for these tests.
- This repository is a content fixture only — no product secrets, tokens, or internal runbooks belong here.
