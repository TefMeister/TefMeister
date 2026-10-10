# 📰 Recent Activity

[← Back to the front page](README.md)

A short, dated line for every working session, newest first. It includes the days when nothing
advanced, because dead ends and corrections are part of how this work really goes. For the full
story of any project, open its repo and read `modding-notes/`.

## 2026-10-10

- 🥽 **Headset checks without wearing it (late evening).** With the Quest connected but not worn, four games were started and measured. Alan Wake and The Evil Within reach the headset; Alan Wake’s 3D still hides Alan and the fog, and The Evil Within runs slowly in its opening cutscene. Hard Reset runs in 3D at about 52 frames a second. XIII’s newest 3D build now starts with the headset.
- 🎮 **Visceral, RE2 VR (evening).** Manual reloads ported from Andyalpa's RELOADED: drop the magazine with B, take a new one from the hip, slide it in; shotgun shells one by one; slide and pump racked by moving the hand. The grenade now comes from the lower back on the right grip, and a swing throws it; Tefa: "feels superb". Saved as BASELINE 3.
- 🎮 **RE Village VR scope (afternoon).** v1.1.5 confirmed in play by Tefa: "finally working as it should in game, this is a huge achievement". The scope is done; v1.1.5 is the version everywhere.
- 🎮 **Visceral, RE3 VR (started).** RE3 got the March REFramework with DLSS ready but off. The first RE2 features are brought over: every weapon now uses the relaxed body pose for Jill and Carlos, plus the hunch fix. Not tried in the headset yet. Later the same evening the whole newest RE2 build was brought over: holsters, running, ladders, menus, two-handed grip, manual reloads and the rest, rebuilt for RE3. The first run showed RE3 was ignoring our settings file, so the poses never loaded; that is fixed. Jill now has the relaxed body; a calmer standing pose is being tried for the forward lean.
- 🎮 **Visceral, RE2 VR (afternoon).** Every menu now sits over the live game world: the inventory, map and item box lost their colour filter, the pause menu its blur and dark overlay. Tefa on the monitor: "looks great!" Pick-ups still hide the world; that is the next job. Music muted on every launch.
- 🧩 **Lanes 0.54.0 and ideas.** Four ideas that waited overnight were filed (three for RE2, one for Lanes: an uninstall command). From now on an idea mentioned during a session is filed straight away instead of waiting for the next session.
- 🏆 **Visceral, RE2 VR (night).** The two-handed grip works in every state: hold the left grip near any gun and the hand takes it, relaxed, walking, running or aiming, with no change of pose; the grip spot comes from the gun's own support-hand anchor. Tefa: "i can now run and shoot at the same time". Reloading while gripping fixed the same night. Saved as the baseline. The main menu shows the last save's scene with rain again.
- 🎯 **Visceral, RE2 VR (late night).** Bullet spread now depends on stance and hands: running is wide, walking is tighter, and standing with both hands on the gun is dead on. Long guns are a step less accurate than handguns.

## 2026-10-10

- 🎮 **RE Village VR scope (night).** Reloads broke whenever the rifle was raised with the left hand gripping: praydog's hands-up block gesture made Ethan guard, which cancelled the reload. Five probe rounds to find the switch the game itself honours; now blocking is off while reloading or with two hands on a gun. The left hand also follows the reload animation. Tefa: *"it works!! ... played perfectly"*. Saved as v1.1.5.

## 2026-10-09

- 🎮 **RE Village VR scope (afternoon).** The lag with the rifle raised is gone: our own code was making the processor wait on the graphics card every frame. The scope picture now waits for both hands to be up, and stops only when the glass is seen nearly edge-on. Tefa: *"the lag is completely gone!"* Then back to v1.1.3 with only the colour fix and the lag fix on top: *"scope is great!"* Saved as v1.1.4.
- 🎨 **Terminal themes.** The newest look, Frequency, added on the home PC as an extra tab.
- 🎮 **Visceral, RE2 VR (afternoon).** Four fixes built, waiting for the headset: the grenade no longer flips in and out while the left grip is held, the black screen at item pick-ups gets a first fix, the holster spots now turn with the player, and Run Hold, auto reload off and aim assist off are set by themselves on the first start.
- 🎮 **Visceral, RE2 VR (night).** Menus: the tilt is gone and the one-frame flash of Leon's body on closing is gone. The inventory still flickers for a frame; DLSS was ruled out. Next: a headset recording picked apart frame by frame.
- 🧩 **Lanes 0.53.0.** A desktop shortcut named Lanes now opens Claude Code in the plugin's look, same font and background. The first session after the look goes on offers it once; so does an update.
- 🎮 **RE Village VR scope.** The outdoor blue tint is solved. The scope's colour dial now pulls blue down on top of the picture, with the sky and fog left in; tuned over three launches to "it's perfect now". Brightness and the VR crosshair-off setting saved with it. Later: the scope's own camera now draws with the lowest picture effects while the game keeps its settings, for a smoother scope, and the DLSS upscaler was switched off after the scope looked DLSS-blurry. Tefa: sharp picture, runs really well; DLSS stays off for Village. Checked whether the scope alone could use low mesh detail: no, this engine picks detail per object, not per camera. The frame drops came only with the rifle out, so the scope's camera now draws only while the rifle is raised to the eye. Worn: it works. The lens also dims when the right hand is away from the headset, and the scope camera only works on every other frame while aiming; tuned with Tefa over several rounds.

## 2026-10-08

- 🧠 **Visceral, RE2 VR (evening).** Read the VR layer's own code and found why menus tilt: it adds the headset's turn on top of a camera that already has it. Also found why the shotgun sits crooked in the light: the two-handed grip reads the relaxed clip's arms. Both fixes built, waiting for the headset.
- 🎮 **RE Village VR scope.** Back to the 1.1.2 scope, plus the one keeper: the scope no longer sees through nearby walls. Built as v1.1.3 and installed; the colour work is set aside. Tefa's observation: the sky went with the layer that removed the blue hue, not with the motion blur. Later the same night: the scope's outdoor colour dial can now pull blue down instead of only adding it, rebuilt on the 1.1.2 plugin and installed at a mild setting.
- ⭐ **Visceral, RE2 VR.** The trigger-only shot works in the headset: one real round per pull. Holding the trigger made the slide keep cycling, so the next build fires once per pull.
- 🎮 **Visceral, RE2 VR.** Built the trigger-only shot: pull the trigger without holding the aim button and the gun fires for real, using the game's own switches. Installed, waiting to be tried in the headset.
- 🎮 **Visceral, RE2 VR.** Wore the menu flicker fix in the headset: the slight tilt on opening and the flicker on closing are both still there. The next idea is that the VR side reads the camera a moment too early.
- 📝 **Session write-ups** got a new look: numbered sections, each with its own colour dot.
- 🎬 **Video recorder (home PC).** Ashes 2063 was recorded on the flat screen: game window only, game sound, 60 fps. The recorder now also says so out loud if a recording never really starts.
- 🧩 **Lanes 0.52.0 and CubeKit 0.18.0** installed on the home PC.
- ⭐ **Far Cry 3: Blood Dragon.** The left/right eye shift was tried in the game and gives real depth. Then built the next step: both eyes shown side by side in the window, each frame filed under the right eye.
- 🎮 **Hard Reset.** Tested the floating screen for menus: the pause menu's words now float at the right distance in both eyes, but its outline frames don't follow yet. That's the next fix.
- ⭐ **Far Cry 3: Blood Dragon.** The left and right eye now see the world from slightly different places, with near things moving more than far ones: real depth, measured in the game. Next is showing both eye pictures side by side.
- 🔧 **Hard Reset.** Read the game's own files: its health and ammo display is a 3D screen on the arm and the gun, so it already works in VR and stays. Only menus and the crosshair will float on a panel.
- 🧩 **CubeKit 0.18.0.** Cubes of different sizes in one model: pick some cubes and make them 8 or 64 times smaller for screws and emblems, then join them back. Tested without opening Blender; bigger sizes are the next step.
- 🧹 **BeG0nE.** Camera Jitter got its ride-along: a mod writes down when it read the headset pose, wrote the camera and sent a picture out, and a rider in the background files each VR session with the cause of any stepping named. Only active while a game is really in VR. A knowledge base keeps one entry per behaviour pattern (no copies), takes Tefa's jittery/smooth label, and rebuilds a findings page naming what separates the two. Controllers are logged on the same line for the Occlusion Drift cure. Lanes 0.52.0 now starts the rider at every session, so it simply rides along. A screen-recording checker built earlier the same day is archived: the flat window never shows VR jitter.
- 🎮 **Hard Reset.** Measured that one game unit is a metre, then switched on head position: leaning and stepping now move the view in the headset simulator. The health dial turned out to be a 3D part of the gun.
- ⭐ **Far Cry 3: Blood Dragon.** Built the step that moves the camera half an eye-width left and right, using Far Cry 2's recipe; it passed a test of about 17,000 checks without the game. One flat run will show it working.
- **Terminal themes:** Frequency, round eight: the big bang now follows the dive into the black hole at once, and the bottle pours into a turning swirl that fills the window.
- 🔍 **Manhunt.** Built the step that makes the game draw its world twice per frame, once per eye, with the same camera for now. It is switched off until a test run turns it on.
- **Terminal themes:** Frequency, round seven: scenes are shorter and roll into each other through long, soft blends, and what pours from the bottle is solid and spread in depth.
- ⭐ **Far Cry 3: Blood Dragon.** Ran the game twice with a logging file and found where it sends the camera: the same slot Far Cry 2 used, and it turns with the mouse. The two-eye step can now be built.
- **Terminal themes:** Frequency, round six: the suburb gained depth (solid shaded houses, shadows, haze), the dive leads into a tube of big bangs, the bottle arcs overhead shrinking to nothing, and glitches became chunky blocks.
- **Terminal themes:** Frequency, round five: one black hole now grows in the middle of the suburb and swallows it, with debris flying in and the colours draining to bleak browns, then a dive into it and a pixelated big bang. Glitch lines are shorter and rarer.
- **Terminal themes:** Frequency, round four: skulls turn after each glitch, chunkier pixel mouths, a slower tunnel, a smoother join after the bottle, a long grey static before the city, and thin glitch lines throughout.
- **Terminal themes:** Frequency, round three: fish glitch between bones and living fish at their own frame rates, the cartoon dog splits into a mirrored pair, black holes swallow three suburbs in turn, and the eyes and mouths are scattered at different depths, each glitching in its own way.
- 🔍 **Far Cry 3: Blood Dragon.** First run on the dev PC. The publisher's launcher signs in by itself, the game plays, and it now runs in a small window with the music off.
- ⭐ **Tomb Raider.** Chose how the VR build will switch on the game's own 3D mode: a small stand-in for NVIDIA's old 3D driver, the trick that already works for Hard Reset. It is built and tested on its own; the game has not been started yet.
- **Terminal themes:** Frequency got a second station: black-hole cubes over a suburb, a bottle pouring letters that turn into earth, eyes, laughing lips and a night city of letters, all slightly wrong. The cubes now glitch in wild colours and the sunrise floor has more detail.
- 🎮 **Psychonauts.** Found a likely reason the head-follow camera went glitchy in the headset: the game may build its next camera on top of our head turn, so the turn keeps adding up. A fix now hands the game its own camera back every frame, and one flat-screen run will show whether that was the cause.
- 🔧 **Enslaved.** Turning and tilting a simulated headset now turns and tilts the game's view, and putting the head back puts the view back. Next is getting the picture into the headset.
- 🧩 **CubeKit** installed in Blender on the dev PC.
- **Terminal themes:** started Frequency, a new look that keeps changing station like a radio dial, from fish bones and skulls to a 1930s cartoon on an old TV and an asteroid field, with random psychedelic glitches. The whole loop plays; tuning comes next.
- 🔧 **Metro Exodus.** The game refuses the usual way of handing its picture to the headset, so a new handover was built with two fallbacks and tested on its own. The next flat run shows which one works.
- 📋 **Weekly check.** One outdated fact (SteamVR now runs older 32-bit games in VR) was still written in three places, and two to-do lists were hidden from the board. Notes left for the owners.
- 🎮 **Ashes 2063.** The cube shotgun does catch the game's real lights, face by face — proven on the flat screen with painted test runs; the earlier "no normals" finding was a misread. A metal shine map gives a faint sheen that moves with the gun. Two headset shortcuts for Tefa to confirm in VR.
- 🎬 **Recording.** The home PC has no E: drive, so its OBS recordings now go to the MEGA transfer folder.
- 🎮 **RE Village — VR scope.** A second night on the scope's colours, Tefa in the headset. The rifle camera's finished picture was smeared by the game's motion blur (now off for that camera) and brightened twice on its way to the glass (fixed). Two things remain: nothing draws the sky for that camera, and its picture lacks the game's haze, so it stays warm and bright. Tefa saw no visible change yet.
- 🎨 **Halloween theme.** Stars are now a handful, scattered across the sky instead of in rows. The chimney smoke takes whichever colour the potion window had when it left, so the puffs match the brew. Tefa called it finished.
- 🎨 **Lanes look.** A new terminal theme: the Lanes banner in dim green behind the text. It is now the look the Lanes plugin ships with (0.51.0), replacing the starburst flower.
- 🧩 **Lanes 0.50.0.** A green tick now tells you when a held test has given enough, so you can lower the controllers.

