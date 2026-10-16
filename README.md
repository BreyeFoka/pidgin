# pidgin

An early-stage dictionary for Pidgin English. So far this repo is the project setup: a Next.js web app and an Express API in a Turborepo monorepo, with shared environment validation. The dictionary itself isn't built yet.

## Structure

```
apps/web      Next.js front end
apps/server   Express API (currently a health check)
packages/env  Typed environment variables
```

## Run it

```bash
npm install
npm run dev     # web on http://localhost:3001, API on http://localhost:3000
```

The apps validate their environment on start, so copy the example values into `apps/web/.env` and `apps/server/.env` first.

## Checks

GitHub Actions runs `turbo check-types` and Biome on every push.
