# 📰 Recent Activity

[← Back to the front page](README.md)

A short, dated line for every working session, newest first. It includes the days when nothing
advanced, because dead ends and corrections are part of how this work really goes. For the full
story of any project, open its repo and read `modding-notes/`.

**Key:** 🏆 breakthrough · ⭐ promising find · 🎮 hands-on test · 🔄 correction · ⚠️ something went
wrong · 🔧 tooling · 📋 housekeeping

---

## 2026-09-16

### RE Village — VR scope
- 🔎 **The one-frame flicker, read from the code (no game running).** Tefa's frame-by-frame video was
  looked at again: for that one frame the scope shows a *different picture*, not the same one with the
  rifle in it. The plugin's high-range picture comes from a buffer the engine hands out from a shared
  pool, and that kind of buffer has shown nothing at all before — the leading suspect is that another
  part of the renderer sometimes draws into it. Three switches were built to prove or disprove it in one
  headset session: a change detector that logs every such frame, a "show the last good frame again"
  guard, and a switch to the picture buffer that is ours alone. All off by default, nothing run yet.
- 🔧 **The dev PC now carries the home PC's build**, and a descriptor file that only existed in one game
  folder is now in the repo.
- 🔁 **The "security camera" after a save reload has a fix waiting for a test.** The picture stayed behind
  because the scope kept reading a buffer the new rig no longer drew into; it now drops back to the one
  that follows the rig, and one word (`rerig`) rebuilds the scope after a reload.
- ⏱️ **The one-second flash of the plain lens when switching away from the rifle** now has a switch to
  try: the scope waits until the rifle is actually put away before handing the lens back. Off until tested.

### Condemned 2: Bloodshot (new project)
- 🏆 **A 2008 Xbox 360 game is now running on the dev PC, on hardware the official PC build
  refuses to start on.** A newly-bought second-hand DVD drive was flashed with the firmware that lets
  a PC read Xbox 360 discs, the disc was copied with zero read errors, and the game files extracted.
  The published PC recompilation then failed with a Windows message that blames a missing file and
  means nothing of the sort — the real cause was that the release needs a processor feature from 2013
  and this machine is from 2012.
- ⭐ **Rebuilt from source instead, and it works.** Built the project the way its own settings ask
  for, the dependence on that 2013 feature drops from 6,214 uses to 39, and the 39 left are never
  reached. Seven separate obstacles had to be cleared along the way; three of them turned out to be
  genuine gaps in the upstream projects rather than local problems, and are written up to be sent back.
- 🔄 **Correction:** this session told Tefa to install Microsoft's compiler as an administrator.
  They did not need to — it was already on the machine, in a non-default folder that the check
  did not look in.
- 🔍 **Still slow, and now we know why.** Lowering every graphics setting barely helped, which
  confirms the old processor, not the graphics card, is the limit. No more time will be spent tuning
  graphics on that machine.

### The Darkness (2007) (new project)
- ⭐ **A second Xbox 360 disc copied perfectly, and the game files extracted.** Two promising leads:
  the engine reads plain-text settings (the whole retail config is three lines, so it very likely
  understands many more), and a **debug** configuration file shipped on the retail disc. Both are
  unproven until the game's main program is unpacked — it is compressed and encrypted, which was
  confirmed by a control test rather than assumed.
- 🔄 **Correction:** this session said nobody was recompiling The Darkness. Wrong — a project
  exists and has shown a working build. The search behind that claim returned dark-mode browser
  extensions, and a useless result was read as a negative one. Tefa caught it.

### Housekeeping
- 🔄 **Correction to this page:** Deus Ex: Mankind Divided and Bulletstorm were listed as
  "still downloading". They are not — and neither are the other four of that batch. **All six are
  fully installed on the dev PC**, which also corrects a note claiming none of them were. Tefa spotted
  the wrong lines.

## 2026-09-15

### The lanes plugin (tooling)
- 🔧 **Its last two known bugs are closed (0.6.2).** The counter for "sessions run with the
  background helper" had been counting from a date, so two sessions from the morning *before* the
  helper existed were being counted as helper runs. It now counts from the exact minute the helper
  shipped, and a test proves the earlier ones are left out. The plugin's own test lane also has
  proper instructions for checking that helper live.
- 📋 **Where it stands:** 33 of the 50 clean two-window runs it needs before going public, and the
  helper's own bar (20 runs) is already past. Zero open bugs.

### Mod ideas
- 📋 Nine ideas filed from the phone dump — five for RE2, one each for RE7 and all the RE games, one
  for every game (casings that stay on the floor), and one for the plugin itself: tell newcomers
  which games are already being converted, so nobody does the same one twice.

## 2026-09-14

### RE Village — VR scope
- 🎮 **The scope now puts its picture back on the glass by itself** after a weapon switch. Tested in
  the headset: it comes back almost instantly, no key press needed.
- 🔧 **A tester package was put together**, with one-click start and fix shortcuts and step-by-step
  instructions, so someone else can run the scope exactly as it runs here.
- 📋 **A new to-do list after a real play session:** the zero has drifted slightly, the stock glass
  flashes during a weapon switch, bullet spread on scoped rifles, and a random flicker. Crouched
  aiming was confirmed working.