**Key:** 🏆 breakthrough · ⭐ promising find · 🎮 hands-on test · 🔄 correction · ⚠️ something went
wrong · 🔧 tooling · 📋 housekeeping

---

**2026-10-07** 🏆 **Visceral RE2:** a round fired with no aim stance at all -- three of the game's own switches, flipped for the press only. Next: wire it to the trigger. 🏆 **RE Village scope:** the rifle camera's finished, game-coloured picture was found in VR (a one-frame census of what the game draws); a headset check of the look is next. 🔧 OBS recording fixed on the home PC; Lanes 0.49.0.

## 2026-10-07: Enslaved — our code turns the view

🎮 First run of the turn test: each numpad press turned the picture 15 degrees, it held still, and one key put it back exactly. That is the spot where head movement will go in next. A second build then gives the game its own direction back after each frame, so turning your head should not steer Monkey. Later the same evening, head turning and tilting from a headset was wired in, ready for a simulator test.

## 2026-10-07: Hard Reset — HUD at a set distance

🔧 Hard Reset's health, ammo and text can now float on a flat panel two metres ahead in the headset, instead of covering the whole lens. Tested without the game; it lands exactly where it should. Next: a look in the running game.

## 2026-10-07: Research sweep

⭐ SteamVR now has a 32-bit headset route, which helps Hard Reset and Alan Wake reach the real headset. Metro got a simpler way to send its picture out. The watch list of other people's VR mods is checked.

## 2026-10-07: Burnout Paradise — night on demand

🔧 Found the game's own time-of-day setting, so night is one menu choice away. At night the headlight light on the road now gets our per-eye fix. Judging how it looks needs a steady camera spot.

## 2026-10-07: Bulletstorm — HUD in both eyes

🔧 Bulletstorm's score, ammo and hints now show in both eyes of its side-by-side view; before, only the right eye had them. Next: sending it to a headset.

## 2026-10-07: Hard Reset — head tracking

🏆 In the virtual headset Hard Reset now follows the head: turning, looking up and tilting all work, and the world stays level. Every frame reaches the headset. Next: head movement, then the real headset.

## 2026-10-07: Hard Reset — in the virtual headset

🏆 Hard Reset now plays in the virtual headset with both eyes, the right way round. Next: a faster hand-over, then the real headset at home.

## 2026-10-07: Hard Reset — two eyes on screen

🏆 Hard Reset now shows both eyes side by side in its window, with real depth: far things sit apart, near things close. Two small helper files fool the game's old 3D checks and catch each eye's picture. Next is sending them to a headset.

## 2026-10-07: Hard Reset and Alice

🏆 Hard Reset draws both eyes by itself once a console setting is on, about 120 times a second each, and it compiles our own edited shader files. The eye pictures do not reach the window yet; catching them is next. 🔧 Alice: the shadow fix was re-worked out from the game's own shaders; the live check waits for Tefa on Friday.

## 2026-10-07: Metro Exodus — headset hookup

🔧 The headset bridge from The Evil Within now runs in Metro: a red and blue test picture reaches the virtual headset at 60 fps. It first froze the game, which is fixed. Next is handing over the game's own picture, which needs a different method. 🎮 The runs were recorded with OBS, game and virtual headset in two separate videos.

## 2026-10-07: Lanes 0.47.0 and recording

🔧 Lanes setup now suggests a synced MEGA folder for files that must not go on GitHub, with a reminder that sharing game files is illegal. On the dev PC, OBS now records test footage using the graphics card after a driver update, and a MEGA transfer folder links the two PCs.

## 2026-10-07: Metro Exodus — two eyes

🏆 With DirectX 11 switched on, the game's camera was read live while it ran, and a small mod now moves it half an eye-width left and right on alternate frames. Near things separate more than far ones, as they should. Tefa played to the first save point.

## 2026-10-07: Work-in-progress videos

🔧 Eight short gameplay videos cut from the raw headset recordings: RE2, RE Village and Ashes 2063, each with a title and smooth fades.

## 2026-10-06: Visceral RE2 — running and ladders worn

🎮 Running works perfectly: let go of the stick and Leon stops at once. 🔄 Ladders, switches and cupboards no longer swing the view round; only a tiny flick is left at the start. ⭐ Saved as a keeper build. 🔧 Late on, a frame-by-frame log showed why the inventory flickers; a fix waits to be worn. The main menu rain is back.

## 2026-10-06: Ashes 2063 — the shotgun gets darker and worn

🔧 The cube shotgun's metal is darker, with the shiny top and light rails painted out. It now uses the smaller cubes, with worn edges, a rubbed muzzle, thin scratches and a few rust spots. After a look: darker gloves and a taller silver panel by the shell opening. 🔧 CubeKit 0.14.0 can show the inside of a model again, 0.15.0 picks a whole loose block with one key, and 0.16.0 and 0.17.0 copy, cut and paste cubes onto a chosen side. A shine test showed GZDoom gives a held gun no light information, so real lights on the gun need our own engine build.

## 2026-10-06: Metro Exodus — the original edition runs on the dev PC

🎮 The original 2019 edition runs where the Enhanced one could not: it reaches its menu, plays in a small window with the music off, and loads our file. ⭐ The game's camera was found in its code, and the old VR switches turned out never to draw two eyes.

## 2026-10-06: The Evil Within — head tracking built

🔧 Built head tracking: the headset now turns the picture. The game's own lens is measured from its drawings while it runs, so nothing has to be guessed, and shadows are left alone. 🏆 Then tried in a headset simulator: turning, nodding and tilting the head all move the view the right way in both eyes, and even a big turn to the side shows a fully drawn street.

## 2026-10-06: The Evil Within — the street mystery solved (there was none), two eyes built

🔍 A new recorder showed that every part of the opening street is reached by our camera change, yet the street still looks untouched, so the cause is further down the line than thought. The game can now be walked around by the computer on its own. 🔄 Then Tefa looked in the running game: the street does tilt. It was never broken; I had misread my screenshots. A first two-eye mode was built and then seen working in the game: one frame per eye, with near and far in the right order. 🏆 Late on, the game showed up in both eyes of a headset simulator, with the menus kept flat while the world is 3D. Sharing the game's own graphics device with the headset froze the game, so the headset now gets its own. The real headset is next.

## 2026-10-06: Alan Wake — the dead end was not a dead end

🔄 A month ago we decided our camera changes did nothing on screen. Re-reading the old pictures showed they did; the comparison had been fooled by the camera moving between runs. A new on/off key proved it live: one eye's view now shifts with proper depth. Music is muted. The game measures in metres, so a real eye distance can now be set. Then built the first two-eye mode, one frame per eye, and saw it alternate in the game. Lighting now follows each eye too, with motion blur switched off. Late on, the code was tidied into smaller files and the first headset output was built: a floating 3D screen, one picture per eye. It then worked end to end in a headset simulator; the real headset is next. Head tracking came last, and in a headset simulator turning, nodding and tilting the head all move the view the right way in both eyes. The real headset is next.

## 2026-10-06: Bulletstorm — two eyes in one frame

⭐ The first camera edit works in the game: the view can be slid sideways like a second eye, with near things moving more than far ones and the HUD staying put. The game now runs in a small window with the music off.

🏆 Later the same day: the game now draws two eyes in one frame, side by side, by borrowing its own split-screen mode. Next is the HUD in both eyes.

