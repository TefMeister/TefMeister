Working on things with Claude Code

---

### 📰 [Recent Activity](ACTIVITY.md)

---

## 🎮 Video games

VR mods for flat-screen games. A quick look at where each one stands, newest state only; the full
story is in each repo. Each game sits in the group that matches its status.

🎮 works in a headset · 🔧 being built · 🔍 studying the game · 🏆 breakthrough · ⭐ promising find · ⏸ paused · 📦 finished

### ✅ Works in headset

| Game | Engine | Where it stands | Updated | Repo |
| --- | --- | --- | --- | --- |
| **XIII** (2003) | Unreal Engine 2 | 🎮 Checked which draws are flat on the screen; only the HUD is. | 10-06 | [XIII2003-vr](https://github.com/TefMeister/XIII2003-vr) |
| **Psychonauts** (2005) | Double Fine engine | 🎮 Worked on the head-follow camera that went glitchy in the headset. | 10-08 | [psychonauts-vr](https://github.com/TefMeister/psychonauts-vr) |
| **Alice: Madness Returns** (2011) | Unreal Engine 3 | 🎮 Got the shadow fix working in the game; the menus now play by themselves. | 09-29 | [alice-madness-returns-vr](https://github.com/TefMeister/alice-madness-returns-vr) |
| **Visceral — RE2 VR** | RE Engine | 🔧 Worked on the grenade flipping in and out, the black pick-up screen, holsters that turn with you and auto-set options. | 10-09 | [visceral-re2-vr](https://github.com/TefMeister/visceral-re2-vr) |
| **Ashes 2063** (2018) | GZDoom | 🎮 Proved the cube shotgun catches the game's real lights, and recorded a flat test run. | 10-08 | [ashes-2063-weapons](https://github.com/TefMeister/ashes-2063-weapons) |

### 🔍 Early RE work

Reverse engineering: taking the game apart to find its camera and drawing code, before it can run in a headset.

| Game | Engine | Where it stands | Updated | Repo |
| --- | --- | --- | --- | --- |
| **Prototype** (2009) | Titanium | 🏆 Worked on checking lock-on with the head turned; needs enemies to test. | 10-01 | [prototype-vr](https://github.com/TefMeister/prototype-vr) |
| **Manhunt** (2003) | RenderWare | 🔍 Built drawing the world twice per frame, once per eye; not tried in the game yet. | 10-08 | [manhunt-2003-vr](https://github.com/TefMeister/manhunt-2003-vr) |
| **Mad Max** (2015) | Apex Engine | 🔧 Worked on keeping the HUD still while the view shifts per eye. | 09-30 | [mad-max-vr](https://github.com/TefMeister/mad-max-vr) |
| **Enslaved: Odyssey to the West** | Unreal Engine 3 | 🔧 Proved head movement turns and tilts the view, in the headset simulator. | 10-08 | [enslaved-vr](https://github.com/TefMeister/enslaved-vr) |
| **Alan Wake** (2010) | Remedy engine | 🔧 Head tracking works in a headset simulator; real headset next. | 10-06 | [alan-wake-vr](https://github.com/TefMeister/alan-wake-vr) |
| **Prince of Persia** (2008) | Scimitar | 🔧 Worked on a start-up safety fix for the graphics add-on. | 09-30 | [prince-of-persia-2008-vr](https://github.com/TefMeister/prince-of-persia-2008-vr) |
| **The Evil Within** (2014) | id Tech 5 | 🔧 Head tracking works in a headset simulator; the real headset is next. | 10-06 | [the-evil-within-vr](https://github.com/TefMeister/the-evil-within-vr) |
| **Hard Reset** (2011) | Road Hog Engine | 🏆 Worked on menus floating at a comfortable distance in the headset. | 10-08 | [hard-reset-vr](https://github.com/TefMeister/hard-reset-vr) |
| **The Witcher 2** (2011) | REDengine | 🔧 Worked on a small script add-on that shows the camera on screen. | 10-01 | [witcher-2-vr](https://github.com/TefMeister/witcher-2-vr) |
| **Metro Exodus** (2019, and the Enhanced Edition) | 4A Engine | 🔧 Rebuilt how the game's picture is passed to the headset. | 10-08 | [metro-exodus-vr](https://github.com/TefMeister/metro-exodus-vr) |
| **The Darkness** (2007) | Starbreeze engine | 🏆 Worked on the two-eye picture: the world holds still between the eyes, but the eyes sometimes swap. | 09-28 | [the-darkness-vr](https://github.com/TefMeister/the-darkness-vr) |
| **Condemned 2: Bloodshot** (2008) | Xbox 360 static recompilation (ReXGlue) | ⭐ Worked on running it on the fast PC, at well over 190 frames a second. | 09-23 | [condemned-2-vr](https://github.com/TefMeister/condemned-2-vr) |
| **Heavy Rain** (2010) | Quantic Dream engine | ⭐ Worked on a hidden debug menu and free camera found in the game. | 09-28 | [heavy-rain-vr](https://github.com/TefMeister/heavy-rain-vr) |
| **Far Cry 3: Blood Dragon** (2013) | Dunia | ⭐ Built showing both eyes side by side; the eye shift already works in the game. | 10-08 | [far-cry-3-blood-dragon-vr](https://github.com/TefMeister/far-cry-3-blood-dragon-vr) |
| **Deus Ex: Mankind Divided** (2016) | Dawn Engine | 🔍 First run: it starts, and it starts with our file in place. | 09-17 | [deus-ex-mankind-divided-vr](https://github.com/TefMeister/deus-ex-mankind-divided-vr) |
| **Bulletstorm: Full Clip Edition** (2011) | Unreal Engine 3 | 🔍 Worked on the HUD: it now shows in both eyes. | 10-07 | [bulletstorm-vr](https://github.com/TefMeister/bulletstorm-vr) |
| **Silent Hill 2** (2024 remake) | Unreal Engine 5.1 | 🔍 Worked on the frame rate in the headset, from 48 to 72 fps. | 09-29 | [silent-hill-2-remake-vr](https://github.com/TefMeister/silent-hill-2-remake-vr) |
| **Tomb Raider** (2013) | Foundation | ⭐ Worked on how to switch on the game's own built-in 3D mode for VR. | 10-08 | [tomb-raider-2013-vr](https://github.com/TefMeister/tomb-raider-2013-vr) |
| **Death Stranding Director's Cut** (2022) | Decima | ⭐ Worked on a small helper that will report where the camera data goes, the first time the game runs. | 10-01 | [death-stranding-vr](https://github.com/TefMeister/death-stranding-vr) |
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
| **Borderlands GOTY Enhanced** (2009) | Unreal Engine 3 | ⏸ Paused: a VR mod already exists (Mastersellz's BL1GOTYVR) | 09-26 | [borderlands-goty-vr](https://github.com/TefMeister/borderlands-goty-vr) |

### 📦 Finished

| Game | Engine | Where it stands | Updated | Repo |
| --- | --- | --- | --- | --- |
| **RE Village — VR scope** | RE Engine | 📦 Finished: v1.1.2 is out. Solved the scope's blue tint and made it lighter on the processor: it only draws while aiming, and dims when lowered. | 10-09 | [re-village-scope-vr](https://github.com/TefMeister/re-village-scope-vr) |
| **Arcade Controls for RE2 VR** | RE Engine | 📦 Closed. Shipped on Nexus to v1.5.0, replaced by Visceral | — | [arcade-controls-re2-vr](https://github.com/TefMeister/arcade-controls-re2-vr) |

All dates are 2026. Almost everything above is **one person, one machine, often one launch**, and
each repo's notes say so.

## 🧩 Plugins

Tools for working with Claude Code itself, not tied to any one game.

| Plugin | What it does | Where it stands | Repo |
| --- | --- | --- | --- |
| **Lanes** | Lets several Claude Code sessions work the same projects at once without treading on each other: a shared work board, one naming rule (nobody's name is written down unless they choose one), and ideas that get filed by themselves. Every project on this page is worked with it. | 🔧 0.53.0: a desktop shortcut named Lanes opens Claude Code in the plugin's look; offered once after the look goes on and after an update. | [lanes-plugin](https://github.com/TefMeister/lanes-plugin) |

## 🧊 Blender

Pixel-style cube models for games, built in Blender by script.

| Tool | What it does | Where it stands | Repo |
| --- | --- | --- | --- |
| **blender-cubekit** | A framework for making game models out of little cubes, like pixel art with depth: one cube size for everything, every number named, no lights, stop-motion animation, straight into the game. Comes with a Blender add-on (buttons and keys) and the write-ups on how it is done. The game models made with it stay in their own projects. | 🔧 0.18.0 (10-08): cubes of different sizes in one model: picked cubes go smaller for fine detail. | [blender-cubekit](https://github.com/TefMeister/blender-cubekit) |

## <img src="https://raw.githubusercontent.com/TefMeister/terminal-themes/main/icons/flower-icon.png" alt="" height="28" align="top"> Terminal Themes

Give your session a fresh look with one of these custom themes.

<img src="https://raw.githubusercontent.com/TefMeister/terminal-themes/main/preview/green-monitor-lanes.png" alt="The green monitor theme with the Lanes banner" width="480">

| Theme | What it looks like | Where it stands | Updated | Repo |
| --- | --- | --- | --- | --- |
| **Green monitor, Lanes banner** | The same old green screen, with the Lanes Plugin banner behind the text in one dim, striped green, so the letters stay easy to read. The look the Lanes plugin ships with. | 🔧 New today; replaced the starburst as the default. | 10-08 | [terminal-themes](https://github.com/TefMeister/terminal-themes) |
| **Green monitor, starburst flower** | An old green computer screen for Windows Terminal: sharp glowing letters, dark corners, and a faint striped flower behind the text, its petals placed like the rays of the Claude logo, with a light that slowly runs down the screen. | 🔧 First theme is up, with two plainer ones beside it; more to come. | 09-30 | [terminal-themes](https://github.com/TefMeister/terminal-themes) |
| **Ocean** | A calm pixel-art view under the sea: daylight sky over a still surface, light blue water, swaying plants, fish swimming near and far, a school of silver fish turning together, and now and then a passing whale. | 📦 Finished: scattered stars and chimney smoke in the window's colour were the last touches. | 10-08 | [terminal-themes](https://github.com/TefMeister/terminal-themes) |
| **Frequency** | A pixel-art background that keeps changing station like a spun radio dial. The first station runs from fish bones and diagonal skulls to a 1930s cartoon on an old TV and a flight through glitching, wildly coloured cubes. The second, where nothing is quite right, runs from a black hole swallowing a suburb to eyes, laughing lips and a night city made of letters. | 🔧 Worked on the big bang following the dive at once and the bottle pouring into a swirl. | 10-08 | [terminal-themes](https://github.com/TefMeister/terminal-themes) |
| **Halloween** | A pixel-art graveyard night: moon, witches on brooms, a witch's hut, candle-lit pumpkins and spiders on the glass. The sky darkens, a big sheet ghost rises in the wind, and lightning keeps flashing while it stays, lighting up the zombies shuffling towards you. | 🔧 Worked on a new preview clip that loops without a jump. | 10-01 | [terminal-themes](https://github.com/TefMeister/terminal-themes) |

## 🧹 BeG0nE tools and mods

Things that universally remove an unwanted feature or a fault from a video game. Each cure comes as a toolkit for
modders, human or AI, and as drop-in fixes for specific games.

| Cure | What it removes | Where it stands | Updated | Repo |
| --- | --- | --- | --- | --- |
| **Occlusion Drift BeG0nE** | In VR, a two-handed weapon's aim drifting because the front hand hides the back controller. The cure: hold the weapon with the left controller just above the right. First game: Resident Evil Village (REFramework). | 🔧 Worked on the Village grip, now shipped inside the RE Village scope mod v1.1.1. | 10-02 | [BeG0nE](https://github.com/TefMeister/BeG0nE/tree/main/occlusion-drift) |
| **Camera Jitter/Shake BeG0nE** | The stepped, jittery camera so many AI-written VR mods have. First find out why; then a tool for modders and a jitter-free camera for specific games. | 🔧 Built the ride-along: a mod logs when it reads the pose and writes the camera, and a background rider names the cause of any stepping and grows a jittery-versus-smooth knowledge base; Lanes starts it at every session. | 10-08 | [BeG0nE](https://github.com/TefMeister/BeG0nE/tree/main/camera-jitter) |

## 🤖 Automated navigation and movement

Tools that let a game get itself from launch to gameplay, so testing a mod does not start with the same menus
by hand every time.

| Tool | How it works | Where it stands | Updated | Where it lives |
| --- | --- | --- | --- | --- |
| **Menu‑o‑matiC** | Records the way through a game's menus once, as key presses plus small screen checkpoints, then replays it by itself. A replay looks at nothing: each checkpoint is a small patch of the screen compared by numbers. Only when something unexpected appears does it save a small picture for someone to look at. Plain Python, usable by anyone; also the `/lanes:menu` command in the Lanes plugin. | 🎮 Now maps a game's menus: separate routes to gameplay, to the key bindings (read once and remembered) and back out. Six games set up with the player; the recorder now takes three keys, and each game gets three goals. | 09-29 | [flat-to-vr-RE-toolkit](https://github.com/TefMeister/flat-to-vr-RE-toolkit/tree/main/tools/menu-o-matic) |
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
