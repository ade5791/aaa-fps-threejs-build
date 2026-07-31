# AAA Three.js FPS - playable build

Play it here: https://ade5791.github.io/aaa-fps-threejs-build/

Browser-based first-person shooter built in Three.js r185 with Rapier physics.
No install, no plugin - it runs in any modern desktop or mobile browser with
WebGL2.

## Play with friends

Everything below works solo against bots. For head-to-head play one person
runs the dedicated server and shares the address:

1. Host runs the server from the source repo: `npm run server` (port 8787).
2. Host makes that port reachable (LAN address, or a tunnel such as
   `cloudflared tunnel --url http://localhost:8787` for a public wss:// URL).
3. Everyone opens the link above, presses the menu button, opens the
   MULTIPLAYER panel, pastes the host address plus a shared room code, and
   presses CONNECT.

Note: this page is served over HTTPS, so the browser requires a secure
`wss://` socket. A bare `ws://` LAN address is blocked by the browser as
mixed content - use a tunnel that terminates TLS.

## Controls

Desktop: WASD move, mouse look, left click fire, right click aim, R reload,
Shift sprint, Ctrl crouch/slide, Space jump, 1-9 weapons, Tab scoreboard,
Esc/menu button for the menu.

Mobile: on-screen stick (left) to move, drag anywhere on the right to look,
plus fire / aim / reload / jump / crouch buttons. Landscape orientation is
required; portrait shows a rotate prompt.

## Direct links

Map and mode can be pinned by query string, which skips the picker:

- `?map=harbour`, `?map=dust2`, `?map=rust`, `?map=inferno`
- `&mode=dm|tdm|sd|hp|dom|kc|survival|gun`

Example: `?map=rust&mode=tdm`

## What is in the build

- 4 maps (Harbour, Dust2, Rust, Inferno) with collision, zones and props
- 8 game modes, all playable solo against bots
- 9 weapons including 6 generated GLB weapon models
- Rigged, animated soldier enemies with patrol, cover-seek and return fire
- Deferred-ish PBR stack: PMREM environment probe, cascaded shadows, SSAO,
  TAA + FXAA, bloom, motion blur, godrays, single-owner tonemap
- Fully procedural WebAudio - no audio files

## Deployment

This branch is the published artifact only - a production `vite build` of the
source project, with the offline texture-authoring source PNGs stripped
(unreferenced at runtime). `.nojekyll` is present because GitHub Pages
otherwise runs Jekyll and drops underscore-prefixed paths.