## 2026-10-06: XIII — the mystery draws were never there

🔄 One keypress in the bank level settled it: nothing is drawn flat on the screen except the HUD, so the twelve "screen-space" draws were a misreading, and the fix for it holds. A second puzzle turned out to be a units slip. Music is now muted, and the game can be quit by keyboard.

## 2026-10-06: Lanes 0.46.0 — builds by feature, originals kept

🔧 Each feature's builds now get their own folder. The game's original files are saved before a mod changes them, so a plain, working game can always be put back.

## 2026-10-06: Visceral RE2 — next jobs lined up

📋 Planned four new jobs: ladder climbing taken over from Arcade Controls, the left hand staying on the gun, quicker stops when running, and no player body showing in menus. Manual reloads wait for the new firing work.

🔧 Rebuilt the ladder and cupboard-push camera fix from Arcade Controls in the new plugin, ready to try in the headset. Each feature's builds now get their own folder.

🔧 Running now stops the moment the stick is let go, or with a second click. Also ready to try.

🔧 The player's body no longer shows in the inventory, map and pause menus. Ready to try.

## 2026-10-05: Visceral RE2 — every gun relaxed

🔧 Leon's relaxed body pose, first made for the pistol, now goes on every gun and its upgrades: magnum, SMG, shotgun, launchers, the flamethrower group, the knife and grenades. Claire and Ada got the same on every weapon. 🎮 Worn: every weapon works, Hunk too; saved as a roll-back build. 🔧 Started a new C++ plugin for the RELOADED features; the four holster spots now take out and put away whatever is in the game's weapon shortcut. Putting grenades there broke the menus, so that was rolled back. Built from the game files alone; not worn yet.

## 2026-10-05: Visceral RE2 — the left hand and the pistol

⭐ The new straight-body animations had lost the game's own switch that keeps Leon's left hand on the gun. A new tool puts that switch back while keeping the straight body; it is in the game, waiting to be worn.

## 2026-10-04: Tidying the game folders

📋 RE Village: the colour work from the test copy now sits in the real game, and the copy is gone. 📋 RE2's old test copy is gone too; its mod files were already saved. 🏆 Visceral RE2: the shake is traced to the upper-body straightener, and with the pistol out Leon now moves exactly like with no gun, straight and smooth. The upgraded Matilda turned out to have its own aiming animations. 🔧 Lanes 0.44.0 and 0.45.0: every session summary is now saved, dated, in its own folder per project, and breakthroughs are marked IMPORTANT.

## 2026-10-04: Research sweep

⭐ Found that a Tomb Raider VR mod switches on the game's own built-in 3D mode with stand-in graphics-driver files, and that Hard Reset could be woken the same way. Two lessons that held in a second game went into the shared library. Silent Hill 2 got its first research page. A second pass covered every game: a public mod maps Death Stranding's camera on our exact version, and Condemned 2's port has a new release with field-of-view and frame-rate settings.

## 2026-10-04: Enslaved — where the camera is decided

⭐ Found the one spot each frame where the game settles where the camera looks, just before it draws. A small numpad test that turns the view from that spot is built and waiting for one launch.

## 2026-10-04: Lanes drops the private game copy

🔧 Lanes 0.43.0: the Mint feature, which modded a private copy of a game instead of the real one, is removed. Modding happens in the game's own folder again. Old copies stay on disk until you decide.

## 2026-10-04: Visceral RE2 — starting over from a clean base

🔄 The working body posture stopped feeling right after a reinstall. RE2 is back on a clean REFramework with DLSS, and it no longer shakes. The working pieces are gathered into one rebuild kit, ready to go back one at a time.

## 2026-10-03: RE Village scope — chasing the outdoor blue

🎮 Indoors the scope's colours are close now, and the 5 cm scope distance is confirmed. Outdoors it stays blue: the game's haze filter was ruled out, and the scope turned out to draw fewer fog volumes than the normal view.

## 2026-10-03: Visceral RE2 — main-menu rain and a step back

🔄 The rain now carries seamlessly between the main menu and the Story page, and the menu no longer goes black after quitting a game. Tonight's posture changes made the walk worse, so the test copy went back to the 25 September package, which moved perfectly.

## 2026-10-03: Visceral RE2 — reload port, step 2

🎮 The mod now has its own sound player for Andyalpa's reload sounds. A first run proved the empty-gun click works in game. The next step, stopping the game's own reload, is drafted.

## 2026-10-03: Lanes 0.42.2

🔧 Session write-ups now show the gate and model box right above the instructions, below the save report.

## 2026-10-03: blender-cubekit — the cube-model framework gets its own repo

🔧 Every cube model in a project now shares one cube size, set in one place. Any single cube can be picked with one key (merged strips are cut back into cubes for editing; the game still gets the lean version). The scripts, a Blender add-on with the buttons and keys, a tutorial and the how-it-works page are in a new public repo. Game models stay out of it. Later the same day, add-ons 0.3.0 and 0.4.0: a picking brush, keys to add and remove cubes, a colour palette, and game-style W A S D movement that is always on. Then 0.5.0: a side can be split into four smaller squares for cracks and wear. Then 0.6.0: a Paint-style palette, with keys 1 to 0 that paint the cube under the mouse. Then 0.7.0: sides split 4 or 16 ways, keeping the fine detail. Then 0.8.0 and 0.9.0: each model can pick a finer cube size, each cube into 8, and go back again; the Ashes shotgun is at 1.7 mm. Then 0.10.0: tidier key help and a Build tab for adding or removing a typed number of cubes. Then 0.11.0: a Move tab for the speeds. Then 0.12.0: a button that counts the cubes between two picked sides. Then 0.13.0: moving picked cubes, and fingers as parts that bend and are posed frame by frame.

## 2026-10-03: RE Village — the game's own colour table on the scope

🔧 The scope picture was still a little too orange next to the world. The missing piece was the colour table the game applies per area after its tone curve; the scope now borrows that same table from the game and applies it too, with three fine-trim knobs. Built and installed on a test copy; one headset session judges it.

## 2026-10-03: Visceral RE2 — the manual-reload port begins

🔧 The plan for rebuilding manual reloads, holsters and recoil natively is written: when in a frame the hands are read and written, which pieces Visceral already covers, and the order to build in. The first piece, a bigger controller bridge that also measures its own timing, is built and waits for a headset run.

## 2026-10-02: RE Village VR Scope v1.1.2

🎮 The rifle no longer jumps to the right when it fires, and the scope now brightens and dims with the game indoors and outdoors, with no blue tint. Confirmed in the headset, then released.

## 2026-10-02: Visceral RE2 — the aim-drop is not the game's own doing

⭐ Flat test, 14 shots: with the aim button held by the game itself the aim never drops, even on our relaxed-walk files. A short gap in the aim input reproduces the headset symptom exactly. So the VR side is refusing the aim: either the controller input going missing for a moment, or the game's "lower the gun near a wall" rule reading the headset. One headset run with the new probe decides it; both fixes are already in the test copy. 🔍 Also found in the code: the Story page's rain is one effect the page requests itself, picked by the last save's location; one flat call next session should put it on the main menu. 🎮 Evening headset rounds: the gun still throws while the aim state stays up, so that reading is withdrawn; next is a round that records the hands and gun every frame. 🏆 That round found it: the shot's kick pulls the support hand off the gun for a third of a second and the VR mod swings the gun after it; one-handed, no swing. 🔧 Late night: the clip edit was not it — the swing comes from REFramework itself re-reading where the left hand sits on the gun every frame. Patched that in its source, rebuilt it, installed it — 🏆 and worn the same night: the swing is gone, after ten days and 45 test builds. 🎮 The title-screen rain now falls on the main menu too.

## 2026-10-03: Visceral RE2 VR 0.3.0

📦 Worn and liked: no gun swing, upright posture, relaxed aim-walk for Claire and Leon, rain on the main menu. Packaged as 0.3.0 for a fellow modder. From here on nothing is released publicly; progress goes out as videos.

## 2026-10-02: Lanes 0.42.0, and a tidy RE2 test copy

🔧 0.42.1 (just after midnight): session write-ups now put the two boxes first and the text last, so the next instructions sit at the bottom of the terminal.
🔧 Live sessions now run a game from its private test copy whenever one exists, unless the game is still at the early reverse-engineering stage. 📋 Visceral RE2: the disproved rain test came out of the test copy (saved as build 40).

## 2026-10-02: RE Village VR Scope v1.1.1

🎮 The left hand now lets go of a gun with a short pull, rests on the pistol without steering it, and no longer floats beside other weapons on the rifle's spot. Worn and confirmed in the headset, then released. Village is now modded on a test copy, and only confirmed builds reach the game and this page.

## 2026-10-02: BeG0nE's Village grip learns to distrust a moving hand

🔧 The far-right rifle after a relaunch is explained: the grip froze its reference while the draw animation was still moving the hand, and kept it. A reference is now taken only once the hand has held still or sits where the rifle's grip is known to be, and a weapon change forgets it. Installed on the home PC for a headset check.

## 2026-10-02: Home PC catches up

📋 The Halloween and Ocean terminal themes reached the home PC, every local theme now fades only at the sides, and six finished reminders came off the board.

## 2026-10-02: BeG0nE's Village grip worn and working

🎮 Seven quick fixes in one headset session: the grip now decides for itself from where the real hand is, keeps hold through the bolt and the reload, and puts its steering back inside the gun's shoot call. The first-shot jerk is gone from the numbers; the small move that remains is the game's own, one-handed too. Not in a download yet.

## 2026-10-02: RE Village VR Scope v1.0.2

📋 v1.0.2 released: the readme's installation steps now name praydog's release plus the five March DLSS loader files, with the reason. Both the manual package and the Fluffy package carry the new text; the Fluffy preview picture was checked in Fluffy. The mod's own files are unchanged.

## 2026-10-01 (late): the Village VR start-up crash is the REFramework build

🏆 The crash that hit the fresh install on the 30th came back and was run down with a launch loop: praydog's September dev build dies the instant the headset says ready, the March build starts every time. The grip fixes, our plugin, DLSS and the window size were all cleared. The install text now points at praydog's own release plus the five March files that differ, offered unmodified on our release page.

## 2026-10-01 (evening): BeG0nE's Village grip gets the two fixes back, without a patched loader

