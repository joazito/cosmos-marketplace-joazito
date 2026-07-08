# Joazito's Cosmos Marketplace

A community marketplace repository for [Cosmos OS](https://cosmos-cloud.io/).

## Add this repository to Cosmos

In your Cosmos dashboard, go to the Marketplace / App Store settings and add:

```
https://joazito.github.io/cosmos-marketplace-joazito/
```

## Currently available apps

| App | Description | Architectures |
|---|---|---|
| [Actual Budget](https://github.com/actualbudget/actual-server) | Privacy-focused budgeting with envelope methodology | amd64, arm64 |
| [Double Commander](https://doublecmd.sourceforge.io/) | Dual-pane file manager (LinuxServer.io) | amd64, arm64 |
| [neTV](https://github.com/jvdillon/netv) | Minimal IPTV player with EPG, VOD, GPU transcoding | amd64 |
| [nodecast-tv](https://github.com/technomancer702/nodecast-tv) | Modern IPTV player with EPG, VOD, Series, auth, hardware transcoding | amd64, arm64 |

## Adding a new app

1. Create a folder `servapps/<app-id>/` with:
   - `description.json` — name, description, tags, repository link, supported architectures
   - `cosmos-compose.json` — Cosmos-formatted compose with `{ServiceName}` templating, routes, labels
   - `icon.png` — app icon (512×512 recommended)
   - `screenshots/` — at least one screenshot (optional but recommended)
2. Add the app name to the showcase list in `index.js`
3. Push to `master` — the GitHub Actions workflow regenerates `index.json` and `servapps.json` automatically

## Based on

Structure follows the [ragdata/cosmos-servapps](https://github.com/ragdata/cosmos-servapps) format.
