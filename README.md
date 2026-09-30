# hello-world-svelte-app

A **Svelte 5 + Vite** starter for [**Webflow Cloud**](https://webflow.com/cloud).

> Looking for the bindings variant (D1, R2, KV)?
> See [`hello-world-svelte-app-bindings`](https://github.com/Webflow-Examples/hello-world-svelte-app-bindings).

[![Deploy to Webflow](https://webflow.com/img/deploy-dark.svg)](https://webflow.com/dashboard/cloud/deploy?repo=https://github.com/Webflow-Examples/hello-world-svelte-app)

## Requirements

- Node **20+**

## What's included

- Svelte 5 (with runes) + Vite 6
- Tailwind CSS v3
- Branded Webflow Cloud landing page with doc links

## Quickstart

```bash
npm install
npm run dev
```

## Deploy to Webflow Cloud

1. Fork this repo.
2. In your Webflow site, open **Apps → Webflow Cloud → Create new app** and select this repo.
3. Push to your default branch to deploy.

## Customizing

Edit `src/App.svelte` to change the landing page content. Shared styles live in `src/app.css` under the `wf-*` class prefix.

## Learn more

- [Webflow Cloud docs](https://developers.webflow.com/webflow-cloud)
- [Quickstart](https://developers.webflow.com/webflow-cloud/quickstart)
- [Vite + Svelte on Webflow Cloud](https://developers.webflow.com/webflow-cloud/frameworks/vite-svelte)

---

Built with Svelte 5 + Vite · Deployed on Webflow Cloud.

## Branch naming convention

This repo is the canonical `hello-world-<framework>-app` example. Every framework
version and variant lives on a branch here, not in a separate repo:

| Branch | Contents |
| --- | --- |
| `main` | Current default example. Advances to the latest framework version once dependent pipelines are updated. |
| `vN` | Framework major version N, no storage bindings (for example `v6`). |
| `vN-with-bindings` | Version N plus D1, R2, and KV bindings and a `/api/binding-status` health check. |
| `sentry` | Latest version with bindings, plus a working Sentry setup. |

### Adding a new framework version

When a new major version M ships:

1. Create `vM` from the new plain app and `vM-with-bindings` from its bindings variant.
2. Point `sentry` at the latest version with bindings.
3. Leave `main` until the pipelines that consume this repo (webflow-cli,
   infrastructure/cosmic-builder, cosmic-test) are updated, then advance `main` to `vM`.
4. Keep older `vN` / `vN-with-bindings` branches so pinned references keep working.

Version branches (`vN`, `vN-with-bindings`, `sentry`) are protected: they can't be
deleted or force-pushed.