🔧 The two grip rules Tefa liked in September (no jerk on the first two-handed shot, and the rifle docks only with the left grip button held) were lost when the scope release moved to praydog's stock REFramework. They are back, inside BeG0nE's own Village script, with a self-check that compares its sums with praydog's every frame. Installed on the home PC, not yet worn.

## 2026-10-01: Visceral RE2, the title rain is not the Story page's camera mode

🎮 Tefa pressed the probe key on the main menu: the screen faded and came back, still dry. So the camera mode the Story page enters is not the rain switch. Eight rounds in; next is a probe that lists what exists only while the Story page is open.

## 2026-10-01: Lanes 0.41.1 and 0.41.2, the green tab opens on the Desktop; the handover light earns its keep

🔧 Lanes 0.41.1: the "Green Monitor Claude" tab the plugin adds to Windows Terminal opened in system32. It now opens on the Desktop, and the plugin says where to find its one look: the small down arrow next to the +. The theme test's helper functions had been missing since 0.41.0, so five of its checks never ran; fixed.

⚠️ The handover light said NOT SAVED on the home PC. The cause was a damaged copy of the shared board: twenty-eight half-finished downloads and a missing commit, so nothing could be fetched or pushed. Nothing was lost; a fresh copy replaced it, the old one is kept on the D: drive, and a stray Silent Hill 2 notes file was saved. Lanes 0.41.2 now says "damaged clone" for exactly this, instead of blaming a missing remote or an unreachable GitHub.

## 2026-10-01: BeG0nE gets its name and a second cure; the lanes plugin gets a look and a close-out box

🔧 BeG0nE: the occlusion-drift repo was renamed BeG0nE and became the home for every cure that removes an unwanted feature or fault from a game, one folder each. A second cure started: Camera Jitter/Shake BeG0nE, for the stepped camera so many AI-written VR mods have. First job is to find out why.

🔧 Lanes 0.41.0: the plugin now ships with a look. The first session after installing puts an old green monitor, a starburst and a rolling light on the terminal, with a backup and an undo. 0.40.0: every write-up now ends with one close-out box, printed from facts, instead of a save table and two loose lines.

## 2026-10-01: New preview clips for the ocean and Halloween themes

🔧 Both themes have fresh preview clips showing their latest look, and each loops without a visible jump. They were recorded from the terminal window alone, so nothing else on screen can appear in them.

## 2026-10-01: Lanes 0.39.0, the handover light

🧩 Every session now opens with three plain lines: is everything on this PC saved to GitHub, when did the other PC last save and how did it end, and is this copy up to date. Built after a check found five helper scripts that lived on one disk only. Every write-up now ends with that line, like the save table.

## 2026-10-01: Halloween theme, quicker start

🔧 Trimmed repeated work in the Halloween theme so its picture appears a little sooner; about 7 seconds is now the floor without removing anything from the scene.

## 2026-10-01: Village's flat-screen scope starts by itself

🎮 On the dev PC's flat-screen copy of RE Village, the scope picture now comes up by itself when the rifle is drawn. The newer rifle-camera picture still stays dark on that PC, so that part is next.

## 2026-10-01: Halloween ravens, and a faster start

🔧 Ravens now sit on the treetops, take off at the first lightning strike and land back once the storm passes. Fewer lanterns, and the picture now appears in about half the time when a tab opens.

## 2026-10-01: Village gets a flat-screen copy, and Dr.BeGonE gets its grip

🔧 RE Village: a second copy of the game now runs in a window on the dev PC for flat-screen work, and the scope comes up there too. Its picture still needs a nudge at start-up, which is next. The grip moved out of the scope mod into Dr.BeGonE, unchanged, ready to be worn in the headset.

## 2026-10-01: Theme edges, Halloween lanterns

🔧 Every terminal theme now fades only in a thin strip at the left and right, and reaches the top and bottom. The Halloween trees got swinging lanterns that light the trunks and passing spiders, and the coloured smoke now blends softly into the grey.

## 2026-10-01: Burnout's car shadow fixed, Enslaved's player found

🎮 Burnout: in the eye-shift test the dark patch under the car now moves with the car, as it should; a fix for the headlights is built too, but it needs night-time to test. Enslaved: my memory probe now finds the real player while playing, and then reads the game's camera: as I turned the mouse, the readout turned with it. Prototype: the lock-on check needs enemies around, so it moves to a later trip. Music muted in Burnout and Enslaved.

## 2026-10-01: The aquarium becomes the ocean; Halloween storm clouds

🔧 The aquarium theme is now the ocean: daylight sky over a still sea, fewer light rays, a passing whale and a school of silver fish that turn almost together. In the Halloween theme, lightning now lights up racing purple and blue storm clouds.

## 2026-10-01: Psychonauts menu void, and Tomb Raider's other VR mod read

🔄 Psychonauts: my first explanation for the empty edge on the main menu was wrong (the fix I blamed was not even switched on that day), so I withdrew it and narrowed it to one quick screen check. Tomb Raider: read another modder's VR mod for it; it uses the same spots in the game's code we found, and ours should go further with full head movement and hands.

## 2026-10-01: Halloween theme, big trees and flowers

🔧 Three big gnarled trees now stand in the field; zombies and the ghost pass behind and in front of them, and lightning shows their bark. Spiders drop from their branches, purple flowers grow in the grass, and the zombies sway more gently.

## 2026-10-01: Tomb Raider shaders checked, Death Stranding helper built

🔍 Tomb Raider: unpacked all 25,000 of the game's shaders; none applies the 3D eye shift, so it happens in one place in the game's code, which keeps the VR hook simple. Death Stranding: built and tested a small helper that will report where the camera data goes the first time the game runs.

## 2026-10-01: Halloween theme spiders, and a list of new theme ideas

🔧 Small spiders now climb the big pumpkins, slip into a mouth and crawl out of an eye. Spiders on the glass only come by now and then, and the chimney smoke fades out softly. 📋 Twelve new theme ideas are filed, from space and sewers to glitch.

## 2026-10-01: Halloween terminal theme, a livelier night

🔧 Zombies now really walk, some straight at you, some at an angle, some sideways, arms out or swinging. The witch's hut brews potions that go bang in purple and pink, colouring the smoke. The ghost turns up in ten places, near and far, and hides behind the hut, trees and gravestones.

## 2026-10-01: Halloween terminal theme, pumpkins and zombies

🔧 The big pumpkins now sit in the bottom corners, turned to look towards the middle, with the biggest half hidden past the right edge. The zombies each sway their own way and walk in more slowly. New preview clip.

## 2026-10-01: Death Stranding, the camera's layout

⭐ Read the exact layout of the camera data Death Stranding sends to the graphics card, straight from the program with the game closed. It is one shared block per view, which is the easiest kind to change for each eye.

## 2026-10-01: Death Stranding, first look done

🔍 Finished the first no-game look at Death Stranding: there is a clear way in for our helper file, photo mode is a ready-made free camera, and an old 3D setting is still listed but does nothing on PC.

## 2026-10-01: Alan Wake and Psychonauts, safer start-up

🔧 Both helper files now pass on every graphics function Windows offers, not just the one they use, which removes a start-up crash seen on another game. Alan Wake's is installed; Psychonauts' waits until the installed version is identified.

## 2026-10-01: The Witcher 2, a camera readout add-on

🔧 Wrote a packer for the game's archive format and a small script add-on that shows the camera's position and view angle on screen once a second. It waits for the game's first plain launch on this PC before it goes in.

## 2026-10-01: terminal themes, the witch's hut

🔧 The Halloween theme got a witch's hut, rounder candle-lit pumpkins, a sky that darkens before the ghost, and lightning for its whole visit. Every theme now fades its picture to black at the edges.

## 2026-10-01: terminal themes, a Halloween graveyard

🔧 A new October theme: a pixel-art night with a big ghost streaming in the wind, three lightning flashes that show zombies walking towards you, glowing pumpkins, witches and spiders. It has its own looping clip on the page.

## 2026-10-01: Enslaved, a better search for the player

🔧 The memory probe that confirmed Enslaved's engine tables could only find the player controller's blueprint, not the controller itself. It now looks for the live one by what kind of object it is, and passed its tests outside the game.

## 2026-10-01: Prototype, lock-on follows the head

🔍 The fix that keeps Prototype's objective arrows over their targets also feeds the game's lock-on targeting. With head tracking on, the game should lock onto what you look at; one flat-screen check will confirm it.

## 2026-10-01: Hard Reset, two eyes from one console setting

⭐ Reading Hard Reset's code showed that one console setting makes it draw the scene twice, once per eye, and announce which eye each time. A small stand-in for NVIDIA's library now listens for that signal; it is installed and waiting for a flat-screen test.

## 2026-10-01: Bulletstorm, the camera hook is built

🔧 Using the game's own debug-symbols file, I found the one spot where Bulletstorm hands its finished camera to the renderer, and built a small hook there that can move the camera sideways like a second eye. It passed its tests outside the game; the first in-game try is next.

## 2026-09-30: terminal themes, fish that fade with distance

🔧 In the aquarium, far-off fish are now dim and grey and the close ones bright and vivid. Each of the four themes has its own short moving clip on the page, and every clip is an exact loop: its last frame joins its first without a seam. The recording tools are in the repo, so new clips loop too.

## 2026-09-30: Lanes 0.38.0, the Inspector's score

🔧 Every lane session now ends with the Inspector's score for the code it wrote. A small fix to its design page went in as 0.37.1.

## 2026-09-30: RE Village VR Scope v1.0.1

🔄 Tefa installed the scope from the readme as a new player and DLSS did not come on: the text named a newer plugin and DLSS pair that load but find nothing. v1.0.1 names the pair that works (Upscaler Base Plugin 1.1.2, DLSS 310.5.3); the mod's own files are unchanged. The Fluffy zip now carries the readme.

## 2026-09-30: Visceral, why the pistol swings after a shot

🎮 Evening, in the headset: measured. Every shot gives a small kick that comes back; the throw is different: about a second after a shot taken while stopping, the game drops out of aiming by itself, the arms play the lower-the-gun pose, and the hands snap back when aiming returns. Why it drops is the next question, and it can be tested without the headset.

