# React Vite SPA Sample

A React single-page application built with Vite and React Router.

## Requirements

- Node.js 20.19 or later
- npm 10 or later

## Run locally

```powershell
npm install
npm run dev
```

## Build and preview

```powershell
npm run build
npm run preview -- --host 127.0.0.1 --port 8080
```

Open `http://localhost:8080`.

## Verify

With the production preview running:

```powershell
npm run lint
.\scripts\verify.ps1 -BaseUrl http://localhost:8080
```

## Builder Apps configuration

The root `builder.yaml` declares one component at `/`. It intentionally relies
on Vite detection to infer:

- The Node.js platform
- `npm run build`
- The `dist` output directory
- The static component role

This keeps the manifest limited to application intent that cannot be obtained
from the Vite repository itself.

## Routes

| Route | Purpose |
|---|---|
| `/` | React landing page and interactive hydration check |
| `/products/widget-1` | Direct client-side deep-link test |
| `/unknown-client-route` | React Router fallback test |
| `/health.json` | Static health marker |
| `/version.json` | Application and framework identity |
