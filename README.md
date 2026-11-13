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
| **Condemned 2: Bloodshot** (2008) | Xbox 360 static recompilation (ReXGlue) | 🥽 The hands now follow the motion controllers through the game's own arm movement (build 4), the Quest controllers work as the gamepad, and the main menu has a Quit line where Multiplayer was; all checked on the pretend headset, not yet worn. Real swings for melee are next. | 11-12 | [condemned-2-vr](https://github.com/TefMeister/condemned-2-vr) |
| **Begin Again (Tale of Two Wastelands) in KUPOkinz's TTWVR** | Gamebryo (Fallout: New Vegas) | 🥽 Tale of Two Wastelands with KUPOkinz's TTWVR plays clean in the headset; Begin Again's mods are staged back in seven steps, each checked to start and load a save with the VR mod on (in a simulated headset), ready for the real headset one step at a time. Every step, the eighth now split into three, passes the desk check in the pretend headset; the 360 Movement mod, whose warning box smeared the view, is now left out of the VR steps, drawing a weapon from the shoulder works, and Begin Again's dense far view comes in at the third step. The fourth step has been worn: four things to sort out there (the holster, the water, the waterline and a smear across the view); Begin Again's full far view now shows in VR on the top step, and the water, a flat green sheet in VR, is the VR mod drawing water over the nearer land. A new check says before a start whether a save will bring up the missing-content box. | 11-13 | [ba-ttr-vr-bridge](https://github.com/TefMeister/ba-ttr-vr-bridge) |
| **Psychonauts** (2005) | Double Fine engine | 🥽 Fixed the head-turn glitch; the picture now turns with the head on the pretend headset. | 10-29 | [psychonauts-vr](https://github.com/TefMeister/psychonauts-vr) |
| **Alice: Madness Returns** (2011) | Unreal Engine 3 | 🥽 The picture now reaches the headset simulator through OpenXR. | 10-26 | [alice-madness-returns-vr](https://github.com/TefMeister/alice-madness-returns-vr) |
| **Visceral — RE2 VR** | RE Engine | 🥽 A torch you hold in the left hand and six holster spots (hips, shoulders, back) work on the pretend headset and are ready to wear; every handgun shows real rounds in its magazine. | 11-12 | [visceral-re2-vr](https://github.com/TefMeister/visceral-re2-vr) |
| **Visceral — RE3 VR** | RE Engine | 🥽 A torch you hold in the left hand and six holster spots (hips, shoulders, back) work on the pretend headset, and Jill's chest lamp is gone in play; the grenade launcher loads by hand, round by round. | 11-12 | [visceral-re3-vr](https://github.com/TefMeister/visceral-re3-vr) |
| **Visceral — RE8 (Village) VR** | RE Engine | 🥽 A torch you hold in the left hand, drawn from the left shoulder, works on the pretend headset, and the view now stays yours when Ethan examines something (proven on the flat screen, built for VR); the thumbsticks drive the VR options menu, and a spare magazine taken from the pouch now hangs under the gun and moves with the left hand (build 119). All wait for a real headset try. | 11-13 | [visceral-re8-vr](https://github.com/TefMeister/visceral-re8-vr) |
| **Ashes 2063** (2018) | GZDoom | 🥽 The guns' look is settled: the game's own pictures in solid cubes, carved and scratched; the JackHammer is next in it. It now also runs on the pretend headset, for tests with nobody wearing one. The shotgun is being reshaped with Tefa (round 12: a bulkier body, bigger shells, a shell port onto the barrel); the stepping "framey gun" was tried and switched off, as it felt bad at every setting. | 11-12 | [ashes-2063-weapons](https://github.com/TefMeister/ashes-2063-weapons) |
| **Hard Reset** (2011) | Road Hog Engine | 🥽 The running game now answers Claude live: pictures, pose, log, keys, console. | 10-23 | [hard-reset-vr](https://github.com/TefMeister/hard-reset-vr) |
| **Far Cry 3: Blood Dragon** (2013) | Dunia | 🥽 Head tracking built and its headset code tidied; first test next. | 10-15 | [far-cry-3-blood-dragon-vr](https://github.com/TefMeister/far-cry-3-blood-dragon-vr) |
| **Silent Hill 2** (2024 remake) | Unreal Engine 5.1 | 🥽 Worn with ray tracing and DLSS on: the game's own cutscenes play on a big screen, the opening-cutscene crash and James's black eyes are cured, and the frame warp runs on the real headset (it switches itself on), at about 62 fps on average, and walking around your room now steps aside whenever the game steers James, with no more short freezes (build 18, worn). The frame warp's maker, PureDark, has allowed a look inside it for this game; the outline around the hands is now reproduced without the headset, and one warp setting avoids it (to try in the headset); the A button at the main menu still does nothing. | 11-13 | [silent-hill-2-remake-vr](https://github.com/TefMeister/silent-hill-2-remake-vr) |
| **The Darkness** (2007) | Starbreeze engine | 🥽 The journal now hangs in the room instead of following your head (build 029), the main menu has a QUIT line in the game's own font, and other people's hands no longer copy yours up close; the faster way of drawing the picture is 37 to 68 percent quicker with the same picture. Waiting to be worn. | 11-12 | [the-darkness-vr](https://github.com/TefMeister/the-darkness-vr) |

### 🔍 Early RE work

Reverse engineering: taking the game apart to find its camera and drawing code, before it can run in a headset.

| Game | Engine | Where it stands | Updated | Repo |
| --- | --- | --- | --- | --- |
| **Prototype** (2009) | Titanium | 🏆 Connected the headset to the head turn; tested without the game. | 10-14 | [prototype-vr](https://github.com/TefMeister/prototype-vr) |
| **Mad Max** (2015) | Apex Engine | 🔧 Worked on driving with your head turned: the ground no longer goes missing on small turns. | 10-15 | [mad-max-vr](https://github.com/TefMeister/mad-max-vr) |
| **Enslaved: Odyssey to the West** | Unreal Engine 3 | 🔧 Tidied the head-tilt log so it shows the game's real camera angle. | 10-15 | [enslaved-vr](https://github.com/TefMeister/enslaved-vr) |
| **Prince of Persia** (2008) | Scimitar | 🔧 Found where the follow camera sets its distance and height. | 11-01 | [prince-of-persia-2008-vr](https://github.com/TefMeister/prince-of-persia-2008-vr) |
| **Heavy Rain** (2010) | Quantic Dream engine | ⭐ Built the code that sends the game's picture to the headset. | 10-29 | [heavy-rain-vr](https://github.com/TefMeister/heavy-rain-vr) |
| **Bulletstorm: Full Clip Edition** (2011) | Unreal Engine 3 | 🔍 Worked on sending the picture to a headset, each eye with its own view. | 10-16 | [bulletstorm-vr](https://github.com/TefMeister/bulletstorm-vr) |
| **Visceral — RE4 VR** | RE Engine | 🔍 Restarted from scratch as our own VR mod, planned around both eyes drawn in one frame. | 11-04 | [visceral-re4-vr](https://github.com/TefMeister/visceral-re4-vr) |

### ⏸ Paused

| Game | Engine | Where it stands | Updated | Repo |
| --- | --- | --- | --- | --- |
| **XIII** (2003) | Unreal Engine 2 | ⏸ Paused for now. | 11-04 | [XIII2003-vr](https://github.com/TefMeister/XIII2003-vr) |
| **Brutal Doom** (Doom 1 and 2) | GZDoom | ⏸ Paused for now. | 11-04 | [brutal-doom-3d-guns](https://github.com/TefMeister/brutal-doom-3d-guns) |
| **The Witcher 2** (2011) | REDengine | ⏸ Paused for now. | 11-04 | [witcher-2-vr](https://github.com/TefMeister/witcher-2-vr) |
| **Metro Exodus** (2019, and the Enhanced Edition) | 4A Engine | ⏸ Paused for now. | 11-04 | [metro-exodus-vr](https://github.com/TefMeister/metro-exodus-vr) |
| **Tomb Raider** (2013) | Foundation | ⏸ Paused for now. | 11-04 | [tomb-raider-2013-vr](https://github.com/TefMeister/tomb-raider-2013-vr) |
| **Death Stranding Director's Cut** (2022) | Decima | ⏸ Paused for now. | 11-04 | [death-stranding-vr](https://github.com/TefMeister/death-stranding-vr) |
| **Burnout Paradise** (Remastered) | Criterion engine | ⏸ Paused for now. | 11-04 | [burnout-paradise-vr](https://github.com/TefMeister/burnout-paradise-vr) |
| **Unreal Gold** (1998) | Unreal Engine 1 | ⏸ Paused: a VR mod already exists (Unreal Revived) | 09-26 | [unreal-gold-vr](https://github.com/TefMeister/unreal-gold-vr) |
| **Far Cry 2** (2008) | Dunia | ⏸ Paused: another Far Cry 2 VR mod is in the works | 09-26 | [far-cry-2-vr](https://github.com/TefMeister/far-cry-2-vr) |
| **Dead Space 2** (2011) | RenderWare-based | ⏸ Paused: chortdev is making a Dead Space trilogy VR mod | 09-26 | [dead-space-2-vr](https://github.com/TefMeister/dead-space-2-vr) |
| **DOOM** (2016) | id Tech 6 | ⏸ Paused: a DOOM VR mod already exists (KHARVOX) | 09-26 | [doom-2016-vr](https://github.com/TefMeister/doom-2016-vr) |
| **Portal** (2007) | Source | ⏸ Paused: a Portal VR mod already exists (BowmanFox's portal1vr) | 09-26 | [portal-vr](https://github.com/TefMeister/portal-vr) |
| **Prey** (2017) | CryEngine | ⏸ Paused: fholger is making a Prey VR mod | 09-26 | [prey-2017-vr](https://github.com/TefMeister/prey-2017-vr) |
| **Manhunt** (2003) | RenderWare | ⏸ Paused: someone else is making a Manhunt VR mod | 11-02 | [manhunt-2003-vr](https://github.com/TefMeister/manhunt-2003-vr) |
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

| Plugin | What it does | Where it stands | Updated | Repo |
| --- | --- | --- | --- | --- |
| **Lanes** | A collection of tools for flat-to-VR AI modding with Claude: skills, helper programs and checks for Claude Code that take a flat-screen PC game into VR, from the first look inside the game to the build you wear in the headset. Optional and modular as much as possible, and it ships with a rule to not say "You're right!" :) | 🔧 Two PCs with separate jobs: one builds, the Keeper uploads and keeps GitHub tidy, and can now open its own window on the building PC. A PC switches off only once every session there has finished and saved, and the weekly full scan proves what it changed. Latest release [0.113.4](https://github.com/TefMeister/lanes-plugin/releases/tag/v0.113.4). | 11-12 | [lanes-plugin](https://github.com/TefMeister/lanes-plugin) |

## 🧊 Blender

Pixel-style cube models for games, built in Blender by script.

| Tool | What it does | Where it stands | Updated | Repo |
| --- | --- | --- | --- | --- |
| **blender-cubekit** | A framework for making game models out of little cubes, like pixel art with depth: one cube size for everything, every number named, no lights, stop-motion animation, straight into the game. Comes with a Blender add-on (buttons and keys) and the write-ups on how it is done. The game models made with it stay in their own projects. | 🔧 Lines drawn on a model (grooves, cracks, scratches, raised lines) no longer come out dotted; a one-zip download, no Lanes needed. | 11-10 | [blender-cubekit](https://github.com/TefMeister/blender-cubekit) |

## <img src="https://raw.githubusercontent.com/TefMeister/terminal-themes/main/icons/flower-icon.png" alt="" height="28" align="top"> Terminal Themes

Give your session a fresh look with one of these custom themes.

<img src="https://raw.githubusercontent.com/TefMeister/terminal-themes/main/preview/green-monitor-lanes.png" alt="The green monitor theme with the Lanes banner" width="480">

| Theme | What it looks like | Where it stands | Updated | Repo |
| --- | --- | --- | --- | --- |
| **Green monitor, Lanes banner** | The same old green screen, with the Lanes Plugin banner behind the text in one dim, striped green, so the letters stay easy to read. The look the Lanes plugin ships with. | 🔧 A still version added: same look, no rolling light, lighter on the PC. | 11-01 | [terminal-themes](https://github.com/TefMeister/terminal-themes) |
| **Green monitor, starburst flower** | An old green computer screen for Windows Terminal: sharp glowing letters, dark corners, and a faint striped flower behind the text, its petals placed like the rays of the Claude logo, with a light that slowly runs down the screen. | 🔧 A still version added: same look, no movement, so the terminal stops redrawing every frame. | 10-31 | [terminal-themes](https://github.com/TefMeister/terminal-themes) |
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
| **Ghost Hand BeG0nE** | In VR, the gaps between your real hand and the player's hand: lag, offset, jumps and lost tracking that make hand gestures like racking a slide miss. It records both controllers and the game's hands, then points at where they part. | 🔧 In daily use: the recorder and its report maker ship in Lanes, and the background rider has filed over 400 reports. | 11-07 | [BeG0nE](https://github.com/TefMeister/BeG0nE/tree/main/ghost-hand) |
| **Flickers BeG0nE** | In VR, parts of the picture flashing wrong for a single frame, like the grass in Resident Evil 4 with REFramework. It catches the flash and shows what it is, then shows the frame before in its place. | 🔧 Built the catcher and its reader as one REFramework plugin file; it found every fake flicker on the headset simulator. | 10-26 | [BeG0nE](https://github.com/TefMeister/BeG0nE/tree/main/flickers) |
| **Eye Difference BeG0nE** | In VR, anything that differs between the left and the right eye: plants or objects drawn in one eye only, one eye darker or tinted, one eye more jagged, the eyes out of line. It reads the Flickers catcher's pictures, takes out the normal 3D shift between the eyes, and says what is left, which eye has it and where. | 🔧 Built and tested on made-up eye pictures; first real job: Resident Evil 4's plants seen in one eye only. | 11-02 | [BeG0nE](https://github.com/TefMeister/BeG0nE/tree/main/eye-difference) |

## ❄️ VR helpers

Small programs that make working in a headset easier, for any game.

| Tool | How it works | Where it stands | Updated | Where it lives |
| --- | --- | --- | --- | --- |
| **Hand Freeze** | A desktop app that holds the VR controllers still in any OpenXR game, left, right or both. Press the snowflake, hold the controllers where the hands should be, and after a countdown they stay put while the game keeps running, so hand poses can be tuned with the mouse. | 🔧 v4: a click of the right thumbstick freezes or frees both hands, and the game never sees that click. | 10-25 | [hand-freeze-vr](https://github.com/TefMeister/hand-freeze-vr) |
| **VR Bench** | A robot player for VR games. With the OpenXR Simulator as the headset, it moves the head, both hands and every button by itself, takes a picture after each, and writes down what the game did, so VR work can be tested with nobody wearing anything. | 🔧 Takes pictures from the newest OpenXR Simulator again, and never starts a game beside a copy still closing (in Lanes 0.106.3); drives Tale of Two Wastelands VR's buttons through the 32-bit layer. | 11-10 | [vr-bench](https://github.com/TefMeister/vr-bench) |
| **Window View** | A desktop app plus an OpenXR layer that hangs any open window in front of your eyes inside the game, like an in-game menu that turns with your head. Add as many as you like, set how see-through each is, drag them by their header, resize them by their corner. Page Up hands your mouse and keyboard to the floating windows (the game sees nothing and is played with the controllers); Page Down hands them back. | 🔧 1.11 built and tested on the pretend headset: typing into a Claude Code window you clicked in VR goes to that window; A is a left click and the right stick works the helper windows' sliders. Download out (v1.11). | 11-12 | [window-view-vr](https://github.com/TefMeister/window-view-vr) |
| **Hand Poser** | A compact window of sliders that poses the player's hands in RE Engine games: add any bone, turn it, see which bones move with it, undo, redo, and keep named pose builds. Meant to hang inside the headset through Window View while Hand Freeze holds the controllers. Inspired by alphaZomega's EMV Engine poser. | 🔧 0.4 built, 30 self-checks pass: ready and free poses for the hands, a pose per gun for each zone of both hands, and spots on the gun (slide, magazine, bolt). Used daily in Village in the headset; download out (v0.4). | 11-12 | [hand-poser-vr](https://github.com/TefMeister/hand-poser-vr) |
| **Animation & Timing** | Hand Poser's sister for things that move: freeze the player's animation, step it a frame at a time, slow it down, and turn any joint on top of it with keys that fade into each other; with Visceral RE8 it also holds the mod's finger movements on a frame, adds or removes frames, moves the whole hand on the gun, and tunes the mod's named timings live. Inspired by alphaZomega's EMV Engine. | 🔧 The new controller buttons (right stick steps, Y undo, B redo, X untick); one picture at the back instead of two, and it finds the hands' joints on the body when the player has none. Tests pass, not yet tried in the game. | 11-09 | [animation-timing-vr](https://github.com/TefMeister/animation-timing-vr) |
| **Grip Zones** | A small window of sliders that moves and resizes every place the hand can grip a gun in VR: the magazine, the well, the slide, pump or bolt, the front grip. Each zone moves on the gun in the game at once, for one gun or all. Hangs inside the headset through Window View. Works with Visceral RE8 for now; more games as we mod them. | 🔧 1.5 built, 12 self-checks pass: the controller buttons step only the helper window clicked last (it wears a yellow strip), the same buttons in every helper. Download out (v1.5). | 11-12 | [grip-zones-vr](https://github.com/TefMeister/grip-zones-vr) |
| **Gun Poser** | A small window of sliders that aims and moves the gun in the right hand in VR: up or down, left or right, roll, and forward, up or sideways in the hand, for one gun or all. Hangs inside the headset through Window View. Works with Visceral RE8 for now; the idea is to make it work across many games. | 🔧 The new controller buttons (right stick steps, X untick); installed. | 11-09 | [gun-poser-vr](https://github.com/TefMeister/gun-poser-vr) |

## 🤖 Automated navigation and movement

Tools that let a game get itself from launch to gameplay, so testing a mod does not start with the same menus
by hand every time.

| Tool | How it works | Where it stands | Updated | Where it lives |
| --- | --- | --- | --- | --- |
| **Menu‑o‑matiC** | Records the way through a game's menus once, as key presses plus small screen checkpoints, then replays it by itself. A replay looks at nothing: each checkpoint is a small patch of the screen compared by numbers. Only when something unexpected appears does it save a small picture for someone to look at. Plain Python, usable by anyone; also the `/lanes:menu` command in the Lanes plugin. | 🔧 Can be held to the game's own program, so a chat window with the game's name in its title never gets a key or a picture again; a game's notes file always lands in its routes folder, and a launch waits for a copy still closing. | 11-10 | [flat-to-vr-RE-toolkit](https://github.com/TefMeister/flat-to-vr-RE-toolkit/tree/main/tools/menu-o-matic) |
| **Move‑o‑matiC** | Moves a character or car along a route. The player drives or walks it once while every key and how long it was held is recorded, and marks where to check it arrived; after that it repeats the route by itself. Each game is first set up together with the player: save point, menu buttons, controls, and a check that inputs reach the game. | 🔧 Uses Menu-o-matiC's busy-keys check, so a walk or a turn never presses into another session's game, and takes the game's program the same way, so it never walks another window. | 11-10 | [flat-to-vr-RE-toolkit](https://github.com/TefMeister/flat-to-vr-RE-toolkit/tree/main/tools/menu-o-matic) |
| **State‑o‑matiC** | Tells whether a game is in a menu, loading, a cutscene, or gameplay, from signs that work outside almost any game: black bars, how much of the picture moves, a lone spinning icon, how hard the game reads its disk, and whether the picture answers a key. Screens that fool it are shown to it once during setup. | 🔧 Says "minimised" instead of failing, finds a game's taught screens by itself, calls a game that stops answering frozen, and can be held to the game's own program. | 11-10 | [flat-to-vr-RE-toolkit](https://github.com/TefMeister/flat-to-vr-RE-toolkit/tree/main/tools/menu-o-matic) |

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
open an issue on the repo (each repo's `CONTRIBUTING.md` says how).*