⭐ Read straight from the animation files: every stock aiming motion carries a small instruction that keeps the left hand on the gun, and the relaxed-walk motions our mod puts in carry none. So while walking and aiming, the support hand is quietly released, and the shot's kick throws the gun. A test build that forces the hold back on, and measures every shot, waits for the headset. The same build tries the Story page's camera on the main menu, to see whether that is where the rain lives.

## 2026-09-30: an aquarium for the terminal

🔧 A second terminal theme joined the green monitor: a calm pixel-art fish tank behind the text. Light blue water, plants swaying on a sea floor that rolls into the distance, rocks, bubbles and a crab. Two each of seven kinds of fish swim sideways, turn, swim away with their tails swinging and come back head-on, passing behind and in front of the plants.

## 2026-09-30: Tomb Raider, the game already draws two eyes

⭐ Tomb Raider (2013) shipped with 3D modes for old AMD and NVIDIA 3D glasses. Reading its code showed how they work: when switched on, the game draws the whole scene twice, once per eye, and one small piece of code sets each eye's view. That is a ready-made starting point for VR; the next step is choosing how to switch it on without the old glasses' drivers.

## 2026-09-30: Prototype, head tracking works in the game

🏆 The head-tracking code built this afternoon went into the game and worked on the first try: turning the "head" 10° turned the view on the spot by exactly the predicted amount, and it stayed turned while Alex walked. The floating objective arrows first stayed behind; a second fix found in the game's code now keeps them over their targets. Keys still stand in for the headset.

## 2026-09-30: Prototype, head tracking every frame

🔧 Yesterday a spare camera slot in Prototype turned and moved the view the way a head would, set by hand from outside the game. Today the code that does it by itself, every frame, is built into the mod and installed, with number-pad keys standing in for the headset for now. It was checked against thousands of test cases outside the game; the first in-game try is next.

## 2026-09-30: Burnout Paradise, the patch that stayed behind

⭐ In the first eye-shift test, one dark patch under the car refused to move with the rest of the world. Reading the game's shader files showed it is not the sun shadow, which is placed correctly: it is one of 14 objects the game draws with its own copy of the camera. A fix that moves those too is built, checked with nearly 6,000 test cases, and installed; one short flat-screen test will tell whether it worked.

## 2026-09-30: Lanes 0.37.0, the Inspector joins

🔧 The Inspector, tested in private for four days, is now part of the Lanes plugin. Switch it on and every piece of code Claude writes is looked over, and anything messy is noted for a decision before it is uploaded. It never changes code itself, and it stays off unless asked for.

## 2026-09-30: Mad Max, the HUD stays still and the smear is solved

⭐ Our per-eye shift in Mad Max used to drag the map and health display along with the world, and left objects smeared. Six test runs later: the HUD is now left alone because it is drawn flat, and the smear turned out to be the game's own motion blur, which disappears when it is switched off. The world now shifts cleanly, with one faint edge left on the car to track down.

## 2026-09-30: The Evil Within, what the camera patch reaches

🎮 Ran The Evil Within with the new tilt test. Menus and a whole room in Chapter 2 tilted, which shows our camera patch reaching them. The street at the start of Chapter 1 stayed level, with odd tilted "ghost" copies of fences and a police car. So something there is drawn another way, and finding out what is the next job. The big code file was split into six tidy ones and checked in the game, and the game's music is now muted for testing.

## 2026-09-30: Prince of Persia, a start-up safety fix

🔧 Our graphics add-on for Prince of Persia only passed on one of the seventeen things the real Windows file offers. On Dead Space 2 that exact gap crashed the game at start. It now passes on all seventeen, using the fix already proven there, and a small test confirms it without starting the game.

## 2026-09-30: Far Cry 3: Blood Dragon, a camera finder

🔧 Built a small read-only add-on for Blood Dragon that, on its first run, will write down where the game keeps its camera, read straight from the game's own shader labels. ⭐ Also found that the game's scripts can nudge the camera's position through one internal setting, which our own code could reach directly: a possible way to move the view per eye or follow head position. Nothing has been run in the game yet.

## 2026-09-30: The Evil Within, a test that can actually be read

🔄 The camera test we had been running on The Evil Within turned the picture 90 degrees in a way that could never look right: the maths squeezes the whole frame into a thin strip, which is the "slivers" seen last time. ⭐ A new test tilts the picture by 15 degrees instead, keeping everything on screen, so the next run can show exactly which parts of the world our patch reaches. Built, checked with numbers and installed, not yet run in the game.

## 2026-09-30: Metro Exodus, first launch

⚠️ Metro Exodus started for the first time. On the weaker PC its graphics card lacks the newer ray tracing this edition needs, so it crashed before the menu; all live testing moves to the stronger PC. ⭐ Reading the game's own code turned up two dormant VR switches from 4A's earlier VR game: a stereo setting that never draws two eyes as it stands, and a hidden "oculus" build option checked in 72 places. Both get their first test on the stronger PC.

🔧 The green terminal theme can now play a moving GIF behind the text.

## 2026-09-29: a picture for the Village scope in Fluffy, and a green terminal

📋 The RE Village VR scope's Fluffy Mod Manager package got its own picture, so it shows in the manager's list, and lost its "unfinished" warning, since the game is finished. The Nexus page text now has clickable links. A new rule came with it: the motion-sickness warning stays only on games still being worked on. Separately, a new repo, terminal-themes, collects retro green looks for Windows Terminal, starting with a starburst drawn as a flower.

## 2026-09-29: research round

🔍 A tidy-up check, a research pass and a cross-game sweep. The research found a likely reason Alice's shadow fix looks wrong (the shadow step works in screen space, not camera space), a clean way to widen Manhunt's view for a headset, and a fresh way into Alan Wake's stuck camera search (its own FOV slider). The shared library gained five lessons that hold across games. Later the same day every game on the account got its research check-in, the library read the games it had skipped, and every waiting note between the working areas was filed: about thirty of them, some over three weeks old. Among the finds: Hard Reset turns out to draw both eyes itself, and Tomb Raider's other VR mod switches on the game's own built-in stereo.

## 2026-09-29: Alan Wake's menus, and a simpler recorder

🔧 The player redesigned the menu recorder: Home starts, Page Down plus a key records one step, End stops, and nothing else is kept. Each game gets three goals, recorded in the player's order: into the game, to the key bindings, and back out to the desktop. Alan Wake was the first: a whole round, from a closed game into the level and back out, now takes 31 seconds by itself. Enslaved's DirectX 10 mode was also tried: it runs, but will not open in a window yet.

## 2026-09-29: Enslaved's menus play themselves, and a road is ruled out

🔧 🔍 One recording by the player became three routes: into the game, back to the main menu, and out. The game's core object lists were confirmed live while the player rehearsed. A one-launch count then showed almost everything the game loads sits in a kind of memory that the easy route to VR output refuses, so a different road is needed.

## 2026-09-29: Manhunt's menus play themselves

🔧 The player recorded Manhunt's menus on the keyboard. The tool learned three things for it: pressing keys the way this old game listens, clicking its launcher's Play button, and closing it cleanly. It now goes from a closed game to playing in about 25 seconds. Later: the black strips the player spotted around the window are fixed, and the camera the game draws with is proven to be the one we read in memory, exactly. A background check of the game's drawing code then found that everything it draws can safely be drawn twice per frame, once per eye, with three small guards.

## 2026-09-29: Menu-o-matiC maps the menus; Prototype's camera traced

🔧 🔍 On the player's idea, Menu-o-matiC now keeps a set of routes per game, each with a start and an end: to gameplay, to the key bindings page (pictured, read once, and remembered), and back out through the game's own menu. In Prototype, the most common camera number turned out to be each object's full camera view, and the camera itself was traced in the game's code, down to a spare slot that looks made for head tracking. 🏆 Tried live the same afternoon: writing into that slot turned the view on the spot and stepped it sideways with correct depth, with no rebuild. Next: a small built-in writer that does it every frame.

## 2026-09-29: Prototype runs in a window

🔧 The game has hidden start-up words for its window. Trying spellings found the one that works (`windowed` with no dash, plus `width=1280 height=720`); the other spellings switched the whole screen instead. Menu-o-matiC also gained the player's rule: rehearse a game's menus once before recording them. After a rehearsal the player recorded the menus once, and they now replay from a closed game to playing in about a minute. The plugin also now asks the player, once per game, to confirm the window before any modding.

## 2026-09-29: Alice's menus play themselves; the shadow fix could never have fired

🎮 🔍 The player recorded Alice's menus once, and they now replay from a closed game to Alice in the level in 50 seconds. Then the mod's log showed why the shadow fix never switched on: the game hands the shadow step its camera numbers just before the step starts, where the fix was not looking. The fix was moved to where the numbers arrive, and it now works in the game; whether the shadows land in exactly the right place is the next check.

## 2026-09-29: Burnout's first recorded drive

🎮 🔧 The game drove itself through its menus again, then the player drove a short stretch while every key was recorded. The replay did not match: the game clock had moved from night to day, and the car started somewhere else. Move-o-matiC now prints a short test brief before recording (what the drive is for, how far, which turn), so the next drive is played to a plan.

## 2026-09-29: Village scope packed for Fluffy Mod Manager

🔧 The finished Village scope was packed so Fluffy Mod Manager can install and remove it with one tick. It still needs a hand test before it becomes a second download. The Lanes plugin also stopped warning about an older build when going back to it was on purpose.

## 2026-09-29: Silent Hill 2 frame rate in the headset

🎮 First tuning pass with the headset connected. Turning settings down one at a time took a heavy apartment room from 48 to 72 fps; shorter, softer shadows gave the most. Outside in the fog it already holds 72. Dark rooms are the hard part, and simpler object detail made no difference, because the cost is lighting and pixels. Next: settings that change by themselves per place, 72 first.

## 2026-09-28: Silent Hill 2 bone names checked

⭐ A small read-only script read James's real skeleton from the running game: 388 bones, and every arm, hand and head name our plan relies on is there. A prediction made from another mod's saved settings, that the upper arms would be bones 56 and 126, came true. Attaching the VR tool with no headset connected froze the game, so that is now written down as a trap.

## 2026-09-28: Burnout set up together

🎮 The player played Burnout from launch to the city once while Menu-o-matiC recorded, marking each screen. The recording showed what guessing had missed: "Press Any Button" appears a moment after the title, and pressing Enter before it does nothing. The route now replays from a closed game to driving, twice in a row, every screen matched.

## 2026-09-28: State-o-matiC

