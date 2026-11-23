# Deploy web UI to Vercel (free)

The React app can be public on Vercel. The Spring/Kafka backend is **not** hosted on Vercel — visitors need Docker locally or a separately deployed backend.

## One-time setup

1. Push this repo to GitHub (public).
2. Go to https://vercel.com → **Add New Project** → import this repo.
3. Configure:
   - **Root Directory:** `web`
   - **Framework Preset:** Vite
   - **Build Command:** `npm run build`
   - **Output Directory:** `dist`
4. Environment variables (optional for local-backend demos):

```
VITE_API_BASE_URL=
```

Leave empty if you only show the UI shell, or set it to a public API URL if you later host the gateway.

5. Deploy the frontend.

## CLI alternative

```bash
cd web
npm i -g vercel
vercel
```

Follow prompts; set root to current folder.

## Honest banner for interviewers

Add this text on the Vercel project description or README:

> Frontend preview on Vercel. Full payment saga (auth → wallet → Kafka fraud → credit) runs with Docker Compose — see the Quick Start section in the README.
