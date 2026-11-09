# HyperLine CMS

Standalone source export of `apps/cms` from `/opt/hyperline-ott` (2026-11-10). Next.js 15 / React 19 administrator UI for the separate HyperLine API.

## Local setup

```bash
npm ci
cp .env.example .env.local
npm run dev
```

Set `NEXT_PUBLIC_API_URL` to the API's `/api/v1` URL before building. Use a local/test API for development. `npm run typecheck` checks TypeScript; `npm run build` creates the production build. The supplied Dockerfile builds from this repository root; pass `--build-arg NEXT_PUBLIC_API_URL=...`.

Companions: [API](https://github.com/AungMyoNyein/hyperline-api), [web](https://github.com/AungMyoNyein/hyperline-web), [mobile](https://github.com/AungMyoNyein/hyperline-mobile).

Features: administrator sign-in/out, dashboard, movie/source editing, genre assignment and publication controls. Use approved existing credentials; no seeded administrator password is included. Changes to this source do not redeploy production.