🔧 New tool: State-o-matiC tells whether a game is in a menu, loading, a cutscene or gameplay. On its first run it watched Burnout from launch to the city: it caught both loading screens by how hard the game read its disk, and the idle cinematic camera by its black bars. Menus with a moving car behind them fooled it, so those screens get taught during setup.

## 2026-09-28: Move-o-matiC

🔄 Driving Burnout by guesswork did not work: the car needs the throttle held, and the on-screen map fades a second after stopping. Lesson taken: every game is now set up together with the player first.

🔧 Built that setup: the tool records the player's own key presses and timing, checks that each input reaches the game, and turns marked moments into checkpoints. Move-o-matiC then repeats the route by itself. Tried on Notepad.

## 2026-09-28: Menu-o-matiC on a real game

🎮 Menu-o-matiC drove Burnout Paradise by itself: from a closed game through the title screen, the menus, the car and paint screens to driving in the city, in two and a half minutes, without looking at the screen once. The title screen ignored the first key press while it was still fading in, so the tool now presses again when a screen is slow to come.

## 2026-09-28: Menu-o-matiC

🔧 New tool: Menu-o-matiC gets a game from launch through its menus by itself, from a route recorded once. A replay looks at nothing; it compares small patches of the screen by numbers and only asks for a look when something unexpected appears. Tried on Notepad: the recorded route replayed, and a route one letter off was caught. It is also the new `/lanes:menu` command (Lanes 0.29.0).

## 2026-09-28: Burnout Paradise

🏆 Found the camera the game draws its world with, and watched it turn with the car. It is stored in an unusual packed form, which explains why an older 3D tool only managed the sky and particles.

🎮 First camera edit: one key moves the whole view a metre to the side, the way a second eye would see it, and the picture keeps its depth. Only the car's shadow stays behind; that is the next fix.

## 2026-09-28: A pass over eight more games

🔍 Tomb Raider is back on the list: its old NVIDIA and AMD 3D modes are still inside the game. Bulletstorm's own symbol file names the camera code. Blood Dragon uses Far Cry 2's camera names. Hard Reset's hidden stereo setting drives NVIDIA's 3D Vision.

⭐ Heavy Rain hides a developer debug menu and a free camera. The Witcher 2's scripts are plain text and already include a free-camera command.

📋 The Evil Within's finished work is merged into its main copy. Death Stranding is off pause, for a version with VR hands and a body.

## 2026-09-28: Dr.BeGonE

🔧 New project: VR Super Infinite OCCLUSION DRIFT BeGonE 3000XXL Turbo, Dr.BeGonE for short. It cures occlusion drift by letting you hold two-handed weapons with the left controller just above the right, so the headset always sees both. The guide and all our code will be free for anyone to use, and each game gets a download once every long weapon in it passes testing. Resident Evil Village comes first, where the grip already works in the headset.

## 2026-09-28: The Darkness

🏆 The first run of the two-eyes-in-one-picture build worked. It proved that holding the world still between the two eyes really works on screen.

⚠️ It also showed why the eyes sometimes come out the same: the game moves its camera on a separate track from drawing the picture, and the two are not in step. Fixing that is the next job.

## 2026-09-28: RE Village — VR scope

📦 The VR scope is finished, the first project to get there. v1.0.0 is up on Nexus Mods as well as GitHub.

📋 Andyalpa is now in the credits, for the picture-in-picture scope idea that started the whole project.

## 2026-09-27: RE Village — VR scope

⭐ Looked into why the picture inside the scope turns golden and too bright outdoors. Our own code does not add the gold. The likely cause is that the rifle camera misses the game's cold outdoor colour grading. A short headset test with existing keys will tell which.

🎮 The headset test settled it: the golden look is already baked into the rifle camera's picture before our code sees it, because its bright parts are cut off. The fix is to darken that camera before the cut-off. The switch for that had a bug where whole numbers became zero; it is fixed and ready to try.

🔄 Tried it in the headset: darkening the rifle camera made the picture darker but still golden, so that idea is closed. Next is the trick that beat the same golden look in August, taking the picture before its bright parts are cut off.

⭐ That August trick turned out not to fit: the rifle camera has no uncut copy to grab. What it is missing is the game's colour grading, the part that gives the outdoors its cold look. A switch that copies the game's grading onto the rifle camera is built and ready for a headset try.

🔄 Tried in the headset: the scope stayed golden with the game's grading copied on, so that idea is closed too. Five ideas were ruled out today. The next try starts from one odd reading that suggests the lens may be showing a different picture than the one being measured.

🏆 Evening, in the headset: the gold was the rifle camera's own glow effect plus its brightest colours being cut off. With the glow off and the rifle camera darker, the scope's colours now largely match the world. The sky is still too bright; that is next.

🏆🏆 The golden scope picture is beaten, after five weeks. The last piece was our own: a script meant to keep the rifle camera matching the main view kept switching its glow back on and undoing the darker setting, nine frames out of ten. Tefa's frame-by-frame video showed it. The scope now shows the world in its real colours.

🎮 The left hand now stays in one grip on the rifle, fingers included, instead of jumping between the game's holding animations. The faint weapon clicks those animations still play were traced to the game lowering and readying the rifle by its angle; silencing them is next.

🏆🏆🏆 The VR scope is complete. The last loose ends went tonight: the weapon-handling clicks the game played when lowering, readying or aiming the rifle are silenced (the bolt and reload sounds stay), and the brightness is set. In Tefa's words: the brightness is perfect, the sounds are perfect, the hand stays on the gun, the scope points where the bullets land, and the picture is crisp.

🎮 Clean-install test passed: a fresh game, praydog's newest DLSS REFramework, DLSS 310.9.1 and the mod package worked together first time, with no batch files. A short scope freeze after taking a hit is fixed too.

🎮 Tefa tried the released scope with SteamVR instead of OpenXR, and it works just as well. The install notes now say it works with both.

📦 **Released: RE Village VR Scope v1.0.0.** A working VR sniper scope for Resident Evil Village: true colours, a steady two-handed grip, clean sound, and a scope that keeps working through hits, knockdowns and weapon switches. It installs on top of praydog's REFramework with no batch files, and the instructions list every version it was tested with.

## 2026-09-27: Visceral — RE2 VR

🎮 After a full delete and reinstall of the game, the two-handed pistol no longer swings aside after a shot. Something left over from earlier installs was causing it. The clean game is fingerprinted so any change can be spotted.

📋 Mod pieces now go back into a separate test copy of the game, one at a time, starting with the walking poses. The test copy now uses OpenXR only, Tefa's choice for every RE game.

⭐ The gun swing was tracked down, step by step, to our relaxed walking poses. The shot's kick is made to sit on top of raised arms, and our walks hold the arms lowered, so the kick threw the gun aside. A new mix, legs from the relaxed walk and arms from the game's own aiming walk, is ready to test.

🎮 That mix still threw the gun, so it waits for a deeper look. Then work started on making the last-save scene the only title background: it now shows from launch, but pressing Story still fades to black and backing out brings the old view back. Nine rounds taught how the title screen really works; the next attempt is written down.

⭐ Round 10 and 11 cracked it: the last-save scene is now the one background from launch, and switching to the Story menu is seamless. Left: the falling rain only shows after pressing Story.

🔍 Six rounds hunting the missing title rain ruled out the lamps, the Story menu's effect and its screen; it is parked with one idea left to try.

🔧 Started the big job of rebuilding Andyalpa's RE2VRMODRELOADED natively in C++ inside Visceral, using his hand poses and sounds: his mod is fully mapped, and our plugin's oversized main file was split into eight tidy files, ready for the new code.

## 2026-09-27: RE Village — VR scope

🔍 The one saved crash report turned out to be from an older build, with none of our code involved, so there is nothing to fix. For the rifle shots landing slightly low, a likely cause was found: each bullet takes the rifle's aim from a split second before the trigger, a fix made for the old mirror scope. A headset test will tell.

🎮 The test confirmed it: taking the aim from a little earlier brought the far shots in to the same small miss as the near ones. The small miss that is left comes from the bullet starting a few centimetres away from the scope's camera, and a fix for it is built and waiting for a test. The scope also survived loading a save while playing.

🏆 The fix worked: shots now land right on the cross from about one metre out to fifty. The bullet leaves from the muzzle, 6 cm below the scope, and each shot is now angled so it meets the scope's centre at whatever you are aiming at. Tefa: "it's so good! so accurate".

## 2026-09-27: Visceral — RE2 VR

🎮 The pistol swing survived every file we took out, down to a game holding nothing but praydog's own framework, so something of ours must be persisting elsewhere. The game was cleaned back to stock with a fresh framework download, and a rebuild holding only the relaxed aim-walk posture is ready to test next. Every change is now saved as a numbered version on GitHub, so both PCs test the same builds.

## 2026-09-26: Visceral — RE2 VR

🏆 The running shake is found: it came from an old REFramework build, and happened even on a freshly reinstalled game with nothing of ours in it. A fresh build is smooth with DLSS working, and our game files on top of it stay smooth. The pistol jumping sideways after a shot turned out to happen only while the left hand grips the gun. Claire's dirty hands turned out to be painted on live by the game, so an HD grime pattern of her own is the plan. Every change is now kept as its own numbered build.

## 2026-09-26

### RE Village VR scope

🏆 The rifle camera works in VR: correct picture and colours, shots land where the rifle points. Tefa: "it really feels so so good now!" Next: a little more brightness, and shots land slightly low.

🎮 First headset tests of the rifle camera: in VR the picture it copies turns out to be the frozen desktop window, not the scope view. Next: finding where the scope view goes in VR.

🏆 The rifle camera now shows its finished picture on the scope glass, in the game's own colours, with no white-out. Tefa: "it looks fantastic!" Next: centring the picture on the lens, then a look in the headset.

🔧 Built a copy of the rifle camera's finished picture taken the moment it is drawn, before the game reuses that memory, plus a switch to test why the scope picture slides. Not tested yet.

🎮 Tested the finished-picture route: it finds the right picture, but the game reuses that memory for the main view
before the frame ends, so it has to be copied earlier. Tefa spotted the rifle camera's picture was upside down; fixed.

🔧 Built the route that takes the rifle camera's finished picture from its last render stage, the way praydog's
VR mod does; it should fix the washed-out outdoors. Built and installed; not tested yet.

