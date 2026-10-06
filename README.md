# PARAS Estate Dashboards — United Malacca Bhd (UMB)

- `index.html` – portal: search and estate cards (reads `data/index.json`)
- `estate.html?e=<slug>` – shared dashboard template (reads `data/<slug>.json`)

- `data/` – one JSON per estate, built from the latest PA and Agronomy reports
- `netlify/functions/ask.mts` – the Ask feature (`/api/ask`); needs env var `ANTHROPIC_API_KEY`

To update an estate after a new report: replace `data/<slug>.json`, regenerate `data/index.json`, commit. Netlify redeploys automatically.

- `ANTHROPIC_WORKSPACE_ID` (needed for Console user keys starting `sk-ant-usr-`): the workspace ID, e.g. `wrkspc_...`. Sent as the `anthropic-workspace-id` header.
