# 📰 Recent Activity

[← Back to the front page](README.md)

A short, dated line for every working session, newest first. It includes the days when nothing
advanced, because dead ends and corrections are part of how this work really goes. For the full
story of any project, open its repo and read `modding-notes/`.

**Key:** 🏆 breakthrough · ⭐ promising find · 🎮 hands-on test · 🔄 correction · ⚠️ something went
wrong · 🔧 tooling · 📋 housekeeping

---

## 2026-09-18

### The Darkness: a hidden developer menu, and an alarm bell that was killing every test

⭐ The Darkness ships with a **built-in developer menu** - a free-flying camera, walk-through-walls,
god mode, and a page of jump-straight-to-any-level buttons. All of it is sitting in the retail game
files, untouched since 2007. A free camera is close to the most useful thing this project could be
handed, because moving a camera independently of the player is exactly what a headset needs.

⚠ It did not open. Every way in is behind a single locked door in the game's own code, and the two
switches that looked like the key turned out not to be. Finding out what that door actually checks
is now the most valuable question on the project.

🔧 Separately, a setting that should drop the game straight into a level - skipping ninety
seconds of logos and menus on every single test - was killing the game instantly, with nothing
written down anywhere to say why. Under a debugger it turned out the game was hitting one of its own
internal alarm bells, a leftover from when it was being developed. On the real Xbox that alarm is
ignored and the game carries on; our version was treating it as fatal. Fixed, so it behaves like the
console did.

Past that, the game asks for a lettering file that is nowhere on the disc - even though the menus
draw text perfectly well - so the shortcut still does not land in a level. But the game's own menu
turned out to have a **checkpoint selector** all along, which needs nothing fixed at all. That is the
way in, and it was there the whole time.

Later the same session the picture got sharper still. That locked door turns out not to be locked
at all - it is **empty**. The check the game runs before opening its developer menu does nothing
whatsoever; it was left as a hollow shell when the game shipped. That is oddly good news: it means
no setting will ever open it, and one small, precisely aimed change to our own build will open all
of it at once - free camera, walk-through-walls, level jumps.

The missing lettering file was found too, packed inside one of the game's own archive files. And
the disc copy was checked against the original, file by file: 498 files, not one missing, not one
the wrong size. The rip was never the problem.

One prediction was wrong and is written down as wrong: a second way of skipping to the menu was
expected to dodge the lettering problem, and it failed in exactly the same place.

Nothing moved on the stereo picture itself. That remains the very next job.


### A measurement that reads zero, and why that was not an answer

⭐ The scope picture flickers in the headset — the wearer counted about a dozen in two minutes — and
the tool built to measure it reported, across 23,400 frames, exactly nothing. Reading the code found
no fault for the third time.

The real problem turned out to be the reading itself. "Zero" was being produced by two completely
different faults that look identical: the measurement never arriving back from the graphics card, and
the measurement arriving correctly and genuinely being zero. The first is a plumbing mistake in our
code; the second would mean the scope picture is not changing between frames at all, which is a much
stranger and more interesting problem. No amount of staring at the code separates those.

So now the tool fills the result slot with an impossible value before asking the graphics card to
write the real one. If that impossible value is still sitting there afterwards, the answer never
arrived. If it has gone and the answer really is zero, the answer really is zero. One start of the
game now settles which — where before it settled nothing.

⚠️ Worth recording honestly: the new switch was built, tested and installed with no way to actually
switch it on — half a change had been applied and everything downstream still looked healthy. It was
spotted by hand, which is luck rather than process, so there is now an automatic check that every
switch of this kind is wired end to end. It immediately proved it catches exactly that mistake.

### Ethan's clothing in the scope: why it cannot simply be masked out

⭐ The loudest complaint from the last headset night was that Ethan's own clothing keeps getting in
the way of the sniper picture. The obvious wish is to leave him out of the scope view only — visible
to the player, absent from the glass. Reading the game's own renderer today showed **that is not
something this engine can be asked for**: every switch it offers for "draw this or not" is about
shadows and reflections of the whole world, and the scope picture is produced by a mirror that has no
settings at all. There is no way to say "everywhere except in there".

So the answer is timing instead. The game turns out to keep its own flag for *the sniper scope is
raised*, and it can be told to stop drawing the body, piece by piece. Put together, the body goes
away for exactly as long as you are looking down the scope and comes back the moment you lower it —
better than the existing option in the VR menu, which hides the body for the whole session and
forgets the setting every time the game starts.

It is written, it passes its own checks, and it is installed — but it has not been run once, and one
thing is still a genuine gamble: whether the mirror obeys "do not draw this" at all. A single
flat-screen start answers that.

⚠️ Three smaller problems turned up on the way and were fixed: this PC was quietly a whole step
behind the other one and nobody had noticed, one self-check had the *other* computer's folder written
into it so it had never once run here, and two more looked broken when they were fine all along.

### The development PC can now test VR without a headset