🔄 Tried four ways to fix the rifle camera's washed-out outdoor picture; none worked, but they showed the picture
arrives before the game's own colour grading. The fix is to take the finished picture instead, as praydog's VR mod does.
🔧 Test launches now watch the screen and press each button the moment it appears: about 30 s from closed to playing.

🔧 The static across the top of the rifle camera's picture was the game's own film-grain effect, copied onto our
camera. Found by saving the picture to disk and switching effects off one group at a time; it is now left off and the
picture is clean. Outdoors is still far too bright; that is next.

🏆 The rifle camera's big slowdown (26 fps) was our own script: it searched the whole level for the rifle
every frame. Found with a new per-stage frame timer, fixed by remembering the rifle; the scope now runs at
150–160 fps with the camera following the rifle. The barrel is hidden by a near plane that follows the
muzzle. Still open: a band of speckle at the top of the picture, and outdoors it is far too bright.

🔧 The scope's new rifle camera showed only a flat blue sky last night. Built two switches to test why:
one lets the camera follow the rifle, the other moves it there by hand every frame and writes down where
it really is.

🎮 Ran it on the flat screen. The camera really was stuck at the centre of the map. Moving it onto
the rifle worked, but the scope picture did not change, so something else is also in the way.

### Silent Hill 2

🧹 Reset the home PC's copy to a clean install. The VR injector and four add-on mods were moved out, not
deleted, and Steam's check found every game file intact. Next: study the two community VR profiles, then
start our own from zero.

🔍 Then read both community VR profiles for one question: do they use the game's own push, pull and lever
animations as your arms? Neither does. One treats those moments as a cutscene; the other replaces them with
hand-built grabs. So the idea is new, and the next step is looking at those animations from James's eyes.

### The tools behind the work

🔧 The lanes plugin now files new ideas by itself, calls each PC PC1, PC2 and so on instead of its real
name, and has a new banner and a clearer front page. A gap that let two safety checks be skipped is closed.

### This page

📋 Paused games now say only who is making their VR mod. This log had fallen a week behind; every session
now starts with a warning when that happens.

## 2026-09-25

### RE Village scope

⭐ The lights now follow the scope's aim. A real camera was put on the rifle and it renders, but its picture
is still flat blue, so the next step is pointing it properly.

### RE2 Visceral

🎮 Firing works again after the aim changes. A running shake was traced to an old framework build, and DLSS
works again. A pistol glitch is next, found by rebuilding a clean install one piece at a time.

## 2026-09-24

### RE2 Visceral

🎮 Claire's torso no longer lurches forward when you aim. It was measured from a recording made inside the
headset, because the VR view cannot be captured on the desktop.

### RE Village scope

🎮 A flat test passed: the scope starts by itself and flips cleanly with two presses.

### Ashes 2063

🎮 The first cube rifle, jackhammer and flamethrower were built with both gloved hands. The shotgun was worn
and felt too toy-like, so it goes back to Blender.

## 2026-09-23

### Every project

🔍 A research sweep checked every game against phunkaeg's VR Modding Playbook, and fresh mod ideas were
copied into each game's repo.

⏸ Games someone else is already making VR were paused and put on a watch list: Far Cry 2, Dead Space 2,
Portal, Tomb Raider, Death Stranding and Borderlands.

### Ashes 2063

🏆 `v0.1.1` released: revolver, pistol, shotgun and lantern. An unmodded Ashes pack is all a player needs.

## 2026-09-22

### RE Village scope

🏆 The scope flicker was found and is gone, confirmed in the headset. An upside-down picture turned out to be
a saved setting from stray button presses, not a bug. The two-handed grip is settled.

### Ashes 2063

🔧 The shotgun hands lost their sleeves: a black glove only.

## 2026-09-21

### RE Village scope

🎮 The stepped jitter when turning your head is gone. A repaired measure counted the flicker for the first
time. The two-handed drift was parked for later.

### The Darkness and Condemned 2

🎮 Frame rates measured on the fast home PC: well over 180 a second, plenty of room for two eyes.

## 2026-09-20

### RE Village scope

🔄 A fix for bullet scatter worked and changed nothing, because the bullet was already fired by then. A
safety check of mine also crashed the game once. Both are written down, and the lesson became a rule.

### Ashes 2063

🎮 Two-handed long guns now aim along the line between your hands, and the shotgun got gloved hands.

### RE2 Visceral

🔍 Studied what the RE4 Remake VR mod can teach this one.

### The board

🔧 The headset tag was split in two: plugged in with nobody needed, or someone wearing it.

## 2026-09-19

### Silent Hill 2: running in VR on day one, and a look under the bonnet of everyone else's work

🎮 A new project, and it moved faster than any other game here ever has. Within one sitting the game runs,
sits in a small window so it can be driven unattended, and the general-purpose Unreal VR injector hooks it and
opens a proper stereo session — a separate picture for each eye, at full resolution. Everywhere else on this
account that point takes weeks of reverse engineering; here it took an afternoon, because this is the one game
built on an engine the injector already understands.

⚠️ It crashed the first time, and the crash turned out to explain itself rather than hide: the game had shipped
set to maximum quality with ray tracing switched on, and the development machine is a long way below what this
game asks for. The error read like something fatal and was really just the game being given two minutes to do a
job that needed longer. Turning everything down and allowing more time fixed it outright.

🔍 The other half of the day went on reading the existing community VR profile end to end — not to use it, but
to learn what its authors had discovered. It is about fifty thousand lines of script, and the interesting part is
that most of it is not about this game at all: it is a general toolkit carried between several different games.
Its own comments are the most useful thing in it. They record that a thorough version of one routine was too slow
to run every frame, that a piece of maths turns a thirty-sixth of a degree of real hand movement into a fifth of a
degree of error which then has to be smoothed away, and that one graphical fix "causes a performance hit … a better
way to do this should be found". That is the jank, described by the people who wrote it.

🔄 Three things written down earlier the same day were wrong and were withdrawn rather than quietly edited —
the profile's size, how it drives the body, and whether it wrote its own posing maths. The conclusion survived the
correction and came out better argued, which is the only reason to check your own work.

### The Darkness and Condemned 2: moving two games to the machine that can actually judge them

📦 Both of these games are our own recompiles of Xbox 360 discs — neither ever had a PC release — and both
have been developed on an old, slow machine where the frame rate means nothing. That has become the thing holding
everything up, because stereo draws every frame twice: whatever a machine manages, halve it. So today both were
packed up to move to faster hardware. Not just copied — every single file was fingerprinted on both sides and
compared, 499 files for one game and 92 for the other, all identical. A file that arrives half-downloaded looks
exactly like a game bug, and that is days of hunting nobody should have to do. Each folder travels with a
plain-English setup guide and its fingerprint list, so the far end can prove the copy arrived whole instead of
assuming it. The one thing that cannot be packed is a folder shortcut — those never survive a copy — so the guide
spells out how to remake it, because nothing runs until it exists.

🔄 One correction worth recording: a note here briefly said Condemned 2 had never run on any of our machines.
It has, since 16 September, and the logs prove it — badly, on old hardware, but properly. What has never run is the
*official* prebuilt build, which needs a newer processor than the development machine has. The difference matters,
because it changes what the next test is for: not "does it work" but "how fast is it really".

### Housekeeping: the to-do boards had been hiding most of their own work

🔧 Every project here keeps a short list of what is left to do, tagged by what each job needs — nothing running,
a monitor, or the headset. A small tool reads those lists so the question "is there anything I can do without
setting up the game?" can be answered without a person going through them. Today that tool turned out to stop
reading a list the moment any entry wrapped onto a second line. On one board it could see one job out of eighteen.
Three other boards were affected, and the failure was completely silent — it reported no error, just a shorter
list. Every board has been rewritten so each job sits on a single line, and a check now confirms all thirty-four
read correctly. Two entries that were already finished had been sitting in a list as though they were outstanding;
those moved out too, since a to-do list that overstates itself is worse than none.

## 2026-09-18

### Ashes 2063: a rifle you hold with both hands, and why it shot crooked

🔫 Hold a long gun with both hands in VR and it should fire along the barrel. It did not: the shot followed whichever way the rear controller happened to be tilted, so the gun looked two-handed and shot one-handed — and the further apart the hands, the worse it got, which is exactly the guns this is for. Most of the groundwork turned out to be done already: the engine has been telling the mod where both hands are since last week, so the rifle could already be drawn along the line between them. Only the aiming was left. That is now written, with two safety checks so it quietly leaves aiming alone whenever the spare hand is not actually on the gun — holding the lantern, or just down by your side. The angle sums were checked 36 ways and then deliberately broken ten ways to prove the checks bite, including the sneaky one where up and down are swapped and the gun simply shoots high. The building and the wearing wait for the PC with the headset.

### RE Village: the second of stock glass was a timer nobody had ever timed

⏱️ Put the sniper rifle away, take it out again, and for about a second you looked at the game’s own dark glass with its orange reticle before our picture came back. The cause was not a hard problem — the mod simply waited a fixed one second before putting our picture on, a number written down once as a guess and never once checked against how quickly it could actually have been done. Shrinking the guess would only have made a smaller guess, and going too early fails silently and costs four seconds instead of one. So it now puts the picture back at the first possible moment, keeps trying until it sticks, and writes into the log exactly how many milliseconds it needed — the first real measurement of this. It also stops the mod doing pointless work when you switch straight back and the picture never came off in the first place. Built, tested 45 ways, deliberately broken nine ways to prove the test bites, and installed — but not yet seen with the game running.

### The Darkness: holding the world still, and cracking the game open

🔓 A side result that changes everything after it: the game's program file turned out to be locked
but not squashed, which means about eighty lines of code will open it up. Forty-five thousand pieces
of readable text came out, along with a full map of the game's twenty-one thousand internal parts.
The engine even names itself in there: Starbreeze's "XReality". Every future question about how this
game works just got much cheaper to answer.

⏱️ The main job was holding the world still. To show a proper stereo pair, both eyes must see the
same instant — otherwise, in a moving car, everything has shifted between them. It turns out the whole
game takes its sense of time from a single clock, so holding that one clock for the second eye holds
everything: people, physics, the car. That is now built, and the clock really is being held — exactly
half the frames, by about one frame's worth each time.

⚠️ What has not been checked is the part you would actually see: whether the world visibly stops.
That is written down as the next job rather than assumed.

