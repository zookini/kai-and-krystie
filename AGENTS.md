# Project Status & Guidelines

1. **GitHub Pages Ready**: All production files (`index.html`, `seating.html`, `seating.tsv`) are at the root. No build steps.
2. **Data Structure**: `seating.tsv` is tab-separated and serves as the source of truth for the seating chart.
3. **Local Testing**: Browser security (CORS) blocks `fetch` on local file systems. Use `serve.js` for local testing via: `fnm exec --using v24.10.0 -- node serve.js`. The server runs on port **3000**.
4. **Mobile Experience (Critical)**: The seating chart uses a fixed-viewport strategy on mobile. It uses a dense 3-column grid and a compact header to ensure all tables fit on a single screen without vertical scrolling. Maintain this density for any future mobile UI updates.
5. **Privacy**: Guest notes (allergies, etc.) are in the TSV but hidden in the public UI. Keep them private in any new guest-facing views.
6. **Tooling**: Use `fnm` for Node/NPX commands if needed.