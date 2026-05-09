# Junto

> Кино — это повод встретиться.

Synchronous group movie watching: shared player, voice chat without echo, real-time reactions. Bring any source — file, magnet, Rutube, HLS — and Junto turns it into one stream for the whole room.

## Live

- 🌐 **[juntoapp.tech](https://juntoapp.tech)** — landing
- 📱 **[app.juntoapp.tech](https://app.juntoapp.tech)** — open the web client
- 🔌 `api.juntoapp.tech` — REST + WebSocket
- 🎙 `livekit.juntoapp.tech` — voice SFU

## Repositories

| Repo | What it is | Stack |
|---|---|---|
| **[junto-frontend](https://github.com/AbobaTeam-Production/junto-frontend)** | Mobile / desktop / web client | Flutter |
| **[junto-backend](https://github.com/AbobaTeam-Production/junto-backend)** | API + WebSocket + media pipeline | Django, Daphne, Celery, Postgres, Redis, LiveKit |
| **[junto-landing](https://github.com/AbobaTeam-Production/junto-landing)** | Marketing site (`juntoapp.tech`) | Static HTML, GitHub Pages |

## Downloads

Latest release artifacts (built by CI on every `v*` tag):

- 📥 [Android APK](https://github.com/AbobaTeam-Production/junto-frontend/releases/latest/download/junto-android.apk)
- 🪟 [Windows installer](https://github.com/AbobaTeam-Production/junto-frontend/releases/latest/download/junto-windows-setup.exe)

## Self-host

Run your own Junto stack on any Linux box — full Pro features, full control. Quickstart:

```bash
git clone https://github.com/AbobaTeam-Production/junto-backend
cd junto-backend
cp deploy/vps/.env.example .env  # fill in secrets
./deploy/vps/init-server.sh      # docker, certbot, ufw
./deploy/vps/deploy.sh           # docker compose pull + up + migrate
```

Detailed walkthrough: **[junto-backend/README#self-hosting](https://github.com/AbobaTeam-Production/junto-backend#self-hosting)**.

## Tech & licensing

- `junto-frontend` — Flutter, **MIT**
- `junto-backend` — Django + Daphne + Celery, **AGPL-3.0**
- `junto-landing` — static HTML, **MIT**

## Status

Beta. Web build auto-deploys on every push to `main`; APK/Win release per `v*` tag. Public Russian-speaking community-first build, but UI is fully localised RU/EN.
