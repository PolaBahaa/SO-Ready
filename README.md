# SO Ready

Offline product pricing and quotation calculator (single self-contained HTML file, Arabic RTL UI, Odoo 18 pricing semantics).

## Versions

- **HTML**: `index.html` at the repo root. Open it in any browser; works fully offline.
- **Windows**: portable `.exe` built with Electron. No install, works offline.
- **Android**: `.apk` built from a minimal offline WebView wrapper in `android/`.

## One source, all versions

`index.html` is the only app source. Every push to `main` triggers the
`Build exe and apk` workflow, which copies `index.html` into the wrappers and
publishes a GitHub Release with the fresh `.exe` and `.apk`. To update all
versions, edit `index.html` and push.

## Repo layout

```
index.html            the app (single source of truth)
electron/             Windows wrapper (Electron, portable target)
android/              Android wrapper (WebView, offline, assets/index.html copied at build)
.github/workflows/    build + release automation
```