📏 And the missing number arrived. One step in this game's world is about an inch, worked out from
seventeen numbers the original designers left in the game's own settings — how tall a person is, how
long a running stride is, how high a step can be. Which means the gap between your two eyes should be
about two and a half of those units, roughly twice what had been guessed.

One thing worth knowing before the headset: at a true eye gap, your own hands and gun sit only a few
inches from your face, and that is genuinely hard for eyes to merge. It is a known problem with
first-person arms in VR rather than a fault, and there are standard ways round it.


### The Darkness: the stereo bug was looking in the wrong place

🔧 Yesterday's stereo work left one bug: two characters' heads were lit red in one eye and dark
in the other. The cause turned out to be a mismatch of bookkeeping. The sideways nudge that makes each
eye was being applied to the picture-taking step alone, but the game works out where each light falls
on screen separately, on the processor, using a camera that never heard about the nudge. So the scene
was drawn from one place and lit as if from another.

The fix was to move the nudge earlier - into the camera itself, rather than the picture-taking - so
everything downstream agrees. The bug did not come back.

⚠️ Honest caveat, and it is written down as one: the check ran at a different moment in the scene
than the one that showed the bug, so it is encouraging rather than proven. A similar "looks fine"
claim was retracted yesterday for exactly that reason, so this one is tagged as unfinished.

That change also settled an open question: this camera really is the thing that decides what you see,
which means it is where head tracking will eventually plug in.

🚧 And it moved the next job to the front of the queue. To measure anything about a stereo pair,
the world has to hold still for the instant between the two eyes - otherwise, in a moving car, you
cannot tell whether the picture shifted because the eye moved or because the car did.


### RE Village: the scope picture is not taken from where the rifle is

⭐ When you crouch, the scope picture goes half under the ground. That was written down as
"something is cutting the picture off". It is not. Nothing cuts it off — **the picture is being taken
from a point that has sunk below the floor**, so the game draws the world from underneath.

The scope works by pointing a mirror at the world. A mirror does not show you the view from where it
hangs; it shows the view from the same distance on the *other* side of it — which is why a mirror on
the floor shows you the ceiling. So the scope's picture comes from a point below the mirror, as far
below as your head is above.

⚙️ And here is the part that had been hiding in plain sight. There are three sliders for where the
mirror sits. Two of them slide it along its own surface, which changes nothing about the view at all.
The third moves it up and down — and **every centimetre it moves the mirror down takes the viewpoint
two centimetres down.** It had been used all along as if it were a framing control. It is not: it is
the only one of the three that moves the viewpoint, and it does it at double speed.

Put numbers on it and the whole complaint falls out. Standing, there is about eighty centimetres of
room below you before the viewpoint reaches the floor. The setting that is currently in use spends
half of that. Crouching spends most of what is left. What remains is about ten centimetres — the
picture is being taken from around your ankles, and a little further puts it through the floor.

Each of the three facts behind this had been written down separately days ago. None of them says
anything on its own. Together they answer the question.

⚠️ Nothing was changed to "fix" it. Whether what you saw really is this, or genuinely something
cutting the picture off, is still a guess until someone looks — and quietly clamping a control on a
guess is how a setting turns into a mystery nobody can explain later. Instead the log now simply
prints how far above the floor the viewpoint is, as a number. Negative means underground.

Not run yet — it rides along with any start of the game.

### RE Village: the reading that should have shown the rifle shaking was quietly smoothing it out

⭐ The rifle in the scope mod shakes, and the scope makes it look worse. The obvious next step was
to look at how the rifle is held — but that part belongs to another mod and cannot be read from here.
The real hold-up was somewhere much closer.

There has been a number in the log for weeks that looks like it measures movement. It does not. It
compares where the rifle is pointing now with where it was pointing a second ago — so anything that
wobbles and comes back reads as no movement at all. Which is exactly what a shake is. A half-degree
shake was showing up as a fiftieth of that.

⚠️ Worse, that number is used to decide whether the rifle was being held still before another check
is trusted. A shaking rifle could pass as perfectly still there, and that check's own note says
getting it wrong costs a day of chasing the wrong thing.

🔧 The log now keeps two things instead of one: how far the aim actually travelled, and how far it
ended up. Those are nearly the same when you are aiming and wildly different when you are shaking, so
one number tells the two apart. It also reports what you actually see, because a telescope multiplies
angles — at six times magnification a tenth of a degree of wobble arrives at your eye as six tenths.
**The picture looking far shakier than the rifle is normal, not a second problem.**

⚙️ And it says honestly what it cannot answer. It can see the rifle, but not what the headset does
to the image after the game has finished drawing it. So the reading splits the question in two rather
than settling it: either the shake is already there before we get the rifle, or it is added after us.
Those are different problems with different owners, and guessing between them is what the last two
attempts at this did.

Not run yet — it rides along with any start of the game rather than needing one.

### The Darkness: the first true left-eye / right-eye picture

🏆 The Darkness produced its first real stereo pair tonight: the same moment in the back of the
car, drawn once for the left eye and once for the right. Measured, not just eyeballed: Jackie's hands
sit about 190 pixels apart between the two views, the seats in front about 47, and the on-screen
prompt exactly zero - near things shift a lot, far things a little, flat things not at all, which is
precisely what two eyes do.

🧭 That settled the big design question. Each eye will get a genuine picture of its own, drawn by
the game, rather than one picture stretched into two by guesswork. The reason is this particular
game: hands, guns and tentacles are in your face the whole way through, and faked depth falls apart
worst on exactly the things closest to you.

🔄 Two corrections, both caught the same evening. I had assumed the game sets up its view once
per frame; it does it three times, so my first attempt was swapping eyes in the middle of a picture.
And a check that said "the lighting is unaffected" was built on those scrambled eye labels, so it
could never have failed - redone properly, two characters' heads turn out lit red in one eye and
dark in the other. That is now the first real bug of the stereo work, written down as open.

Still ahead: freezing the world for the instant between the two eyes, showing the pair side by side,
and the headset itself.


### RE Village: why the scope picture was upside down, and why the button that should fix it did nothing

⭐ Two complaints from the last headset session looked separate. In one of the scope's two picture
modes everything was upside down; and the button meant to flip the picture the right way up did
nothing at all when pressed. They turn out to be the same fault, and finding that needed no game
running at all — just reading the code carefully.

That one button's setting is used in two different places on the way to your eye. Once when the
picture is built, and once again when it is handed to the glass of the scope. In the older mode only
the second one uses it, so the button works. In the newer mode both do — and two flips cancel each
other out. So the picture is locked to one orientation, and the button that should have corrected it
is the very thing holding it there.

⚙️ The honest half: it is now proved that the button cannot help, and that proof does not depend on
anything unknown. But whether the locked orientation is the right way up or the wrong way up depends
on something only the game itself can tell us. There were two reasonable answers and no way to choose
between them by reading. So nothing was guessed. Instead there is a new switch that breaks the
connection, with two settings that are proved to be exact opposites — so one of them is the right way
up, whichever answer the game gives. Two clicks in the headset settles it, instead of a session spent
finding out a guess was wrong.

A second thing worth keeping, and it is the same lesson as this morning from the other direction. The
test that proves all this works out the answer using a small copy of the rule, written inside the test
itself. If the real code changed, that test would carry on passing while describing something that no
longer exists. So it now also reads the three real places in the code and checks they still say what
it thinks they say. Then each of those was deliberately broken, one at a time, to be sure the test
noticed. All five were caught.

Not run yet — installed and waiting for the next start of the game.

### RE Village: the scope's settings file was quietly saving experiments as permanent

⚠️ The scope has a set of temporary switches you can flip while playing, to try something out for
one session. It also has a settings file that remembers your real choices for next time. Today it
turned out that pressing any of the tuning buttons wrote whatever temporary switch happened to be
flipped into that file, as if you had chosen it. It had already happened once, in the headset on the
17th: a setting nobody had chosen became the default and had to be undone by hand.

Nothing looked wrong at the time, which is the worst part — the switch was already flipped, so the
picture did not change. The bill only arrived at the next start, with nothing left on screen to
explain it. The settings file now keeps what you actually started with, and says in the log whenever
it refuses to make a temporary switch permanent.

🔧 Two smaller things went with it. Twenty-one of those switches are now buttons inside the
headset, so trying one no longer means taking the headset off, walking to the desk and typing. And
the game's log, which used to be wiped every time the game started — losing two of three test runs on
the 17th — now gets copied and kept.

⚙️ There is a lesson worth keeping from how this was checked. The new safeguard came with a set of
tests, and the tests passed. Then each piece was deliberately broken one at a time to see whether the
tests would notice. Four of the five breaks were caught. The fifth — quietly unplugging the one wire
that joins the two halves — sailed through every single check with the original fault fully back. The
tests were checking both ends and not the join, while looking thorough. That gap is closed now, but
the habit is the point: a test that has never been made to fail has not been shown to work.

None of this has been run in the game yet. It is installed and waiting, and it rides along with any
start rather than needing one of its own.

### The Darkness: the trick that gives each eye its own view works

🏆 Until today, everything about how to give each eye its own picture in The Darkness was worked
out on paper, by reading the game's code. Tonight it ran in the real game.

Two checks had to pass first. The game draws its view twice every frame, and the numbers that
describe that view had to stay put while the camera turned - if they moved with the camera, the whole
plan would have been built on sand. They stayed put, exactly. And the check was a real one: the
picture visibly swung round while it was being measured. An earlier attempt was thrown away because
the stick was pushed too gently to turn anything, so "nothing changed" meant nothing at all.

Then the shift itself: nudge the viewpoint sideways, which is all one eye of a stereo pair really is.
It landed to the exact amount asked for, six hundred times over, on the one view it was aimed at and
not the other, with the game looking completely normal. Pushed deliberately far, the 3D world
distorts wildly while the on-screen text and buttons sit perfectly still - which is exactly the right
thing to happen, and the clearest sign it is reaching the world and nothing else.

One safeguard in the plan turned out to be useless and was corrected: it was meant to protect the
on-screen display from being shifted, but the display never passes through that part of the game at
all, so it was guarding an empty room.

Still to come: both eyes at once rather than one nudged eye, and nothing has been seen in a headset
yet. But the hard part - the exact spot to change, and proof it does what it should - is now real
rather than theoretical.


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
