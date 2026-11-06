# Tab Remote for DeskThing

Play/pause and jump ±5 seconds in the video playing in an Edge or Brave tab
(YouTube, Stremio web, and other HTML5 players), from your Car Thing.

Two parts:
- `dist/tabremote-v<version>.zip` — the DeskThing app (install in DeskThing)
- `extension/` — the browser extension (load unpacked in Edge or Brave)

They talk over `ws://127.0.0.1:38475`, which only accepts browser extensions.

## Rebuild after changes
    npm install
    npm run build        # makes dist/tabremote-v<version>.zip

## Where things are
- `server/index.ts`  actions, settings, local socket for the extension
- `src/App.tsx`, `src/index.css`  the Car Thing screen
- `extension/background.js`  finds the playing tab and moves the video
- `shared/types.ts`  messages between server and screen
