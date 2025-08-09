# AI Command Station (Next.js, Node 20, Vercel-ready)

Minimal, clean starter that **builds on Node 20** and includes a health-check endpoint wired for SmartMail/SmartTalk.

## Quick start

```bash
npm ci
npm run build
npm start
```

## Deploy (Vercel)
- Node runtime: **20** (repo sets engines + `.nvmrc`; Vercel defaults to 22 but respects 20 when configured).
- Env vars to set:
  - `SMARTMAIL_API_URL`
  - `SMARTMAIL_API_KEY`
  - `SMARTTALK_API_URL`
  - `SMARTTALK_API_KEY`

Open `/api/health` to verify and use the buttons on the homepage to ping services.

## Files
- `package.json` – pinned `next@14.2.5`, `react@18.3.1`, Node engines `>=20 <21`
- `next.config.js` – `output: 'standalone'`
- `vercel.json` – maps `api/**/*.js` to `nodejs20.x`
- `.nvmrc` – `20`
- `pages/api/health.js` – verifies env + upstream health
- `components/CommandStation.jsx` – basic control card
- `pages/index.js` – simple UI shell
