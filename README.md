Working on things with Claude Code

---

### 📰 [Recent Activity](ACTIVITY.md)

---

## 🎮 Video games

VR mods for flat-screen games. A quick look at where each one stands, newest state only; the full
story is in each repo. Each game sits in the group that matches its status.

🥽 works in a headset · 🔧 being built · 🔍 studying the game · 🏆 breakthrough · ⭐ promising find · ⏸ paused · 📦 finished

### 🥽 Works in headset

| Game | Engine | Where it stands | Updated | Repo |
| --- | --- | --- | --- | --- |
| **XIII** (2003) | Unreal Engine 2 | 🥽 The newest 3D build now starts with the real headset on the home PC. | 10-10 | [XIII2003-vr](https://github.com/TefMeister/XIII2003-vr) |
| **Psychonauts** (2005) | Double Fine engine | 🥽 Fixed the head-turn glitch; the picture now turns with the head on the pretend headset. | 10-29 | [psychonauts-vr](https://github.com/TefMeister/psychonauts-vr) |
| **Alice: Madness Returns** (2011) | Unreal Engine 3 | 🥽 The picture now reaches the headset simulator through OpenXR. | 10-26 | [alice-madness-returns-vr](https://github.com/TefMeister/alice-madness-returns-vr) |
| **Visceral — RE2 VR** | RE Engine | 🥽 Found the ladder-start flick: the head's turn counted twice for three frames; a fix is built. | 10-29 | [visceral-re2-vr](https://github.com/TefMeister/visceral-re2-vr) |
| **Visceral — RE3 VR** | RE Engine | 🔧 The steady-light switch from RE2 is built in, waiting for its first run. | 10-30 | [visceral-re3-vr](https://github.com/TefMeister/visceral-re3-vr) |
| **Visceral — RE8 (Village) VR** | RE Engine | 🥽 Found and fixed why the hands sat low at some starts; the adapting light is held still and both eyes match. | 10-30 | [visceral-re8-vr](https://github.com/TefMeister/visceral-re8-vr) |
| **Ashes 2063** (2018) | GZDoom | 🥽 The player's body rig runs in the headset simulator: arms, torso and walking legs. | 10-29 | [ashes-2063-weapons](https://github.com/TefMeister/ashes-2063-weapons) |
| **Hard Reset** (2011) | Road Hog Engine | 🥽 The running game now answers Claude live: pictures, pose, log, keys, console. | 10-23 | [hard-reset-vr](https://github.com/TefMeister/hard-reset-vr) |
| **Far Cry 3: Blood Dragon** (2013) | Dunia | 🥽 Head tracking built and its headset code tidied; first test next. | 10-15 | [far-cry-3-blood-dragon-vr](https://github.com/TefMeister/far-cry-3-blood-dragon-vr) |
| **Silent Hill 2** (2024 remake) | Unreal Engine 5.1 | 🥽 Worked on the body layout: the right grip draws weapons from their spots, the left grip takes the map, syringe and drink. | 10-29 | [silent-hill-2-remake-vr](https://github.com/TefMeister/silent-hill-2-remake-vr) |
| **Condemned 2: Bloodshot** (2008) | Xbox 360 static recompilation (ReXGlue) | 🥽 First VR build released: it plays like a VR game with a controller. | 10-25 | [condemned-2-vr](https://github.com/TefMeister/condemned-2-vr) |
| **Manhunt** (2003) | RenderWare | 🥽 Found why the two eyes sat too far apart, and built the fix. | 10-29 | [manhunt-2003-vr](https://github.com/TefMeister/manhunt-2003-vr) |

### 🔍 Early RE work

Reverse engineering: taking the game apart to find its camera and drawing code, before it can run in a headset.

| Game | Engine | Where it stands | Updated | Repo |
| --- | --- | --- | --- | --- |
| **Brutal Doom** (Doom 1 and 2) | GZDoom | 🔧 The guns can now be built without hands, for the new body's own hands. | 10-29 | [brutal-doom-3d-guns](https://github.com/TefMeister/brutal-doom-3d-guns) |
| **Prototype** (2009) | Titanium | 🏆 Connected the headset to the head turn; tested without the game. | 10-14 | [prototype-vr](https://github.com/TefMeister/prototype-vr) |
| **Mad Max** (2015) | Apex Engine | 🔧 Worked on driving with your head turned: the ground no longer goes missing on small turns. | 10-15 | [mad-max-vr](https://github.com/TefMeister/mad-max-vr) |
| **Enslaved: Odyssey to the West** | Unreal Engine 3 | 🔧 Tidied the head-tilt log so it shows the game's real camera angle. | 10-15 | [enslaved-vr](https://github.com/TefMeister/enslaved-vr) |
| **Prince of Persia** (2008) | Scimitar | 🔧 Got our own camera following the Prince in normal play. | 10-16 | [prince-of-persia-2008-vr](https://github.com/TefMeister/prince-of-persia-2008-vr) |
| **The Witcher 2** (2011) | REDengine | 🔧 Turned the camera smoothly from outside the game, a first step to head tracking. | 10-16 | [witcher-2-vr](https://github.com/TefMeister/witcher-2-vr) |
| **Metro Exodus** (2019, and the Enhanced Edition) | 4A Engine | 🔧 Worked on keeping the picture's shape in each eye of the headset. | 10-15 | [metro-exodus-vr](https://github.com/TefMeister/metro-exodus-vr) |
| **The Darkness** (2007) | Starbreeze engine | 🥽 Worked on the hands: only the player's move now, and a hand poser lines them up. | 10-29 | [the-darkness-vr](https://github.com/TefMeister/the-darkness-vr) |
| **Heavy Rain** (2010) | Quantic Dream engine | ⭐ Built the code that sends the game's picture to the headset. | 10-29 | [heavy-rain-vr](https://github.com/TefMeister/heavy-rain-vr) |
| **Bulletstorm: Full Clip Edition** (2011) | Unreal Engine 3 | 🔍 Worked on sending the picture to a headset, each eye with its own view. | 10-16 | [bulletstorm-vr](https://github.com/TefMeister/bulletstorm-vr) |
| **Tomb Raider** (2013) | Foundation | ⭐ Worked on how to switch on the game's own built-in 3D mode for VR. | 10-08 | [tomb-raider-2013-vr](https://github.com/TefMeister/tomb-raider-2013-vr) |
| **Death Stranding Director's Cut** (2022) | Decima | ⭐ Built a read-only camera logger, ready for its first run. | 10-28 | [death-stranding-vr](https://github.com/TefMeister/death-stranding-vr) |
| **Burnout Paradise** (Remastered) | Criterion engine | 🏆 Worked on night driving: the headlights now get their per-eye fix at night. | 10-07 | [burnout-paradise-vr](https://github.com/TefMeister/burnout-paradise-vr) |

### ⏸ Paused

| Game | Engine | Where it stands | Updated | Repo |
| --- | --- | --- | --- | --- |
| **Unreal Gold** (1998) | Unreal Engine 1 | ⏸ Paused: a VR mod already exists (Unreal Revived) | 09-26 | [unreal-gold-vr](https://github.com/TefMeister/unreal-gold-vr) |
| **Far Cry 2** (2008) | Dunia | ⏸ Paused: another Far Cry 2 VR mod is in the works | 09-26 | [far-cry-2-vr](https://github.com/TefMeister/far-cry-2-vr) |
| **Dead Space 2** (2011) | RenderWare-based | ⏸ Paused: chortdev is making a Dead Space trilogy VR mod | 09-26 | [dead-space-2-vr](https://github.com/TefMeister/dead-space-2-vr) |
| **DOOM** (2016) | id Tech 6 | ⏸ Paused: a DOOM VR mod already exists (KHARVOX) | 09-26 | [doom-2016-vr](https://github.com/TefMeister/doom-2016-vr) |
| **Portal** (2007) | Source | ⏸ Paused: a Portal VR mod already exists (BowmanFox's portal1vr) | 09-26 | [portal-vr](https://github.com/TefMeister/portal-vr) |
| **Prey** (2017) | CryEngine | ⏸ Paused: fholger is making a Prey VR mod | 09-26 | [prey-2017-vr](https://github.com/TefMeister/prey-2017-vr) |
| **Alan Wake** (2010) | Remedy engine | ⏸ Paused: fholger is making an Alan Wake VR mod | 10-25 | [alan-wake-vr](https://github.com/TefMeister/alan-wake-vr) |
| **Deus Ex: Mankind Divided** (2016) | Dawn Engine | ⏸ Paused: someone else is making a Deus Ex: Mankind Divided VR mod | 10-27 | [deus-ex-mankind-divided-vr](https://github.com/TefMeister/deus-ex-mankind-divided-vr) |
| **The Evil Within** (2014) | id Tech 5 | ⏸ Paused: a VR mod is being worked on | 10-27 | [the-evil-within-vr](https://github.com/TefMeister/the-evil-within-vr) |
| **Borderlands GOTY Enhanced** (2009) | Unreal Engine 3 | ⏸ Paused: a VR mod already exists (Mastersellz's BL1GOTYVR) | 09-26 | [borderlands-goty-vr](https://github.com/TefMeister/borderlands-goty-vr) |

### 📦 Finished

| Game | Engine | Where it stands | Updated | Repo |
| --- | --- | --- | --- | --- |
| **RE Village — VR scope** | RE Engine | 📦 Finished: v1.1.5 released on GitHub on 2026-10-14 — the scope works as it should. | 10-14 | [re-village-scope-vr](https://github.com/TefMeister/re-village-scope-vr) |
| **Arcade Controls for RE2 VR** | RE Engine | 📦 Closed. Shipped on Nexus to v1.5.0, replaced by Visceral | — | [arcade-controls-re2-vr](https://github.com/TefMeister/arcade-controls-re2-vr) |

All dates are 2026. Almost everything above is **one person, one machine, often one launch**, and
each repo's notes say so.

## 🧩 Plugins

Tools for working with Claude Code itself, not tied to any one game.

| Plugin | What it does | Where it stands | Repo |
| --- | --- | --- | --- |
| **Lanes** | A growing collection of tools, skills and programs for Claude Code, primarily meant for flat-to-VR video game modding. Optional and modular as much as possible, and it ships with a rule to not say "You're right!" :) | 🔧 10-28: [0.95.0](https://github.com/TefMeister/lanes-plugin/releases/tag/v0.95.0): a security and privacy test day; a new check at session start says when a project's game moved, changed or went missing. | [lanes-plugin](https://github.com/TefMeister/lanes-plugin) |

## 🧊 Blender

Pixel-style cube models for games, built in Blender by script.

| Tool | What it does | Where it stands | Repo |
| --- | --- | --- | --- |
| **blender-cubekit** | A framework for making game models out of little cubes, like pixel art with depth: one cube size for everything, every number named, no lights, stop-motion animation, straight into the game. Comes with a Blender add-on (buttons and keys) and the write-ups on how it is done. The game models made with it stay in their own projects. | 🔧 10-24: adding and carving can keep a model's colour pattern, or use one chosen colour. | 10-24

## <img src="https://raw.githubusercontent.com/TefMeister/terminal-themes/main/icons/flower-icon.png" alt="" height="28" align="top"> Terminal Themes

Give your session a fresh look with one of these custom themes.

<img src="https://raw.githubusercontent.com/TefMeister/terminal-themes/main/preview/green-monitor-lanes.png" alt="The green monitor theme with the Lanes banner" width="480">

| Theme | What it looks like | Where it stands | Updated | Repo |
| --- | --- | --- | --- | --- |
| **Green monitor, Lanes banner** | The same old green screen, with the Lanes Plugin banner behind the text in one dim, striped green, so the letters stay easy to read. The look the Lanes plugin ships with. | 🔧 New today; replaced the starburst as the default. | 10-08 | [terminal-themes](https://github.com/TefMeister/terminal-themes) |
| **Green monitor, starburst flower** | An old green computer screen for Windows Terminal: sharp glowing letters, dark corners, and a faint striped flower behind the text, its petals placed like the rays of the Claude logo, with a light that slowly runs down the screen. | 🔧 First theme is up, with two plainer ones beside it; more to come. | 09-30 | [terminal-themes](https://github.com/TefMeister/terminal-themes) |
| **Ocean** | A calm pixel-art view under the sea: daylight sky over a still surface, light blue water, swaying plants, fish swimming near and far, a school of silver fish turning together, and now and then a passing whale. | 📦 Day and night added: three minutes each, stars by night, rare sunbeams by day. | 10-24 | [terminal-themes](https://github.com/TefMeister/terminal-themes) |
| **Frequency** | A pixel-art background that keeps changing station like a spun radio dial. The first station runs from fish bones and diagonal skulls to a 1930s cartoon on an old TV and a flight through glitching, wildly coloured cubes. The second, where nothing is quite right, runs from a black hole swallowing a suburb to eyes, laughing lips and a night city made of letters. | 🔧 Worked on glitches in patches all over the window and the cartoon running back the other way. | 10-23 | [terminal-themes](https://github.com/TefMeister/terminal-themes) |
| **Halloween** | A pixel-art graveyard night: moon, witches on brooms, a witch's hut, candle-lit pumpkins and spiders on the glass. The sky darkens, a big sheet ghost rises in the wind, and lightning keeps flashing while it stays, lighting up the zombies shuffling towards you. | 🔧 Worked on the ravens, now a very dark grey, and a 12-minute video of the night. | 10-23 | [terminal-themes](https://github.com/TefMeister/terminal-themes) |

## 🧹 BeG0nE tools and mods

Things that universally remove an unwanted feature or a fault from a video game. Each cure comes as a toolkit for
modders, human or AI, and as drop-in fixes for specific games.

| Cure | What it removes | Where it stands | Updated | Repo |
| --- | --- | --- | --- | --- |
| **Occlusion Drift BeG0nE** | In VR, a two-handed weapon's aim drifting because the front hand hides the back controller. The cure: hold the weapon with the left controller just above the right. First game: Resident Evil Village (REFramework). | 🔧 Worked on the Village grip: a reload is no longer cancelled by the block gesture, and a grip now needs the hand near the gun. Shipped inside the RE Village scope mod. | 10-28 | [BeG0nE](https://github.com/TefMeister/BeG0nE/tree/main/occlusion-drift) |
| **Camera Jitter/Shake BeG0nE** | The stepped, jittery camera so many AI-written VR mods have. First find out why; then a tool for modders and a jitter-free camera for specific games. | 🔧 Built the ride-along: a mod logs when it reads the pose and writes the camera, and a background rider names the cause of any stepping and grows a jittery-versus-smooth knowledge base; Lanes starts it at every session. | 10-08 | [BeG0nE](https://github.com/TefMeister/BeG0nE/tree/main/camera-jitter) |
| **Ghost Hand BeG0nE** | In VR, the gaps between your real hand and the player's hand: lag, offset, jumps and lost tracking that make hand gestures like racking a slide miss. It records both controllers and the game's hands, then points at where they part. | 🔧 Built today: the recorder and its report maker, shipped in Lanes. First job: hand racking in RE2. | 10-12 | [BeG0nE](https://github.com/TefMeister/BeG0nE/tree/main/ghost-hand) |
| **Flickers BeG0nE** | In VR, parts of the picture flashing wrong for a single frame, like the grass in Resident Evil 4 with REFramework. It catches the flash and shows what it is, then shows the frame before in its place. | 🔧 Built the catcher and its reader as one REFramework plugin file; it found every fake flicker on the headset simulator. | 10-26 | [BeG0nE](https://github.com/TefMeister/BeG0nE/tree/main/flickers) |

## ❄️ VR helpers

Small programs that make working in a headset easier, for any game.

| Tool | How it works | Where it stands | Updated | Where it lives |
| --- | --- | --- | --- | --- |
| **Hand Freeze** | A desktop app that holds the VR controllers still in any OpenXR game, left, right or both. Press the snowflake, hold the controllers where the hands should be, and after a countdown they stay put while the game keeps running, so hand poses can be tuned with the mouse. | 🔧 v4: a click of the right thumbstick freezes or frees both hands, and the game never sees that click. | 10-25 | [hand-freeze-vr](https://github.com/TefMeister/hand-freeze-vr) |
| **VR Bench** | A robot player for VR games. With the OpenXR Simulator as the headset, it moves the head, both hands and every button by itself, takes a picture after each, and writes down what the game did, so VR work can be tested with nobody wearing anything. | 🔧 v0.1.1: its log now says in one line why a hand does or does not move; it also steps around the room, bends over and crouches like a standing player. | 10-27 | [vr-bench](https://github.com/TefMeister/vr-bench) |
| **Window View** | A desktop app plus an OpenXR layer that hangs any open window in front of your eyes inside the game, like an in-game menu that turns with your head. Add as many as you like, set how see-through each is, drag them by their header, resize them by their corner. Page Up hands your mouse and keyboard to the floating windows (the game sees nothing and is played with the controllers); Page Down hands them back. | 🔧 1.7.2: holding the left stick half a second (was 2 s) shows or hides Window View in the headset. | 10-29 | [window-view-vr](https://github.com/TefMeister/window-view-vr) |
| **Hand Poser** | A compact window of sliders that poses the player's hands in RE Engine games: add any bone, turn it, see which bones move with it, undo, redo, and keep named pose builds. Meant to hang inside the headset through Window View while Hand Freeze holds the controllers. Inspired by alphaZomega's EMV Engine poser. | 🔧 v0.2 download: one button per hand, the joint list folded away; in use with Visceral RE8. | 10-28 | [hand-poser-vr](https://github.com/TefMeister/hand-poser-vr) |
| **Grip Zones** | A small window of sliders that moves and resizes every place the hand can grip a gun in VR: the magazine, the well, the slide, pump or bolt, the front grip. Each zone moves on the gun in the game at once, for one gun or all. Hangs inside the headset through Window View. Works with Visceral RE8 for now; more games as we mod them. | 🔧 v1.3 download: Gun Poser moved to its own page; the sliders reach a rifle's length. | 10-29 | [grip-zones-vr](https://github.com/TefMeister/grip-zones-vr) |
| **Gun Poser** | A small window of sliders that aims and moves the gun in the right hand in VR: up or down, left or right, roll, and forward, up or sideways in the hand, for one gun or all. Hangs inside the headset through Window View. Works with Visceral RE8 for now; the idea is to make it work across many games. | 🔧 v1.0 download: its own page and icon; not yet tried in the headset. | 10-28 | [gun-poser-vr](https://github.com/TefMeister/gun-poser-vr) |

## 🤖 Automated navigation and movement

Tools that let a game get itself from launch to gameplay, so testing a mod does not start with the same menus
by hand every time.

| Tool | How it works | Where it stands | Updated | Where it lives |
| --- | --- | --- | --- | --- |
| **Menu‑o‑matiC** | Records the way through a game's menus once, as key presses plus small screen checkpoints, then replays it by itself. A replay looks at nothing: each checkpoint is a small patch of the screen compared by numbers. Only when something unexpected appears does it save a small picture for someone to look at. Plain Python, usable by anyone; also the `/lanes:menu` command in the Lanes plugin. | 🎮 Each game now keeps a note of what sessions have learned about driving it, read before every launch and added to as they go. | 10-14 | [flat-to-vr-RE-toolkit](https://github.com/TefMeister/flat-to-vr-RE-toolkit/tree/main/tools/menu-o-matic) |
| **Move‑o‑matiC** | Moves a character or car along a route. The player drives or walks it once while every key and how long it was held is recorded, and marks where to check it arrived; after that it repeats the route by itself. Each game is first set up together with the player: save point, menu buttons, controls, and a check that inputs reach the game. | 🔧 First Burnout drive recorded with the player; each drive now comes with a short plan, and the recorder's keys moved to Page Up/Down, Home and End. | 09-29 | [flat-to-vr-RE-toolkit](https://github.com/TefMeister/flat-to-vr-RE-toolkit/tree/main/tools/menu-o-matic) |
| **State‑o‑matiC** | Tells whether a game is in a menu, loading, a cutscene, or gameplay, from signs that work outside almost any game: black bars, how much of the picture moves, a lone spinning icon, how hard the game reads its disk, and whether the picture answers a key. Screens that fool it are shown to it once during setup. | 🔧 First live run on Burnout: loading screens and the idle cinematic camera read right; menus with a moving car behind them need teaching. | 09-28 | [flat-to-vr-RE-toolkit](https://github.com/TefMeister/flat-to-vr-RE-toolkit/tree/main/tools/menu-o-matic) |

## How the game repos are organized

**One repo per game.** Consolidated on 2026-08-30 from the earlier
six-repos-per-game layout — every folder below used to be its own repo and
keeps its full git history. Inside each game repo:

| Folder | What's there |
| --- | --- |
| `mod/` | Release packaging and player-facing docs — the releases themselves are on the repo's Releases page |
| `dev-archive/` | The live mod source plus the full messy in-progress history: snapshots, probes, dead ends |
| `modding-notes/` | Readable field notes / progress ledger, one dated entry per session |
| `engine-research/` | Distilled current truth: the engine dossier (the shared VR-RE playbook it follows lives in the toolkit, linked below) |
| `external-research/` | Public-research leads (prior art, techniques) gathered separately from hands-on modding |

Work-in-progress that isn't ready for browsing lives in one private `staging`
repo, a folder per game. Release notes always carry a disclaimer of what the mod
is/isn't, plus a motion-sickness caution while a project is unfinished.

Since 2026-08-26 the whole account also runs on a **one-writer-per-file rule**. Several of my
sessions can work a project at the same time — hands-on modding, per-game public research, and a
cross-project research sweep — so every folder above has exactly one session type that curates it,
and anything one lane finds for another travels as a dated, create-only file in the receiving
lane's `inbox/` folder; the owning session folds it into the curated docs and deletes it. So if
you see an `inbox/` folder with files in it, that's knowledge in transit between sessions, not
clutter. The full playbook text lives only in
[flat-to-vr-RE-toolkit](https://github.com/TefMeister/flat-to-vr-RE-toolkit) (each project's
`PLAYBOOK.md` is a pointer to it), and cross-game engine knowledge is unified in the library's
[per-engine family pages](https://github.com/TefMeister/flat-to-vr-cross-engine-research/tree/main/docs/engines)
— one page per engine family, linking every sibling project's dossier.

## Shared knowledge (applies across every project, and to games with no project yet)

- **[flat-to-vr-cross-engine-research](https://github.com/TefMeister/flat-to-vr-cross-engine-research)** — a public, engine-agnostic library of *publicly-available* flat→VR modding knowledge: an engine landscape index, [per-engine family pages](https://github.com/TefMeister/flat-to-vr-cross-engine-research/tree/main/docs/engines) tying my sibling projects on the same engine together, generic-driver options (vorpX, geo-11), engine-agnostic core patterns, and worked case studies. Every source credited in its `ATTRIBUTION.md`.
- **[flat-to-vr-RE-toolkit](https://github.com/TefMeister/flat-to-vr-RE-toolkit)** — battle-tested tools, skills, and the canonical copy of the reusable VR reverse-engineering playbook every project above follows.

---

*All reverse-engineering here targets legitimate copies of each game (owned, or free from the official source) for personal,
non-commercial modding. No original game assets or engine source are redistributed in any
repo above. Corrections/removal requests from actual rights holders are honoured promptly —
contact details are in each repo's `CONTRIBUTING.md`.*