🔧 The dev machine here has no headset, so anything involving two eyes has always had to wait for
the other PC. That changed today. A desktop OpenXR runtime — originally by **fholger**, extended by
**elliotttate** and then by **webhead2oo9** — pretends to be a headset and draws both eye views into
an ordinary window, reproducing the measured lens shape, panel resolution and eye separation of ten
real headsets. So a stereo error that only shows up on one particular headset can now be reproduced
at a desk.

Alongside it we wrote `openxr-probe`, a one-command check that opens a real VR session, submits
thirty genuine frames and answers with nothing but an exit code. Its first run: two stereo views at
1280×1400 an eye, correctly asymmetric and mirrored field of view, 64.0 mm between the eyes, 16.6 ms
a frame — pass. The idea of making a probe's answer an exit code is webhead2oo9's, from the probe he
wrote for BetterVR; ours is a fresh implementation of the same idea in Python, and he is credited in
the toolkit's `CREDITS.md`.

The honest limit: this covers VR output that goes through OpenXR. A mod that builds its own stereo
inside the game's renderer still needs a real headset. Which is the main reason the plan from here
is to target OpenXR for new work.

### RE Village scope — the change that broke the sky is fixed, and it was two right ideas in the wrong order

🔄 A change made two days ago demoted the scope picture to a lower-quality source every single
time the scope was set up — which is what turned the sky black and the colours golden in the
headset test the night before. The cause turned out to be small and a little embarrassing: the
code already knew how to tell a genuine problem from an ordinary start-up, six lines further
down. The rescue simply ran first and threw the good picture away before that check could speak.

Two right pieces of code in the wrong order. It is fixed, and given a test that was itself proved
able to fail before it was trusted. Found on the way: a fix confirmed in the headset the day
before had only ever been typed into the home PC's settings by hand, so the development PC was
still running without it. It is baked into the mod now, which is where a confirmed fix belongs.

### Lanes plugin — the setup walk-through learns to look before it asks
- 🔧 **The dev PC's toolbox went from 14 to 20 of 22 tools**, adding a decompiler that reads a game's
  code with nothing running, a link into Blender for building 3D props, and a syntax checker for game
  script files.
- ⚠️ **The tool that reports what is missing was wrong about two things, in the same way:** it tested
  one fixed folder and called anything installed elsewhere absent. 7-Zip was on another drive; SteamVR
  was installed all along, in a Steam library the check never looked in. A false "missing" is worse
  than no check, because it sends setup off to reinstall what the machine already has.
- 🔄 **Fixed, and then widened by Tefa's own suggestion:** a setup walk-through should find out what
  already works before asking anyone to do anything. It now asks Blender directly whether the link
  answers, and says so instead of walking a returning user through steps they finished long ago.

### Silent Hill 2 (2024 remake) — new project
- ⭐ **A new game joins the list, and it is not like the others: it runs on Unreal Engine 5.** Every
  other game here uses an engine that has to be taken apart from scratch before a headset sees
  anything. Unreal has a general-purpose VR tool already — praydog's UEVR — which understands how
  Unreal hands out cameras and pictures. So the part that usually takes months may be the *starting
  point* here.
- 📋 **The repo is open, and honest about being empty.** Nothing has been built, and the game has
  never been launched for this project. The notes deliberately contain no confirmed findings at all,
  and say so at the top, so nobody later mistakes a plan for a result.
- 🔎 **First job needs no game running:** read the two VR profiles other people have already published
  for this game, and write down what each of them had to *discover* — then build our own that needs
  none of their files installed. That last part is what makes it something we can share.
- ⚠️ **One suggested shortcut is parked until it is checked.** A modified version of UEVR was proposed
  as the foundation; nothing is known about it here, so the plan stands on plain UEVR until somebody
  has actually looked. Whether the game's copy protection interferes is also unchecked.
- 🎯 **What it is meant to become:** a harder, quieter *Silent Hill 2* in a headset — fewer enemies
  that can really kill you, no radio warning you they are coming, and everything you carry hanging off
  your body instead of sitting in a menu, with the torch stowed above your head so putting it away
  still lights the fog.

### Housekeeping
- 📋 **Three ideas typed in from a phone were filed**, two of them the Silent Hill 2 ones above. The
  third asked whether several games can be worked on at once from different stores — the answer is
  mostly yes already, and the real limit turns out to be which window is on top, not how fast the PC
  is.

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
- 🔭 **Different zoom for each scope needs the mod to know which scope is fitted**, and the game files do
  not say: both scopes share one rifle model. The mod now writes a short fingerprint of the rifle to its
  log each time the scope picture attaches, so one quick look with each scope will tell them apart.
- 📍 **The invisible object that carries the scope's mirror was parked over a metre from the rifle.** A
  check on the mod's own maths showed two of its three offsets cannot affect the picture at all, so the
  set-up now pulls it in to the rifle, and one height knob is left to try against the branches and
  clothing that show up in the scope.
