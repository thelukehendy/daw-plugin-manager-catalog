# DAW Plugin Manager — public catalog feed

This repository is the **public version catalog** consumed by the DAW Plugin Manager app.

- App source / feedback / operator notes live in a **separate** (private) repo.
- Version authority is store-export only (`catalogSource: store-export:*`).
- Live feed: `catalog/catalog.json` + `catalog/catalog-version.json` (v2 pointer).

## Endpoints

| File | Role |
|------|------|
| [`catalog/catalog-version.json`](./catalog/catalog-version.json) | Tiny pointer (buildId, sha256, commit-pinned URLs) |
| [`catalog/catalog.json`](./catalog/catalog.json) | Full PluginCatalog |

**Pointer (raw):**  
`https://raw.githubusercontent.com/thelukehendy/daw-plugin-manager-catalog/main/catalog/catalog-version.json`

Do not treat mutable `@main/catalog/catalog.json` as the update path — the app uses commit-pinned URLs from the pointer.
