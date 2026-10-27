# tv-home-player

A one-page YouTube playlist player for a home-made Samsung TV launcher.

The launcher is a packaged Tizen web app, and YouTube refuses embeds from packaged apps (they send no Referer). This page gives the embedded player a real web origin. The launcher shows it in a small iframe and controls it with `postMessage`.

- `player.html?list=<playlist id>&autoplay=1`
- Commands in: `{"src":"home","cmd":"toggle"|"play"|"pause"|"next"|"prev"|"load","list":"…"}`
- Events out: `{"src":"tvplayer","type":"ready"|"state"|"error",…}`

No data is stored or collected. Playback uses YouTube's official IFrame Player API.