- 🎯 **Bullets straying from the crosshair when scoped:** the game's files do not name the spread value, so
  the mod can now list, on one command, every setting the game itself calls spread, recoil or accuracy,
  with the rifle's live numbers. Two runs, aiming and not aiming, should point at the one to pin.
- 👀 **The slight shake in the scope picture has a likely cause and a switch to try.** The headset draws
  from the left eye one frame and the right eye the next, and the mirror's viewpoint hops with it, so a
  picture aimed in a fixed direction lands on a slightly different spot every frame. The mod can now aim
  at the point the rifle is pointing at instead, from whichever eye drew the frame. Off until tested.
- 🧭 **Why the scope picture needed a half-turn is now understood:** the rifle's own sideways axis points
  the opposite way from what the maths assumed, and the glass shows the picture upside down by itself.
  The two together are exactly the half-turn the wearer picked. The mod can now build that orientation
  directly, so its warning about a mirrored picture means something again. One look confirms it.
- ✋ **One hand hiding the other controller:** the VR menu's own hand-position slider most likely never
  reaches the hands, so the mod now has a one-line command that sets how much higher you hold a
  controller than its hand is drawn. Waiting for a headset test.
- 🧾 **Board tidy-up:** the last no-game item, a rifle with no scope until you buy one from the Duke, turns
  out to hinge on one question the new rifle fingerprint already answers in the game, so it now waits
  for that test. Nothing on RE Village is left to do without the game on this PC.

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
- 🏆 **Our own build of The Darkness now runs — later the same day.** It started as a skeleton that crashed instantly, looking for one missing piece of its own code after another. Rather than hunt them one crash at a time, a helper worked out *why*: the game was built without the internal labels the toolkit relies on to find that code. It then found 235 of the missing pieces in one pass — one of them predicted before a crash independently confirmed it. After that the game played its intro logos, reached **The Darkness** title screen, and carried on into the opening sequence.
- ⚠️ **Not claiming more than that.** A character name card appeared, but the game’s trailer also plays automatically when left idle at the menu, so it is not yet certain the 3D engine is drawing. The helper found a built-in switch that jumps straight into the first level, which will settle it.
- 🔧 **Tested hands-off while Tefa worked on the same PC**, photographing only the game’s own window so their work was never interrupted. One run ended with focus on a different window and it could not be told why, so no further runs were made — Tefa’s other program drives a real engraving machine.
- 🔄 **The 3D test, and an honest no.** What looked like the game’s 3D engine drawing a character turned out to be the game’s own trailer, which plays by itself when the menu is left idle. Detailed logging proved it: the trailer file opened at the exact moment the character appeared, and no level was ever loaded. A built-in shortcut straight into the first level does work, but trips an internal safety check a second later. Two likely causes were tested and ruled out. **Next:** start a game from the menu, or find what that check wants.
- 🏆 **And then it worked — the same evening.** A virtual game controller pressed Start and A through the menus, and The Darkness loaded its first level in our own build. It is real, live 3D: first-person, Jackie’s hands in the back of the car, the “Use to look around” prompt, then the whole opening car chase through the tunnel with the lights sweeping past. That is the point where VR work can begin, and the game being first-person is exactly what VR wants.
- ⚠️ **One thing not yet proven:** that pushing the look stick turns the camera. The first try was muddled by the car moving on its own; it needs a quicker before-and-after comparison.
- 🏆 **Proven that night: the look stick turns the camera.** Pictures taken a split second either side of each nudge, with do-nothing checks in between, showed the view swinging left when pushed right, right when pushed left, and up when pushed up — and not moving at all when nothing was pressed. The first attempt wrongly said it didn’t work: the on-screen “Use to look around” text never moves, and it fooled the measurement. **Every flat-screen step before VR is now done** — in a headset, your head does that looking.

  ![The Darkness opening car chase, rendered live in our own build](https://raw.githubusercontent.com/TefMeister/the-darkness-vr/main/dev-archive/milestone-captures/2026-09-16-first-3d-car-tunnel.png)
- ⭐ **Found the two places VR plugs in.** Reading the toolkit’s code turned up one spot where every finished frame passes on its way to the screen — where frames can go to a headset instead — and a second, earlier spot where the game sets up its camera. **Both are needed, and that is the part that is easy to get wrong:** a frame at the first spot is already a flat picture, so sending it to both eyes gives no depth. Real 3D needs each eye drawn from a slightly different position, which is what the second spot allows. Neither place has any VR code in it yet. The same code runs every Xbox 360 port on this toolkit, so this also answers the question for Condemned 2.
- ⭐ **Found the exact spot for each eye’s camera.** The game works out how to squash its 3D world onto the flat screen in one place, a few times per frame, separately from where each object sits. Nudging that single calculation sideways moves the whole view for one eye — and leaves menus and the HUD alone. It was worked out by reading the translated game code and checked by recreating the maths, not yet by running it. Along the way: an out-of-date graphics file had been quietly running all day and was replaced, and the game’s controller turned out to stop listening whenever another window is in front.

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
