# Changelog

## [0.1.1](https://github.com/RNZ01/palworld-server-dashboard/compare/0.1.0...0.1.1) (2026-07-27)


### Features

* **auth:** 4/4min brute-force limiter (failed-attempts only); hide owner account from mod widget ([d8ccb60](https://github.com/RNZ01/palworld-server-dashboard/commit/d8ccb60ceed87e607b910ed2d0f216df4c6891ec))
* **auth:** two-tier password system — full admin + MOD widget, server-side enforced ([c96d342](https://github.com/RNZ01/palworld-server-dashboard/commit/c96d3422f305c0acc782978b92044041e5f36d6b))
* **chat:** admin-gated journald chat API + fix login-probe lockout bug + per-IP failure dedup ([86c5e07](https://github.com/RNZ01/palworld-server-dashboard/commit/86c5e074db1f8eb215afe7baed0bef9dc2c178c3))
* **chat:** read live chat from a log file (systemd-less source) ([588fa63](https://github.com/RNZ01/palworld-server-dashboard/commit/588fa6390e0c5b6fe909e2c1fd3baddb86ef92c8))
* **chat:** read live chat from a log file (systemd-less source) ([f5817cc](https://github.com/RNZ01/palworld-server-dashboard/commit/f5817cc496ac9e3edafc270566d3114e75ea4c94))
* **chat:** show only chat messages in the console (joins/leaves filtered — count + roster cover presence) ([fe64404](https://github.com/RNZ01/palworld-server-dashboard/commit/fe644046159232012240098d9921b77d48306700))
* **dashboard:** live Chat console + send-on-click quick messages ([dfddabd](https://github.com/RNZ01/palworld-server-dashboard/commit/dfddabdeff32db3fcd22667f1526dde0b3b6a994))
* **dashboard:** player watchlist — eye-icon toggle pins flagged players to a top tier (owner order) ([28b9104](https://github.com/RNZ01/palworld-server-dashboard/commit/28b910456fc0d6d6f9a3338907839949de59a8e4))
* **docker:** add docker-compose configuration for dashboard and fps-… ([87fdf75](https://github.com/RNZ01/palworld-server-dashboard/commit/87fdf757ec9dbd7051c14da9578248d4d53f5186))
* **docker:** add docker-compose configuration for dashboard and fps-sampler services ([ce19136](https://github.com/RNZ01/palworld-server-dashboard/commit/ce191361d5eae8752a7f1faa35622b00281563aa))
* **fps-history:** ship the server-side FPS sampler ([e7d4d64](https://github.com/RNZ01/palworld-server-dashboard/commit/e7d4d643e670ed0d5303f6b67a06205a1c5d5fad))
* **fps:** run the FPS sampler in-process (replaces the sidecar/systemd sampler) ([dac059d](https://github.com/RNZ01/palworld-server-dashboard/commit/dac059da717872ffe2e651e3ebfdfe32c2a5df35))
* **fps:** run the FPS sampler in-process (replaces the sidecar/systemd sampler) ([09f216d](https://github.com/RNZ01/palworld-server-dashboard/commit/09f216dad7c7aa79b494a05e33f0d19eeea08af3))
* **map:** add touch pan/pinch-zoom support to live map ([b73d782](https://github.com/RNZ01/palworld-server-dashboard/commit/b73d7820ca4810382dbad036d8821032e25ba140))
* **map:** gmaps-style interaction — cursor-anchored zoom, fixed viewport, edge-clamped pan ([d59babe](https://github.com/RNZ01/palworld-server-dashboard/commit/d59babea6329438969944fe61b979c88ed011725))
* **map:** persist layer toggles in localStorage (owner order) ([3bcb824](https://github.com/RNZ01/palworld-server-dashboard/commit/3bcb824d9ed144bed2ec41e099927975db3f30fd))
* **map:** viewport-space nametags — fixed-rez, never scaled, gesture-delta tracked (owner spec) ([8a8954c](https://github.com/RNZ01/palworld-server-dashboard/commit/8a8954c9ed1346d536c2e020dd475b21d2e64d85))
* opt-in public read-only status page (/view) ([ec251f0](https://github.com/RNZ01/palworld-server-dashboard/commit/ec251f0fbb92a9684a7968556f51e63a8e3acdd7))
* opt-in public read-only status page (/view) with metrics, live map, and players ([262255c](https://github.com/RNZ01/palworld-server-dashboard/commit/262255c3188faea912ee07ad3610bfb9cb77c96a))
* **panel:** multi-tier auth, watchlist, warned restart, player actions — as deployed 2026-07-10/11 ([87771ef](https://github.com/RNZ01/palworld-server-dashboard/commit/87771ef86877a2869293d6bb55c995397edbdbab))
* **polling:** build-time snapshot cadence knob ([ed6f1e8](https://github.com/RNZ01/palworld-server-dashboard/commit/ed6f1e8c7c474a4218563f7bf4c881a813997958))
* **public-view:** optional player-name anonymization ([305ad90](https://github.com/RNZ01/palworld-server-dashboard/commit/305ad90060d76e44eac41f867d98df6dec56097e))


### Bug Fixes

* **chat:** absolute-fill feed so it matches row height instead of ballooning ([c879436](https://github.com/RNZ01/palworld-server-dashboard/commit/c87943606f9b85e448e04780410a11ed66ee3440))
* **dashboard:** two missed minutes-era countdown resets (post-fetch reset showed 1:00 on 1s rate) ([e246492](https://github.com/RNZ01/palworld-server-dashboard/commit/e2464929996cf99a0b632ffae7c8a6874b398c9c))
* **fps-graph:** plot against fixed 4h window with fixed -4h/-2h/Now axis (was stretching data span to full width) ([5ef9afc](https://github.com/RNZ01/palworld-server-dashboard/commit/5ef9afc8259e63e8b23b9cc70c78119d77535f87))
* **fps-history:** honor FPS_WINDOW_MINUTES in the dashboard window ([e51749b](https://github.com/RNZ01/palworld-server-dashboard/commit/e51749bfe651b283fb85254fa6f960b2f60bcd60))
* **fps-history:** honor FPS_WINDOW_MINUTES in the dashboard window ([192caf4](https://github.com/RNZ01/palworld-server-dashboard/commit/192caf43750495387ba159f0399ed3b6890d622c))
* **fps-sampler:** discard boot-window fps outliers (FPS_SANE_MAX, default 65) ([5f3b8ab](https://github.com/RNZ01/palworld-server-dashboard/commit/5f3b8ab030d683874a441779368f8e36fd51bc0e))
* **fps-sampler:** discard boot-window fps outliers (FPS_SANE_MAX, default 65) ([89cda8a](https://github.com/RNZ01/palworld-server-dashboard/commit/89cda8a16281fc359128fbc94911cabc876111d4))
* **map:** &lt;picture&gt; AVIF-primary (q85) + WebP fallback (q92) — Chromium gets AVIF quality, Firefox gets WebP ([b5240eb](https://github.com/RNZ01/palworld-server-dashboard/commit/b5240eb7bd37082aacfc22283b60a912f9c7b742))
* **map:** add touch pan/pinch-zoom support to live map ([74d0f1f](https://github.com/RNZ01/palworld-server-dashboard/commit/74d0f1fcbe27dfd0c43c7171a710c4a3212d77f2))
* **map:** correct origin-point projection bug and add missing fast travel points ([14dada9](https://github.com/RNZ01/palworld-server-dashboard/commit/14dada999d256b3347b41499201c21cba2d5e9a8))
* **map:** serve WebP not grid-AVIF — Firefox can't render tiled AVIF (same 3MB size, universal support) ([0ff9138](https://github.com/RNZ01/palworld-server-dashboard/commit/0ff9138a747cd2fb037940b2c65592ff1588fbb9))
* **polling:** sane REST cadences + 1h FPS history ([98d5cef](https://github.com/RNZ01/palworld-server-dashboard/commit/98d5cef828041f4b7336fdcac0a2fce16bef9cde))
* **public-view:** harden route review findings ([86b856f](https://github.com/RNZ01/palworld-server-dashboard/commit/86b856f11f1b6e38725c8023452e04ee0fe49ff3))
* re-apply owner-mandated 1s map refresh (reverted by layout rewrite) ([f3dd6f3](https://github.com/RNZ01/palworld-server-dashboard/commit/f3dd6f3ca98fb8828eea881719773cfab83f3cec))
* **refresh:** units were MINUTES — convert to seconds, default 1s (owner order) ([bcc38e9](https://github.com/RNZ01/palworld-server-dashboard/commit/bcc38e95d916207529c67a73592c4d9690c8ae17))


### Performance Improvements

* **map:** imperative compositor-path gestures + quantized grouping deps; remove refresh badge ([bdf9d6b](https://github.com/RNZ01/palworld-server-dashboard/commit/bdf9d6b28999a1b463edc74beba35f2eba449ee5))
* **map:** rAF-coalesced view updates, quantized grouping zoom, unpin giant layer ([1357629](https://github.com/RNZ01/palworld-server-dashboard/commit/135762915ffcd1261610e0725a3fbd63370bcf7c))
* **map:** restore will-change retained-layer fast path + zoom gesture smoothing ([7974f4d](https://github.com/RNZ01/palworld-server-dashboard/commit/7974f4da181e18705e2b4703b53c8d5714d1d14a))
* **map:** split image and marker layers — image raster never invalidated (owner-diagnosed) ([21ab1e7](https://github.com/RNZ01/palworld-server-dashboard/commit/21ab1e7f69740f1b34ea276842888ae3bf15aec6))


### Documentation

* add public /view page preview screenshot ([1dafda0](https://github.com/RNZ01/palworld-server-dashboard/commit/1dafda0d332928cb03d75febccc5f81f192cd025))


### Miscellaneous Chores

* compose/env docs to support FPS_SANE_MAX move into main container ([e5e3605](https://github.com/RNZ01/palworld-server-dashboard/commit/e5e36052e9d7f834b90da86a3366fda6c2f6215a))
* update Node.js version and dependencies; add knip configuration ([fd732f0](https://github.com/RNZ01/palworld-server-dashboard/commit/fd732f046d5c4f5a2be1a752266c167dd9581bd3))
* **upstream:** de-brand for general use ([851bcac](https://github.com/RNZ01/palworld-server-dashboard/commit/851bcac2f7db101ab77f841c56dbf8e85ae6b9eb))
* **upstream:** port multi-tier docker-compose + .env.example packaging from the panel-auth branch ([94165a2](https://github.com/RNZ01/palworld-server-dashboard/commit/94165a29a57d4c4b8b32387d6b57d481cca022ae))


### Code Refactoring

* **dashboard:** consolidate redundant metrics — Live Performance hero anchors the layout ([cbc9f26](https://github.com/RNZ01/palworld-server-dashboard/commit/cbc9f2686d8b48a5a55e1638c21f6640bb58a9ff))