### Hard Reset
- 🎮 **First launch, with TefMeister at the keyboard.** The developer console works (Ctrl + ~). The
  old 3D switch does *something* on a modern graphics card, which I had just predicted it would not.
  But it looks like a mix-up of the game's images, not two views. A test of whether the game will
  use an edited shader file is set up and waiting for the next start.
- 🔄 **A hope withdrawn the same day, and something better found in its place.** The game's
  built-in "stereo" settings drive NVIDIA's retired 3D Vision, not a VR-style renderer of its own.
  But unlocking the data archives showed the shaders ship as **readable source**, naming the
  camera's matrices outright.
- ⭐ **First look:** eye-separation settings, a real console and an embedded scripting language that
  can run a file off the disk, all in the shipped game.

### Prototype
- 🏆 **The camera is found.** Register `c0`, left-handed, 16:9, near plane 0.3, far 7500, **80.00°**,
  with textbook-standard depth maths.
- 🔄 **A correction to my own claim from four hours earlier.** I had argued from one small shader
  sample that the camera was fused and head tracking would be harder. The live run shows it is not.
  Withdrawn.

### Dead Space 2
- 🏆 **The per-eye maths is derived**, and tested 59 ways. It needs two numbers changed, not one. My
  first attempt used one, and the test caught it straight away.
- 🏆 **The camera is found.** Register `c4`, left-handed, exactly 16:9, X axis mirrored. It was
  picked out from two rivals because it was the only one that moved during a zoom.
- 🏆 **A way into the game, proven.** An earlier start-up crash is explained: the game asked for a
  graphics function our file did not provide. The theory that the copy protection was rejecting us
  is **disproved**.
- ⚠️ **An instrument that could never have worked.** Something else, almost certainly the Steam
  overlay, held the spot it needed, so a whole playthrough was logged for nothing. Fixed.
- 🔄 **Engine lineage corrected** to RenderWare, the same framework as Manhunt on this account.

### Tomb Raider (2013)
- ⭐ **117 shaders live inside the executable with their descriptions intact**, so the camera is
  readable with nothing running. One of them is a per-eye `StereoOffset`, left over from the 3D-TV
  era.

### The Witcher 2
- ⭐ **A debug console, a debug menu and a free camera** are all in the shipped game, and its memory
  addresses stay put between runs.

### Portal
- ⭐ **Valve's own VR mode still ships**: 36 VR settings, head-relative aiming, the HUD in the world,
  and the VR toggle in the menu. Exactly one file is missing: the part that talks to the headset.

### Across the account
- 🔍 **A hidden bug flagged in three other projects.** Psychonauts, Alan Wake and Prince of Persia
  use the same risky file shape that broke Dead Space 2. They work today only because those games
  don't ask for the missing part.
- 🔧 **The front page is now checked by a tool**, which warns when this list falls behind the work.
  The tool immediately caught a bug in its own test.
- 📋 **This page was split off the front page**, so the front page stays a quick look at where each
  mod stands.
- 📋 **Six install checks.** Four games were already on the development PC. The Witcher 2 and Tomb
  Raider were downloaded the same day.

---

## 2026-09-13

- 📦 **Four early releases, all clearly labelled as unfinished:** XIII `v0.3.0-alpha`, Far Cry 2
  `v0.2.0-alpha`, Psychonauts `v0.1.8-alpha` and Unreal Gold's first `v0.1.0-alpha`. Each release
  note lists what does *not* work first.
- 🎮 **RE Village: the scope is zeroed** in the headset, and TefMeister confirmed the values are
  accurate.
- 🔄 **Alice: Madness Returns: we were chasing the wrong matrix.** The sliding shadows are better
  explained by a shadow matrix built from the game's unedited camera.
- 🆕 **Three new projects started:** Hard Reset, Death Stranding and Metro Exodus.

## 2026-09-12

- 🔧 **DOOM (2016): the arrow keys are fixed.** Windows itself reports those keys the wrong way, which
  is how the bug got in. The fix has not been run in the game yet.

## 2026-09-11

- 🏆 **Manhunt: he walks.** The character moved under automation for the first time. The keys were
  right all along; the way they were being sent was wrong.
- 🔄 **Visceral RE2: the grip bug is fixed, and that morning's diagnosis of it was wrong.** The
  values were never being sent at all.

## 2026-09-10

- 🎮 **Eight games worn back to back in a real headset in one evening**, the first time the whole queue
  was cleared in one sitting. **XIII** showed true stereo in VR for the first time. **Unreal Gold**
  fused, and the world came out life-size. **Alice** got live head tracking. **Far Cry 2** got
  matching stereo and head rotation. **Resident Evil 2** carried head and controller poses across for
  the first time.
- ⚠️ **Two did not go well.** Psychonauts' camera-follow build went badly glitchy within seconds and
  was not shipped. Enslaved could not be worn at all, because the side-by-side output mode doesn't
  exist yet.
- 💡 **The lesson landed twice that evening:** turning the picture *after* the game has already
  decided what to draw leaves nothing behind the player. Head rotation has to reach the game's own
  camera.

A caveat that applies to nearly everything above: most of it is **one person, one machine, often
one launch**. "It fused once" is a much smaller claim than "it is comfortable", and I try not to let
the first quietly become the second.

---

## 🗂️ Older months

Each month stays on this page while it is happening. When a new month starts, the whole of the
previous month moves to its own page, listed here, newest first.

- [August 2026](activity/2026-08.md): the month it all began, with highlights and flops

*September 2026 moves here on 1 October.*
