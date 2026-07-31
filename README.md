# AAA FPS (Three.js)

A browser-based first-person shooter built with Three.js r185 and Rapier physics.
No install. Runs on desktop and mobile.

## Play now

Primary (Cloudflare): https://aaa-fps-threejs.rose-spy.workers.dev

Mirror (GitHub Pages): https://ade5791.github.io/aaa-fps-threejs-build/

## Playing with friends

Same-screen rivalry: pick the same map and mode and compare scores.

LAN multiplayer: clone the source repo, run `npm install`, then
`npm run server` to start the WebSocket match server and share
`?host=<your-lan-ip>:8080` with friends on the same network.

## Controls

Desktop
- WASD move, mouse look, Left click fire, Right click ADS
- Shift sprint, Ctrl/C crouch (slide while sprinting), Space jump
- R reload, 1-9 weapon select, Esc pause menu

Mobile (phone or tablet, landscape)
- Left thumb: floating virtual stick (press anywhere lower-left, drag)
- Right thumb: drag anywhere on the right half to aim
- On-screen FIRE / ADS / JUMP / RELOAD / CROUCH / SPRINT / weapon swap

## Maps and modes

4 maps (Harbour, Dust2, Rust, Inferno) x 8 modes (Deathmatch, TDM,
Search and Destroy, Hardpoint, Domination, Kill Confirmed, Survival,
Gun Game). Pick both from the boot screen or the pause menu (Esc / MENU).

Query strings: `?map=rust&mode=tdm` jumps straight in.
