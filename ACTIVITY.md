# 📰 Recent Activity

[← Back to the front page](README.md)

A short, dated line whenever the work moved forward, newest first: something that now works, a cause
found, a piece built and proven, a release. Work still waiting for its test stays on the boards. For the full
story of any project, open its repo and read `modding-notes/`.

## 2026-10-28

- ❄️ **New downloads:** Window View v1.6, Hand Poser v0.2 and Grip Zones v1.1 (with Gun Poser), each saying which games it works with today. Hand Poser and Window View no longer say untested: both are in use in the headset.
- 🥽 **The Darkness:** found why the first headset run turned in a curve. The camera's three axes had been named in the wrong order since September, so every head movement landed one axis off and the two eyes sat one above the other. Fixed and proved on the OpenXR simulator: turn, nod and tilt all go the right way, left eye on the left. Later the same day the picture lagging behind the head was fixed too: every picture now reaches the headset with the head position it was drawn with. Headset check next. Evening: the first step towards motion-controlled hands landed: the table of bone positions the game sends to the graphics card was found live (three numbers-rows per bone, from slot 96), which is where a hand can be moved from. Late evening: a better way turned up. The game has its own hand-aiming code with a "put the hand here" input; fed a point of ours, the first-person hand swings into view and reaches for it, and follows the point wherever it is put (proved on the simulator). Later still, the controllers were wired in: moving a (simulated) right controller moves the right hand the same way, and the left controller moves the left arm. The hands follow position only so far; the controller's rotation is next.
- 🔧 **Lanes 0.95.0:** a day of security and privacy tests. The privacy guard now catches more ways a home folder or e-mail can be written, checks every commit again before it goes to GitHub, and can search GitHub for personal details; the ones it found were cleaned. New: each session start says when a project's game moved, was updated or went missing.
- 🔧 **Lanes 0.94.2:** found why project rows on this page fell behind (one PC's sessions never reach their end steps; nothing checked the rows) and fixed it: each session's closing box now names a row it left behind, and /od checks every row against the real work.
- 🥽 **Visceral RE8:** the game's own idle pose, which moved the gun and hands after standing still, comes from REFramework's motion-controls timer; with it set to a day the pose stayed away in the headset.
- ❄️ **Hand Poser:** one button per hand now adds the wrist and all five fingers, the long bone list folds away behind a button, and the docked left wrist (the one-night Dock Poser window) is a box inside it. Tried on a pretend game.
- ❄️ **Gun Poser (new, in Grip Zones' download):** sliders that aim and move the gun in the right hand, for each gun or all. The Village mod already reads these numbers, so the game needed no change. Tried on a test folder.

## 2026-10-27

- 🧩 **Lanes 0.94.1:** `/od` ran on the home PC. It found eight paused games whose GitHub description still said "work in progress", and fixed them. It now reads each page as GitHub shows it, not an old copy on the PC.
- 🔧 **VR Bench 0.1.1:** a new download of the robot player. Its log now says in one line why a hand does or does not move, so a run where nothing happens explains itself. Built and its 51 tests pass; not yet tried in a game.
- 🧩 **Lanes 0.94.0:** new `/od`, Out of Date. It finds anything on our GitHub older than the work behind it: a download older than its program, a tool with no download, a page behind. Its first run found VR Bench's download three changes behind. The weekly full scan now runs it before the tool check.
- ❄️ **Grip Zones (was Grab Zones):** the gun-grip sliders now have their own repo and download, ready to grow beyond Village.
- ❄️ **Downloads for our own tools:** Hand Freeze v4 (the right-stick click), Window View v1.2, Hand Poser v0.1 (not yet tried in a game) and CubeKit 0.20.0 now have their own downloads, checked with checksums. The toolkit, the game control profiles, BeG0nE and the terminal themes each got a one-zip download link on their front page, so nobody needs Lanes to get them.
- 🧩 **Lanes 0.93.0:** our own apps and libraries can now be added from Lanes as optional downloads, with tick boxes: Window View, Hand Poser, CubeKit, the toolkit, the game control profiles and more. The weekly check now spots a tool of ours that Lanes does not offer, and a connector in use that the skills page never names. The toolkit's skills and setup pages were brought up to date the same day.
- 🧩 **Lanes 0.92.0:** ten tools by elliotttate can now be added as optional downloads, each with a link to its maker: a recorder for the headset's own view, an in-headset frame-rate graph, an image sharpener, frame-inspection connectors and more. Downloads are checked against the maker's own checksums. The BeG0nE test recording now films the headset view when that recorder is installed.
- 🧩 **Lanes 0.91.0:** the weekly tool check now makes sure our toolkit page lists every tool and app we made, and flags one that has moved on since. The toolkit page itself was brought up to date: Hand Poser, Grab Zones, Window View, VR Bench, BeG0nE, Menu-o-matiC and a dozen small tools added, Hand Freeze brought up to v3.2.
- 🧩 **Lanes 0.90.0:** the BeG0nE test videos now clean up after themselves. A video is taken off the PC once the game is tested again on a later day, or after two weeks, and only after its jittery frames are cut out; the frames and reports stay. The automatic recording and the clean-up are now one optional pair.
- 🧩 **Lanes 0.89.0:** new `/ch`, Code health. It saves a working copy of every tool first, then finds what can be tidied without changing how anything works, and the weekly `/fullscan` now runs it. The first pass found a Village grip fix that had never reached the copy Lanes ships, and brought it level; every test passed after the clean-up.
- 🧩 **Lanes 0.88.3:** the second weekly check-up ran. The jitter reports can now cut out their jittery frames on the home PC (the video tool was installed but not found), and Gold Digger opens a saved report by the name its own list shows.

## 2026-10-26

- 🧹 **Flickers BeG0nE (new):** a catcher for the single-frame flicker in Resident Evil 4's grass in VR, built as one REFramework plugin file. It keeps the last 72 pictures of each eye and saves them; a reader marks the frames that flash. On the headset simulator it found all fake flickers and nothing else. Next: the real grass on the home PC.
- 🧩 **Lanes 0.88.1:** the first full weekly check-up ran: 218 saved test reports read, 27 games researched, the shared library brought up to date. Gold Digger no longer crashes on unusual characters in a log, and stops marking clean "0 failed" lines as warnings.
- 🥽 **Alice: Madness Returns:** the picture now goes to the headset through OpenXR, like Psychonauts. In the game, on the headset simulator: both eyes show, the depth check passes, and turning the head turns the view. Alice draws one eye per frame, so each headset picture is a left and right frame paired with one head pose. Next: the real headset.
- 🧩 **Lanes 0.88.0:** every run's logs and jitter reports are now kept by themselves on labelled shelves (camera, guns, menus and so on) in the folder both PCs share. `/gd` reads them shelf by shelf, and `/fullscan` runs the whole weekly check-up in one go, ending with one tick list of every update, "Everything" first.
- 🧩 **Lanes 0.87.0:** every Claude Code session can now start with Remote Control on, so it can be reached from the phone or the other PC. Lanes asks once on each PC and names the slash command either way.

## 2026-10-25

- 🥽 **Ashes 2063 and Brutal Doom:** darkness now hides the 3D guns. The engine had been drawing the held gun brighter than the room on purpose; a new setting gives it the room's own light, and lamps and fire still light it. Tefa tried it in the headset: "it looks good".
- 🥽 **The Darkness:** first run in a real headset, with Condemned 2's headset code carried over. It is in VR but still broken: the controls lag, the view swings in a curve when the head turns, and the eyes do not line up. Tefa: "it's now playable broken in VR :) very cool".
- 🥽 **Silent Hill 2:** firing with the gun lowered works in the real headset, no aim stance needed. The hand reload ran too; its buttons clash with the game's, so a single button layout is next.
- 📦 **Condemned 2 and Manhunt:** first VR builds released as work-in-progress pre-releases on each game's page, the same day each first ran in the real headset.
- 🥽 **Condemned 2:** first run in the real headset, and it just works. Tefa played it for a while with the controller: "it's like playing a vr game with a controller". 47,100 headset frames, none dropped or failed.
- 🥽 **Manhunt:** first run in the real headset. Head tracking works. The two eye pictures were pushed apart by a wrong sign in the lens maths; flipping it made it much better. A smaller gap is left for the dev PC.
- 🔧 **Heavy Rain:** head tracking works in the real headset: turning the head turns the game's view. The picture itself is not sent to the headset yet; that is next.
- 🥽 **Visceral RE8:** the grab zones now show on the gun in the headset. They had been made too late in each frame to be drawn. Hand Freeze's right stick click was worn and works.
- 🔧 **Helper apps (Window View, Hand Poser, Grab Zones, Hand Freeze):** the windows are still now, with no moving light, scan lines or animated scenes, and redraw only when something changes. Each uses under 1 % of a processor core at rest, so the headset is no longer fed a fresh picture many times a second.
- 🔧 **Hand Freeze v4:** a click of the right thumbstick now freezes or frees both hands while the app is open, and the game never sees that click, so Village no longer crouches. Proven with a new test program that presses the buttons itself.
- 🥽 **Visceral RE8:** found why the left hand jumped onto the rifle's forestock when reaching for the bolt: a stacked-hands gesture from the scope mod took it. Switched off. The front grip is now a zone the Grab Zones window can move.
- 🔧 **Window View 1.5:** a left stick click hands the motion controllers to the windows: point with the right one to click and drag sliders, and either grip carries a window, one in each hand. The pointer is now drawn every headset frame, and windows are captured straight from the screen compositor, so sliders no longer trail behind. Windows can also stay put in the room instead of following the head. Tested on the simulator, including a game that uses its own controllers.
- 🔧 **Hand Poser:** a bend-all slider per finger moves all its joints together, and each joint now shows live how it is turned as seen from the hand. Ticked sliders can be stepped with the controller buttons in Window View's controller mode, and a held grip repeats the steps.
- 🔧 **Window View 1.3:** apps are added with an ADD AN APP button or by dragging the app or its shortcut onto the window, instead of picking from a list of every open window. An app that is not running is started, and its window joins the headset when it opens. Each row shows the app's own icon. The four helper apps now share one icon style and a Lanes-style background.
- 🔧 **Hand Poser and Grab Zones:** found why their sliders flickered white: the stock Windows slider paints itself white for a moment, and Window View photographs the window many times a second. Both apps now draw their own sliders; 100 quick photos of each window came out identical. Hand Poser also has a new icon with five separate fingers, and each app shows its own icon, pixelated, behind the window.
- 🥽 **Visceral RE8 (Village):** the last headset run's log explained its four faults. The pulled magazine went straight back in because "clear of the gun" was measured closer than "in the gun". The left hand landing beside the right one was the rifle's bolt zone measured from the controller, which sits behind the drawn hand, so a missed reach for the magazine was taken by the bolt. Both fixed and installed, to be worn.
- 🥽 **Visceral RE8 (Village):** the quick slots now come from the left thumb rest and the right stick, confirmed in the headset. The game's own left-hand docking is switched off while the grip is up, so the free hand no longer jumps onto the gun. Both hands hold the shotgun again, the pump lands in the same place every grab, and the body is finally drawn turned (still an experiment, behind a switch). Later the same night: the rifle's magazine comes out by hand, grip on it and a trigger pull, drops when let go, and a fresh one goes in from the pouch.
- 🧩 **Lanes 0.86.0:** a privacy guard. Every commit on the PC is checked first, and one carrying the PC login, a home-folder path or the e-mail address is refused. 27 repos had picked up the home PC's login in notes and old scripts; all of them, and two old side branches, are clean now. The history of all 50 public repos was cleaned as well, and 0.86.1 checks pushes too.

## 2026-10-24

- 🔧 **Window View:** first real headset use. Windows opened later now show up in its list by themselves, and the mouse pointer is bigger and never gets lost between windows. Tefa: "this works really well now!"
- 🧩 **Lanes 0.85.0:** a new rule for every session: use the tools we already have before doing anything by hand, write down what was learned, and add a small tool whenever the same thing gets done by hand twice.
- 🥽 **Visceral RE2:** found why the world jumps sideways for a frame when the inventory closes: the game hands the camera back with the head's turn already in it, and the VR layer adds the head's turn once more. Read off the last headset run's log, 22 closes, all the same. The fix is built; the ladder start got a frame-by-frame probe and an on/off switch for our own view hold.
- 🥽 **Resident Evil Village:** every gun's own reload sounds were heard and named by Claude alone, so each gun now has its own handling sounds. The quick-slot cross is redrawn as four holster spots (shoulders and hips) with their names, and the repo is public.
- 🥽 **Resident Evil Village:** Claude now gives itself every gun in the game and puts each in hand, with nobody at the PC. A survey recorded all 16 guns' moving parts and sounds, so the hand reloads can reach every gun. The music is muted too.
- 🥽 **Resident Evil Village:** the guns' own handling sounds now play when the hand works them (slide, magazine, shotgun pump, rifle bolt), found by name in the game's sound bank. The whole pistol magazine drops out, and the left hand carries a new one in.
- 🥽 **Silent Hill 2:** the gun fires with the gun lowered, no aim stance: the game's own shot call, called straight, fires a real round (proven on the simulator, ten shots emptied the pistol); the trigger now does that, and the old script's "trigger = aim + fire" rule is off. Why the gun would not fire before is found in the game's code: two switches checked before every shot. Also found: the arms had lost their finger poses when the C++ took them over; they are ported.
- 🔧 **Brutal Doom and Ashes 2063:** every cube gun made so far is now in the games: 25 more in Brutal Doom and nine more in Ashes 2063, held still in the hand for now. All of them load and show as 3D models.
- 🔧 **CubeKit 0.20.0:** adding and carving cubes now keep a model's colour pattern: a new cube takes the colour of the one it sits on, and a carve paints the cube underneath in the carved one's colour. Or pick one colour for both. The build brush follows the same choice.
- 🥽 **Silent Hill 2:** found why the crosshair followed the head (the game's own one was never taken off the screen), and our plugin now removes it for good. The hand reloads were planned the Resident Evil Village way, gun by gun.
- 🥽 **Visceral RE2:** found why the VR menu text looks squished, and hand poses made in EMV Engine can now go straight into the mod. The game's long-magazine pickup already has bullets in it, so those can be copied onto the magazines.
- 🥽 **Ashes 2063:** found why every free left hand since September looked like a right hand: the game draws everything held in the left hand mirrored. A mirrored test hand showed up as a proper left hand, so the new relaxed left hand is built the other way round.
- 🖥️ **Terminal themes:** every Claude theme now opens on the Desktop, instead of a system folder or the Steam folder. New themes come with the same setting.
- 🏆 **The Darkness:** the game's hidden developer menu opens: one small hook gave the game's empty "cheat" command a body, and X on the main menu now shows it, with an Unlock all that opens every extra. The test PC's build caught up with the dev PC's and now drives itself from the title into the first level with no window in front.
- 🥽 **Silent Hill 2:** the arms moved into our C++ plugin and work in the headset: they follow the controllers, the gun sits in the right hand and bullets go where it points. Found why a lowered gun will not fire on request (the game's own code checks its aim state, not the answer scripts can change) and found the number that makes walking while aiming as fast as normal walking.
- 🌊 **Ocean theme:** day and night now take turns, three minutes each with a soft change between. Stars come out over the water at night and everything below goes darker; by day rare sunbeams reach down through the water. A 12-minute video plays the whole cycle twice with no visible join.

## 2026-10-23

- 🥽 **Silent Hill 2:** our own C++ plugin now runs inside the game beside the Lua scripts, reads their settings, and can call the game's own functions by name (checked live: position, rotation, distance). The first step of the rewrite; the hands are designed and next.
- 🥽 **Resident Evil Village:** the crash that hit about ten times in play is found: the ammo counter asked the game to show itself with the wrong kind of answer. Fixed, and the plugin now refuses any such call before it reaches the game.
- 🥽 **Silent Hill 2:** now plays in VR as one package: jbusfield's VR mod, LukasBlaster7's manual reloads and VynnGfx's performance tweaks, all with permission. The repo is public. In the prison armory it runs at about 41 frames a second, and the processor turned out to be what holds it back.
- 🎃 **Halloween theme:** the ravens are a very dark grey now, so they just stand out from the night. A 12-minute video of the night was made too: the loop runs twice with no visible join.
- 📻 **Frequency theme:** glitches now pop up in patches all over the window, each in its own way, and the old cartoon runs the other way after the two dogs merge. A 12-minute video plays the whole night of stations twice with no visible join.
- 🔧 **Doom and Ashes cube guns:** all 46 newer cube guns are now in separate pieces (grip, barrel, stock, magazine, sights and more), so each piece can be picked on its own in Blender. Nothing about their look changed.
- 🧱 **CubeKit 0.19.0:** a build brush: sweep the left mouse over a model to add one layer of cubes on its surface, the right mouse to carve one out. B switches it on and off.
- 🏆 **The Darkness:** the game bridge now works here too, built straight into our own build of the game. Claude took pictures from inside it, read its log, pressed through the title to the main menu with a virtual controller while another window was in front, then closed it cleanly.
- 🥽 **Hard Reset:** the running game now answers Claude live through a new game bridge: pictures of both eyes from inside the game, the head and hand poses, its log, keys and mouse while another window is in front, and console commands (`quit` closed it cleanly). First proof of the bridge on a real game.
- 🧰 **Two new tools (private for now):** MCP Game Bridge³, the bridge above, built so any mod can carry it and grow it; and 0ut-0f-f0cus, a game out-of-focus tool that keeps a game playing and taking input behind other windows. Both pass their self-tests on 32- and 64-bit.
- 🧩 **Lanes 0.84.0:** every Lanes feature is now optional, each with a link to read up on it first. Features that work well together are offered as a set.
- 🧩 **Lanes 0.83.0:** updates that could break a build (compilers, Visual Studio, Python, Blender, big library jumps) are now test-built first: our add-ons are built before and after, and the update is put back if one stops building. Archivers and small updates install as before.
- 🧩 **Lanes 0.82.0:** setup now offers praydog's RE Engine MCP and elliotttate's UEVR-MCP, so Claude can look inside a running Resident Evil or Unreal Engine game and read its values live. New installs choose six built-in extras instead of getting them all.
- 🧩 **Lanes 0.82.1:** the weekly tool check now ends with tick boxes, each update with a plain warning of what it could break.
- 📋 **Account tidy-up:** the e-mail address is gone from every repo, release note and download; contact is through GitHub issues now.

## 2026-10-19

- 🧩 **Lanes 0.81.0:** offers once to unlock every weapon and item in a game before modding it, found in the game files or on the first run.
- 🔧 **Doom and Ashes:** both now start with every gun.
- 🔧 **Fire and barrel glows:** burning drums and campfires in Ashes now cast flickering firelight, and Doom's barrels glow green further, so both light the guns and gloves.
- 🔧 **Gloves on the newer cube guns:** Doomguy's gloves on 23 Brutal Doom guns and the Ashes gloves on 19 Ashes guns, a first pass to look over together.
- 🔍 **Silent Hill 2:** starting again from zero, in C++. The old work is cleared and the repo will be private for now.
- 🥽 **Visceral RE2:** the left grip locks the hand onto the shotgun pump again. It had stopped gripping at all after the pump was given a single grip spot.
- 🔧 **Ashes 2063 weapons:** every weapon from Ashes 2063, Dead Man Walking, Afterglow and Hard Reset, 21 in all, now exists in cubes, copied from the game's own pictures. Big cubes for the bodies, half cubes on corners, tiny ones for screws, cuts and cracks.
- 🔧 **Brutal Doom 3D guns:** 26 more cube guns in bold free designs, from the axe and chainsaw to the BFG 10K, the Unmaker and the Dragonslayer.
- 🧱 **blender-cubekit:** a new forge that builds a whole model in three cube sizes from a short script, without opening Blender.
- 🎨 **Terminal themes:** new videos of Frequency and Halloween, each loop three times over, without music.
- 🔧 **Brutal Doom 3D guns:** the pistol, shotgun and machine gun went into the VR game for the first time, over Brutal Doom in Doom 1. Worn the same night: they sit in the hands and catch the room's light. Next, explosions and glowing items lighting them too.
- 🧩 **Lanes 0.80.0:** BeG0nE now films every headset and simulator session by itself, from the moment any of its logs starts. Setting BeG0nE up asks once: with recordings (recommended) or on its own, and where the videos go.

## 2026-10-18

- 🔧 **Brutal Doom 3D guns:** Doomguy's gloves now hold the machine gun with both hands and the hand cannon with the right.
- 🔧 **Brutal Doom 3D guns:** the machine gun got slimmer, with green sights inside its box sight, an ammo counter, barrel fins, a blade, a flashlight and a skull carved in the stock.
- 🔧 **Brutal Doom 3D guns:** the machine gun's magazine moved forward and leans forward now, and its sides got plates, levers, clamps, a grille and UAC markings.
- 🔧 **Brutal Doom 3D guns:** started the machine gun, a mash of two sci-fi guns. Dried blood stains were tried and dropped; it is worn dark red, grey and black instead.
- 🔧 **Brutal Doom 3D guns:** made three steam hiss sounds from scratch for the hand cannon's heat collector, soft to loud by how hot it is.
- 🔧 **Brutal Doom 3D guns:** the hand cannon's vent became a heat collector: it glows redder with each shot as the magazine empties. The in-game glow and steam come later.
- 🔧 **Brutal Doom 3D guns:** the hand cannon got a steam vent under its nose, for steam to blow out when a magazine drops, and gunmetal grip plates.
- 🔧 **Brutal Doom 3D guns:** the hand cannon is now black with a longer grip, and its sights are lined up for real aiming in VR.
- 🔧 **Brutal Doom 3D guns:** the hand cannon's heavy nose now runs the whole length of the barrel, with wider //// ridges spread along it.
- 🔧 **Brutal Doom 3D guns:** the hand cannon got a slimmer grip, a heavier nose with //// ridges and a longer barrel. Five diamond holes on the left, and on the right a bullet port with a cover that can swing open.
- 🔧 **Brutal Doom 3D guns:** the pistol became a hand cannon: a bigger slide with windows onto its copper barrel, a ported compensator, and silver grip plates with a military star.
- 🔧 **Brutal Doom 3D guns:** the cube pistol now follows the DOOM (2016) pistol: a boxy slide, a copper barrel in a top window and a ring module under the front, without the blue glow or the hammer. Small red and white marks are built from the smallest cubes.
- 🔧 **Brutal Doom 3D guns:** the shotgun got a thick barrel jacket with machined windows and a worn serial number. Doomguy's gloves are bigger, with leather, small-cube studs and stitching, and the Slayer's mark raised on the left hand.
- 🔧 **Brutal Doom 3D guns:** the cube shotgun now takes after the DOOM (2016) combat shotgun, keeping its dark oak pump; the stock became a dark oak grip. Panel lines, vents, screw heads and small white arrows are made of the smallest cubes. Doomguy's gloves hold it.
- 🔧 **Brutal Doom 3D guns (new):** started a project to give Brutal Doom 3D guns with Doomguy's gloves. Every weapon's fire rate, damage, reload and sound timings are now read from the mod's own files. The shotgun is under way in cubes: a dark oak stock and a square, nearly black body.
- 🧩 **Lanes 0.79.0:** the setup list now names who made every tool and says what it is for. It also offers the image and recording tools we use, and describes everything Lanes does by itself.
- 🧩 **Lanes 0.78.0:** new step-by-step guide for setting up a GitHub account the Lanes way. Claude then builds the private work board, ideas and other repos, plus a ready repo for each project.
- 🥽 **Ashes 2063:** the test tools now close the game by its window instead of typing "quit", so a test run can end without the game being in front. Typing into the wrong window had crashed the session twice.
- 🥽 **Ashes 2063:** all six cube guns now have scratches, chipped edges and small pits cut into them with the smallest cubes, instead of painted on. Saved as new copies to look at together in Blender.
- 🧩 **CubeKit:** a new script does that carving for any cube model, the same way every time.
- 🌸 **Frequency theme:** the loop now joins by the sea rising over the window into the fish, with only a soft glitch. The city's sky turns from a starry night with a moon to day, the cartoon dogs part and rejoin, and the sand and the laughing mouths fade and glitch away instead of vanishing.

## 2026-10-17

- 🌸 **Frequency theme:** the loop now ends and starts on the same colourful glitch, so a video of it joins up. The grey static sways, the bottle pours fine coloured sand, and the letter ocean heaves like water.
- 🌸 **Halloween theme:** the whole night is now one endless loop of seven and a half minutes, joining in the quiet between two ghost visits.
- 🥽 **Hard Reset:** holding the gun with both hands now puts the other hand on the barrel, and the jitter checker records those holds. Smooth turning is there as an option beside snap turns. The whole pause menu now shows on the floating panel in the headset, frames and words included.
- 🧩 **Lanes 0.77.1:** the two-handed-hold checker now also works in mods written in C, first used in Hard Reset.
- 🥽 **Hard Reset:** the gun's handle now sits in the hand, and its dial shows its numbers and moves with it. The game also keeps running and follows the aim with another window in front.
- 🧩 **Lanes 0.77.0:** a recording that stops mid-session is noticed, noted in the jitter report and restarted. VR Bench now steps, bends over and crouches. The superpowers skills are offered once.
- 🧩 **Lanes 0.76.0:** the game is now recorded by itself while the jitter checker logs a headset session, and each report comes with its jittery seconds cut out as pictures. First tried on Hard Reset.
- 🧩 **Lanes 0.75.0:** every offer is now asked once only, at the first setup or the update that brings it. New optional offer: star and follow the people whose tools and findings your work uses.
- 🥽 **Hard Reset:** the game's own gun now goes where the controller is, not only where it points. The dial on the gun does not follow properly yet.
- 🥽 **Hard Reset:** the gun's aim now leaves the menus alone, which also stopped the game minimising itself. The robot player then proved that walking goes where the head looks, that holding the gun with two hands is recognised, and that shots land where the hand points.
- 🥽 **Hard Reset:** the robot player pressed every controller button in the game, and each one did its job. It also showed the game never listens to a game pad, so walking now uses keys.
- 🧩 **Lanes 0.74.0:** VR Bench is released inside Lanes, fixed the same day after its first game showed two weak checks.
- ⭐ **Thanks:** stars on 192 more outside projects these mods have used.
- 🧩 **VR Bench (new, in Lanes):** a robot player for VR games, built on the OpenXR Simulator. In its first test it moved a hand left, up, right and down exactly as asked, in both eyes.
- 🥽 **Psychonauts:** the headset side now runs through OpenXR, the same way as Hard Reset; it is installed and waits for its first run on the pretend headset.
- 🥽 **Alice: Madness Returns:** the same OpenXR move is now on its work board.
- ⭐ **Thanks:** stars left on the 21 outside tools these projects rely on.

## 2026-10-17

- 🔧 **Visceral RE2:** the late title-screen rain is understood: the game cleared its own scratch memory under the effect it was making. The plugin now holds that off during the request; rain on the first try, before and after a game.
- 🥽 **Visceral RE2, later:** worn: the rain is fixed and the pause menu no longer flickers. The inventory still flashes on closing; its one bad frame was caught in the log .

## 2026-10-16

- 🎬 **Recording:** automatic game recording is switched off on both PCs. Progress videos stop; each mod gets one long playthrough once it is finished.
- 🧩 **Lanes 0.73.1 and 0.73.2:** the weekly tool check no longer flags a page that only quotes its own words, and it now test-starts the tool connectors after a big library update, after one nearly broke the debugger's.
- 📚 **Research:** the shared library gained four lessons from this week, the biggest being to look for a game's own lens input before rebuilding its picture maths.
- ⭐ **Death Stranding:** first live session. The game now runs in a window with a small file of ours loaded, and can be driven from the menu into play. One way of finding the camera turned out to be a dead end.
- 🔧 **Prince of Persia (2008):** our changed camera rule now gives a normal camera that follows the Prince, and a test with a different camera showed the game really uses our change. The game can now be driven from start to gameplay without help.
- 🔍 **The Witcher 2:** the camera can now be turned from outside the game, and the turning looks smooth. That is the first step towards head tracking.
- 🔍 **The Witcher 2: first live session.** It now runs in a window with our small file loaded. Our own script runs inside the game and shows the live camera on screen, once we found the check value the game puts on its script archives. A hidden network console also turned up that takes commands, such as changing the field of view.
- 🧩 **Lanes 0.73: a pretend headset on offer.** Setup and the next update now offer to download the OpenXR Simulator by elliotttate, which shows a VR game's two eyes in a desktop window. A fork that also runs 32-bit games is the other choice. Downloading never switches it on.
- 🧩 **Lanes 0.72: simulator tests record themselves.** When a game is recorded, the headset simulator's preview window is now recorded too, in its own file, even if it opens later.
- 🎮 **Hard Reset: our own VR hands (evening).** The game's model files have no tools anywhere, so instead of teaching the game a new hand, our add-on now draws the hands itself: it tracks both controllers and paints two hands into each eye where the controllers are. Proven on the headset simulator with a blocky stand-in hand. Later the same day the simulator's controllers were moved about and round a circle, and the hands followed in both eyes, on video. Then the gun was aimed by the controller while the head looks freely (the add-on steers the game's own aim to the hand and draws the picture from a fixed body frame), proven on a stand-in with 16 checks. In the afternoon it ran in the game for the first time: the gun turned with the simulator's controller while the street stayed still, on video. Found on the way: a Hand Freeze that was switched ON before v3.1 kept an old one-copy registration that stopped 32-bit VR games from starting; Hand Freeze v3.2 and Window View v1.1 now mend that by themselves.
- 🎬 **Fifteen YouTube videos cut from the 7-15 October recordings (night into morning).** One per game, named "RE2 1", "RE3 1", "Mad Max 1" and so on: only moments where the player's hands or gun are in view or the player moves, idle stretches cut, a lofi beat underneath. RE2's runs two hours. The cutting tools are kept for the next batch.

## 2026-10-16

- ❄️ **Window View, a new VR helper (afternoon).** Any desktop window can now hang in front of your eyes inside an OpenXR game, following your head like a menu: pick it in a small app, set how see-through it is, drag it by its header, resize it by its corner, and Page Up hands the mouse and keyboard to the floating windows while the game only hears the controllers. Built in one afternoon on the same two-part shape as Hand Freeze and proven on the headset simulator: Notepad showed in both eyes, typing landed in it, a drag moved it. Public repo.
- ❄️ **Hand Poser built (evening).** The window and its in-game script exist: press LEFT FINGERS and every finger of the left hand gets three sliders, already set to where the game has it; drag one and the finger follows and stays, the joints it carries along light up, undo and redo go back through 200 changes, named builds and an autosave keep poses. Proven against a stand-in game so far.

## 2026-10-15

- 🧩 **Lanes 0.71.0.** Sessions no longer answer "you're right". They check the fact first and say what they found, ask when they cannot check, and say "agreed" only after checking.
- 🎮 **Visceral RE2: why the title rain starts late (night).** The rain's "refusal" turned out to be a small crash inside the game's effect code, read from a log already on the PC.
- 🎮 **Visceral RE3: checking what came over from RE2 (night).** RE3 still uses some of RE2's numbers and gun parts. The mod now writes the game's real numbers and each gun's parts into its log, so one start shows what needs changing.
- 🎮 **Far Cry 3: Blood Dragon: a tidy-up (late night).** The headset code was split into smaller pieces without changing what it does, and an old to-do turned out to be done already.
- 🎮 **Deus Ex: Mankind Divided: its own 3D mode draws each eye (evening).** On the dev PC the game now runs in a window with the music off. Its built-in side-by-side 3D mode really draws the world from two eye positions, and the camera finder found the game's camera on its first run. The next step is seeing how the two eyes are set up.
- 🎮 **Mad Max: driving with your head turned (late evening).** Turning your head while driving made the ground vanish on that side. A fix has the game draw a wider view than the eye sees, and on small turns the ground now stays whole. The jitter checker can read Mad Max now: smooth in the headset simulator.
- 🧩 **Lanes 0.70.0.** The jitter checker now keeps flat-screen, headset-simulator and real-headset runs apart, because jitter feels different in each.
- 🎮 **Enslaved: a tidier head-tilt log (night).** The log now shows the game's own camera tilt even when the head is still, so tests are easier to read. Nothing in the game behaves differently.
- 🎮 **Deus Ex: Mankind Divided: a camera finder (night).** A small add-on that spots the game's camera by its maths, so we need no names from the game's files. It passed 20,000 made-up cameras; it waits for its first run in the game, after the 3D-mode test.
- 🎮 **Mad Max: the game's own picture reaches the headset (evening).** Steam's overlay no longer fights the headset link, and the game's real picture shows in both eyes of the headset simulator, turning with the head. The blur over the steering wheel and hands is gone: the switch built earlier had never been reached, and now it is.
- 🎮 **Deus Ex: Mankind Divided: a built-in 3D mode (late evening).** A first look through the game's files found that it can already draw two eyes side by side, a mode made for 3D TVs. The game's code is locked until it runs, so the next step is a test run with that mode switched on.
- 🎮 **Metro Exodus: the picture keeps its shape (late evening).** The game's wide picture looked stretched in each tall headset eye. That turned out to be the test tool's own preview, but one gap was real: with head tracking off, a headset would have stretched it too. Now every eye tells the headset the game's real viewing angles. Built and checked without the game.
- 🎮 **Metro Exodus: the game's own picture reaches the headset (afternoon).** Until now only a red and blue test picture got through; the game's real picture now shows in both eyes of the headset simulator. Turning your head turns the view the right way and it comes back without drifting. A view that looked broken turned out to be the test tool's own head floating 11 m up; a safety fix for the head's height went in anyway.
- 🎮 **Mad Max: where the blur inside the car comes from (evening).** The game's settings could not remove the blur over the steering wheel and hands. The game's own picture pass shows which numbers make it.
- 🧰 **Recording tool: dev PC videos reach the home PC by themselves.** They had been copied by hand, and none arrived after 10-11. Each finished test recording is now copied into the shared folder automatically.
- 🎮 **Condemned 2: the game runs in the headset simulator (afternoon).** Turning, tilting and looking up move the view the right way, and nothing froze. The game now draws exactly what the headset can see, and the eye spread comes from the headset's own setting. Next: the first try in a real headset at home.
- 🎮 **The Evil Within: why the first headset look failed (afternoon).** The "two pictures at once" came from one depth setting, now set automatically. A likely reason the world stayed flat and followed the head is fixed, and the log will now show whether it was the cause. Built and tested without the game; the home PC gets it next.
- 🎮 **Mad Max: the light turns with your head (afternoon).** Turn your head and the ground stays lit and the car's shadow stays under the car. The first try at the headset link crashed the game; Steam's overlay turned out to loop back into our code, and a guard now keeps the game alive.
- 🎮 **Condemned 2: the picture goes to the headset (afternoon).** Each eye of the stereo pair is now handed to the headset, and turning your head turns the game camera. Tested on the dev PC's headset simulator with a test program for 1,500 frames without a fault; the game itself has not been run with it yet.
- 🎮 **The Darkness and Condemned 2.** Both games and the shared library they run on now build with the newer compiler both PCs use. The new compiler also pointed at one likely fault in the shared library, now on the list.
- 🧩 **Lanes 0.69.0.** The weekly tool check (/gu) now also goes over every public repo and flags descriptions and front pages that fell behind the work; its first run fixed nine more player pages. Silent Hill 2 moved to the headset group.
- 🧹 **Front pages brought up to date (morning).** The Village scope pages now point to v1.1.5 on GitHub, Visceral RE3 says its first build is out, and The Darkness, Condemned 2 and Silent Hill 2 no longer say work has not started. Twelve repo descriptions refreshed. The dev PC's tools were updated and checked.
- 🎬 **Four progress videos compiled (night).** From ten hours of headset and flat recordings of 10-13 October: Visceral RE2 (67 min), the Village scope (17 min), the first RE3 port runs (41 min), and first looks at six other games (43 min). Desktop footage and idle stretches cut; ready for YouTube.

## 2026-10-14

- 🧩 **Hand Freeze v3 (late evening).** A new BUTTONS TOO tick box: a freeze now also holds the trigger, grip, stick and buttons of those controllers, for poses that only exist while something is pressed. Then v3.1 the same night: 32-bit games (Manhunt) failed to start with the switch on; a 32-bit copy of the layer now sits beside the 64-bit one, proven with a small test program in both sizes. Released on GitHub and installed on the home PC. RE2's bridge script now records headset pose and camera for the jitter checker.
- 🥽 **RE Village scope v1.1.5 released (evening).** The 1.1.5 build, confirmed in play last week, is now on the GitHub release page with its notes. Visceral RE2 b174 built from Tefa's evening list: an empty gun no longer triggers the shooting animation (the likely source of the phantom gunshot), and the camera is held steady for the frames a ladder or cupboard takes the body over. The menu rain's refusal points were read from the game code and are now logged. Later: the stocked Matilda's own animation lists were decoded (a hidden extra block for its shooting clips) and given the same walk fix as the plain gun, keeping its stock recoil. Tefa then wore the evening's build: the empty-gun gunshot is gone, and Hand Freeze's button hold works in the game. Night build b176: one grip spot on the shotgun instead of two, and the pistol no longer follows the left hand while it works the slide.
- 🧩 **Compiler update (late night).** Both PCs moved to the new compiler, the program that turns mod code into game files. Dead Space 2, Prototype, Psychonauts and The Evil Within rebuild cleanly with it, and their build recipes now find whichever version is installed.
- 🧩 **Lanes 0.68 and the first tool check (late night).** The weekly tool check can now update without asking and also covers the PC's own programs; its first run updated the build tools, editors and Python packages. Games that work in a headset now carry a 🥽 headset icon on this page.
- 🧩 **Lanes 0.67 (late night).** New weekly tool check, `/gu`: it brings our own tools up to date in both directions, keeps the two copies of a tool in step, lists new releases of outside tools like UEVR, and feeds lessons from game sessions into the tools. Its first run found the two copies of the menu tool had drifted apart, and they were put back in step.
- 🧩 **Lanes 0.66.1.** Sessions no longer ask whether you can see Claude beside a windowed game; you place the windows yourself.
- 🧩 **Lanes 0.66.0 and Menu-o-matiC (night).** Sessions now drive games with the recorded menu routes first and keep a note per game of what they learn (menu buttons, controls, hazards), read before every launch. Plugin updates now list what each new version adds.
- 🔍 **Manhunt.** The game itself now shows up in the headset simulator, one picture per eye, and turning the head turns the view the right way. Two faults were fixed on the way, and each eye is sharper now that the game runs at 1280x720.
- 🔧 **Mad Max (evening).** The pass that lights the ground now turns with the head as well, so light and shadow should stay in place when looking around. Built and checked on paper; the next game run will show it.
- 🔧 **Mad Max.** Turning the view with a head pose was tried on the monitor. At first it broke the colours; that is fixed, and the world now turns and looks up the right way. Lighting and shadows do not follow yet.
- 🧩 **Lanes 0.65.0.** Each PC keeps a note of which of our apps it has, so the other PC knows. Saying a job is done on the other PC now clears its reminder.
- ❄️ **Hand Freeze is public.** It works, so its repo is open to everyone now.
- 🧩 **Lanes 0.64.0.** Setup can install Hand Freeze straight from GitHub, and update tells you when a newer one is out.
- 🎞️ **YouTube footage list.** Every recording that goes into a video is now listed, so the same footage is never used twice.
- 🔧 **Visceral RE2.** The left hand now opens as it reaches for the slide or pump and curls closed on the grab, with its own shape for the pistol handle. The left hand can also be posed on its own, and two grab spots on the straightened shotgun are fixed.

## 2026-10-13

- 🔧 **Visceral RE2 (late).** The hand-tuning menu now keeps separate numbers for a gun with upgrades, such as the long magazine, and the plain gun. Tefa's tuning so far carries over.
- ❄️ **Hand Freeze (night).** The look got a last tidy, and the tool now has its own repo, private until it is tested in real games.
- ❄️ **Hand Freeze (evening).** Clearer pixel lettering, the flame button now reads UN- / FREEZE, and the rows say LEFT HAND, RIGHT HAND and BOTH HANDS. The window grew a little so everything fits, with the sun and moon in the middle of the title box.
- ❄️ **Hand Freeze (late afternoon).** New pixel-art look: summer and winter backgrounds, a round red-to-green switch, and snowflake and flame buttons for the left hand, the right hand or both. Tested on the simulator.
- ❄️ **Hand Freeze (afternoon).** A new desktop app holds both VR controllers still in any OpenXR game after a countdown, so hands can be posed with the mouse. Tested on the headset simulator.
- 🧩 **Lanes 0.63.0.** Conversations now get summarised earlier, at 40% full, so sessions stay sharp. A checkpoint is saved first and the full logs are kept on the PC. The front page now has a full guide for beginners.
- 🎮 **Visceral RE2 (morning).** The hand-tuning menu now covers the right hand too: every finger joint, the grip, and where the gun sits in the hand, saved per character and per gun.
- 🎮 **Visceral RE2 (after midnight).** Measured hand racking with Ghost Hand: the pistol slide was already steady, and the shotgun's pump area and push back are fixed. Racking by hand now replaces the button. New hand-tuning sliders save per character, per gun and per hold.

## 2026-10-12

- 🧩 **Lanes 0.62.1 (night).** Sessions now say whether anything they left running still matters, so you know when it is safe to close.
- 🧩 **Lanes 0.62.0 and Ghost Hand (night).** The BeG0nE tools now ship inside Lanes, joined by a new one, Ghost Hand, which measures where your real hand and the game's hand part. After each headset session the PC turns recordings into short reports, and the raw numbers are locked away.
- 🎮 **Visceral RE2 (night).** The finger and grip settings tuned in the headset last night are saved as build 160.
- 🎮 **Condemned 2 (late evening).** The blur and screen effects can now be switched off for VR, and both eyes show the same moment. The game makes clean stereo pairs on the monitor; next is the headset.
- 🎮 **Manhunt (night).** Checked a worry that each eye's picture would look squeezed: it won't. It is only a little less sharp side to side. Everything left on Manhunt now needs the game running.
- 🎮 **Condemned 2 (evening).** Runs on the older PC from our own build. Found where the game sets its camera; splitting it gives two viewpoints side by side. Music switched off.
- 🎮 **The Darkness (evening).** Each picture now knows which eye it is, and with a fixed freeze both eyes show the same moment. Seen in one test so far.
- 🎮 **Manhunt (evening).** Head tracking is built: turning your head turns the view, and each picture is shown from exactly where it was drawn. Proven in the small test program with the headset simulator; next, in the game.
- 🎮 **Manhunt (later).** Each eye now gets the headset's own field of view, filling the whole view instead of a floating screen. Proven in the small test program; the world does not turn with the head yet.
- 🎮 **Manhunt (late).** Built the link that sends each eye's half of the picture to the headset. Tested in a small program with the headset simulator: the left half reached the left eye and the right half the right. Next: the same in the game.
- 🎮 **Mad Max (late).** Built the headset link in, copied from the one Metro uses: each picture goes to the eye it was drawn for, with the head pose, and the headset can now turn the view. Switched off until its first test with the headset simulator.
- 🎮 **Manhunt (evening).** Started the last save test: past the first hunter and through the car-park door. Tefa will play the rest at home, so the test now waits for them; a backup tool that skips the fighting is ready but not installed. Then each eye got its own half of the screen, the step before the headset. Music muted.
- 🎮 **Mad Max (evening).** The four 3D fixes (car, shadow, motion blur, ground) now follow a head turn as well as the eye spacing. Tested without the game; a small text file can now hold a test head pose, so the next game run can try it on the monitor.
- 🎮 **Manhunt (late afternoon).** Each eye now gets its own slightly shifted view in the game, with correct depth. The grainy camcorder look can be switched off for VR.
- 🎮 **Mad Max (later).** Built the maths that turns the game's view with your head, and tested it thoroughly without the game: it turns the right way and matches the 3D that already works. Not connected to the game yet.
- 🎮 **Mad Max (afternoon).** Planned the way into the headset: one eye per frame, and head turning built on the same trick that already makes the 3D work. Also listed which blur and screen effects to switch off for VR.
- 🎮 **Manhunt (afternoon).** The world now draws twice per frame, once per eye, without changing the game's speed. It first gave a black screen; found why (the camcorder effect on the first frame) and fixed it.
- 🧩 **Lanes 0.61.0 (afternoon).** New `/lanes:uninstall`: shows what Lanes put on the PC, asks, then takes it all off, the plugin last. Your repos, notes and tools stay. The weekly `/gs` check now also tests Lanes' health.
- 🧩 **Lanes 0.60.0 and 0.60.1 (afternoon).** New standing rule: in VR every blur and every effect painted on the screen (blood spatter, rain drops, the low-health red tint, screen shake) is found and switched off, so there is only gameplay. Also fixed a settings line with a note after it being misread. Every test passes.
- 🎮 **Mad Max (afternoon).** Drove the car with the 3D on: the picture stays clean and the shadow stays under the car, straight and in turns. The cockpit view works with a real eye spacing.
- 🎮 **Silent Hill 2 remake (afternoon).** Planned how the VR arms will work: the game keeps animating James, the arms copy that each frame, and your hands steer them on top. So the game's own push, pull and lever animations can show through, then hand the arms back smoothly.
- 🎮 **Heavy Rain (afternoon).** The headset feed now runs inside the game: turning the simulated headset turns the view and it holds steady. The game can keep its own old helper files, so a Steam file check won't break it.
- 🎮 **Prototype (afternoon).** The headset can now turn the camera instead of the number pad, tilt included. Tested in a small program against the headset simulator: turning the simulated head turned the view the right way. Next: try it in the game.
- 🎮 **Metro Exodus (midday).** Built head tracking: turning your head will turn the game camera, and each picture tells the headset which way the head was facing when it was drawn, so it should not swim. Tested without the game; it stays switched off until a game test.
- 🎮 **Mad Max (midday).** The car's shadow now sits under the car in the 3D picture, in both eyes: the sun's settings were in a different place than the shader files said. Motion blur no longer smears the near sand either.
- 🎮 **Heavy Rain (morning).** Found why linking the headset closed the game: the game carries an old copy of a Microsoft helper file that the newer VR software crashes on. Proved it with a small test program, and the mod now stops safely instead. Next: try the game without that old copy.
- 🎮 **Visceral RE2 (late night).** Leon's left hand now closes its fingers round a magazine or shell while reloading, using poses saved from the older Arcade Controls work. The hand also grips the slide to rack it, and the slide now stays back until the trigger is let go.

## 2026-10-11

- 🧰 **Install check (night).** A mod file that was only moved to another folder is now reported as "moved, nothing lost" instead of "gone", and one command updates the record. This stops a false warning that had shown up at every session start for a week.
- 🧩 **Lanes 0.59.0 (evening).** Every VR mod still early in development now gets the BeG0nE jitter recorder built in, so the cause of a jittery camera is on file from the first headset run.
- 🎮 **Alan Wake and Far Cry 3 Blood Dragon (evening).** Both seen in a real headset for the first time and released as first VR builds. Blood Dragon has real depth and runs smoothly; Alan Wake's head tracking works, with jitter still to fix.
- 🎮 **Releases (evening).** Visceral RE2 0.4.0 and Visceral RE3 0.1.0 are out as public work-in-progress builds, and The Evil Within's first VR build is up as a milestone, not for playing.
- 🎮 **Alan Wake and Hard Reset (evening).** Alan Wake's head tracking works in the real headset; both now record camera timing so the jitter can be found.
- 🎮 **The Evil Within (evening).** Tefa saw it in the real headset for the first time, saved as the first VR build. The menus show in both eyes, but gameplay is still flat and stuck to the view.
- 🎮 **Heavy Rain (evening).** A head turn now rotates the free camera and it holds steady, the way looking around in VR needs. The first try at linking the real head-tracking crashed the game, so that is being tracked down.
- 🎮 **Mad Max (late).** Found that our own logging was cutting off part of what it reported, and that it never watched one way the game can send its settings. Fixed both.
- 🎮 **Mad Max (evening).** Motion blur no longer smears the 3D picture: the car stays sharp. The car's shadow still lags behind; one more suspect was ruled out.
- 🎮 **Heavy Rain (evening).** Built the first step of head tracking: a head turn laid on top of the game's free camera, done so the camera cannot start spinning. Tested without the game; next is one try in it.
- 🎮 **Mad Max (later).** Found what most likely makes the car's ground shadow lag behind in 3D: a shadow box under the car, placed using the unshifted camera. Built a fix that moves it with the eye; tested without the game, not yet in it.
- 🎮 **Heavy Rain (live test).** Our code switched on the game's hidden free camera: it takes over from the film camera and can be flown around with the keyboard. That is the starting point for looking around in VR.
- 🎮 **Mad Max.** Measured that the 3D shift moves the car and the ground but leaves the car's shadow behind, which explains the faint dark edge. Two fixes were tried and ruled out.
- 🔎 **Research sweeps.** Checked the whole collection for wrong or out-of-date notes, looked up news for the games being worked on, and fixed an old line in the shared library: SteamVR now runs 32-bit VR games through OpenXR. Found a public RE2 VR pack with holsters and reloading, and a known way round the Tomb Raider sign-in pop-up.
- 🎮 **Heavy Rain (later).** Built the switch for the game's own free camera into our file: one key turns it on and a log shows whether it worked. Tested without the game; next is one try in the game.
- 🎮 **Heavy Rain.** First run on the dev PC, now in a window with the music off. The hidden debug menu cannot be switched on by a file, but the game's own free camera can be switched on from our code; the recipe is written down.
- 🎮 **Far Cry 3: Blood Dragon.** Both eyes now show side by side in the window with real depth, and the game reached a headset simulator with each eye its own picture. Next is a real headset.
- 🎮 **Alan Wake (live test).** The fix works: the road, trees and Alan now move together in 3D, also when the simulated headset turns. The mod also finds the camera on its own now, so each PC needs no special numbers.
- 🎮 **Alan Wake.** Found why the 3D hid Alan and the fog in the headset: the game draws its world in two halves, and only one followed the 3D. Built a fix that moves both together; not tried in the game yet.
- 🧩 **Lanes 0.58.0.** New GitHub repos are now private by default, and a session asks first before making any repo public.
- 💽 **Dev PC tidy-up.** The games came off the drive that ran hot; it now holds only videos and files. Paused games and the Resident Evil copies were removed from this PC to make room.
- 🎮 **Visceral, RE2 and RE3.** The slide rack and the shotgun pump now work on a button (left grip + left trigger), the way Arcade Controls did it, so combat stays fluid. The hand-motion version is kept for later.
- 🎮 **Visceral, RE2 (late).** The D-pad moved to the right stick click, and a flashlight like RE3's got its first light: LT at the left shoulder, a beam from the chest that turns with the head. It still flickers; parked for another day.

## 2026-10-10

- 🧩 **Lanes 0.56.0 and 0.57.0.** Sessions now say plainly when the game can be closed, and short answers come as a few plain lines instead of a formatted report.
- 🎬 **Game recorder.** The automatic OBS recorder now checks every 10 seconds that it is getting a picture, and reconnects to the game window after 30 seconds of black. The same recorders now ship with Lanes 0.55.0.
- 🥽 **Headset checks without wearing it (late evening).** With the Quest connected but not worn, four games were started and measured. Alan Wake and The Evil Within reach the headset; Alan Wake’s 3D still hides Alan and the fog, and The Evil Within runs slowly in its opening cutscene. Hard Reset runs in 3D; Tefa then wore it, a flicker was found and fixed, and it is “really fun in VR”. Its first build, 0.1.0, is out on GitHub; the 3D now switches on by itself. XIII’s newest 3D build now starts with the headset.
- 🎮 **Visceral, RE2 VR (evening).** Manual reloads ported from Andyalpa's RELOADED: drop the magazine with B, take a new one from the hip, slide it in; shotgun shells one by one; slide and pump racked by moving the hand. The grenade now comes from the lower back on the right grip, and a swing throws it; Tefa: "feels superb". Saved as BASELINE 3.
- 🎮 **RE Village VR scope (afternoon).** v1.1.5 confirmed in play by Tefa: "finally working as it should in game, this is a huge achievement". The scope is done; v1.1.5 is the version everywhere.
- 🎮 **Visceral, RE3 VR (started).** RE3 got the March REFramework with DLSS ready but off. The first RE2 features are brought over: every weapon now uses the relaxed body pose for Jill and Carlos, plus the hunch fix. Not tried in the headset yet. Later the same evening the whole newest RE2 build was brought over: holsters, running, ladders, menus, two-handed grip, manual reloads and the rest, rebuilt for RE3. The first run showed RE3 was ignoring our settings file, so the poses never loaded; that is fixed. Jill now has the relaxed body; a calmer standing pose is being tried for the forward lean.
- 🎮 **Visceral, RE2 VR (afternoon).** Every menu now sits over the live game world: the inventory, map and item box lost their colour filter, the pause menu its blur and dark overlay. Tefa on the monitor: "looks great!" Pick-ups still hide the world; that is the next job. Music muted on every launch.
- 🧩 **Lanes 0.54.0 and ideas.** Four ideas that waited overnight were filed (three for RE2, one for Lanes: an uninstall command). From now on an idea mentioned during a session is filed straight away instead of waiting for the next session.
- 🏆 **Visceral, RE2 VR (night).** The two-handed grip works in every state: hold the left grip near any gun and the hand takes it, relaxed, walking, running or aiming, with no change of pose; the grip spot comes from the gun's own support-hand anchor. Tefa: "i can now run and shoot at the same time". Reloading while gripping fixed the same night. Saved as the baseline. The main menu shows the last save's scene with rain again.
- 🎯 **Visceral, RE2 VR (late night).** Bullet spread now depends on stance and hands: running is wide, walking is tighter, and standing with both hands on the gun is dead on. Long guns are a step less accurate than handguns.
- 🎮 **RE Village VR scope (night).** Reloads broke whenever the rifle was raised with the left hand gripping: praydog's hands-up block gesture made Ethan guard, which cancelled the reload. Five probe rounds to find the switch the game itself honours; now blocking is off while reloading or with two hands on a gun. The left hand also follows the reload animation. Tefa: *"it works!! ... played perfectly"*. Saved as v1.1.5.

## 2026-10-09

- 🎮 **RE Village VR scope (afternoon).** The lag with the rifle raised is gone: our own code was making the processor wait on the graphics card every frame. The scope picture now waits for both hands to be up, and stops only when the glass is seen nearly edge-on. Tefa: *"the lag is completely gone!"* Then back to v1.1.3 with only the colour fix and the lag fix on top: *"scope is great!"* Saved as v1.1.4.
- 🎨 **Terminal themes.** The newest look, Frequency, added on the home PC as an extra tab.
- 🎮 **Visceral, RE2 VR (night).** Menus: the tilt is gone and the one-frame flash of Leon's body on closing is gone. The inventory still flickers for a frame; DLSS was ruled out. Next: a headset recording picked apart frame by frame.
- 🧩 **Lanes 0.53.0.** A desktop shortcut named Lanes now opens Claude Code in the plugin's look, same font and background. The first session after the look goes on offers it once; so does an update.
- 🎮 **RE Village VR scope.** The outdoor blue tint is solved. The scope's colour dial now pulls blue down on top of the picture, with the sky and fog left in; tuned over three launches to "it's perfect now". Brightness and the VR crosshair-off setting saved with it. Later: the scope's own camera now draws with the lowest picture effects while the game keeps its settings, for a smoother scope, and the DLSS upscaler was switched off after the scope looked DLSS-blurry. Tefa: sharp picture, runs really well; DLSS stays off for Village. Checked whether the scope alone could use low mesh detail: no, this engine picks detail per object, not per camera. The frame drops came only with the rifle out, so the scope's camera now draws only while the rifle is raised to the eye. Worn: it works. The lens also dims when the right hand is away from the headset, and the scope camera only works on every other frame while aiming; tuned with Tefa over several rounds.

## 2026-10-08

- 🧠 **Visceral, RE2 VR (evening).** Read the VR layer's own code and found why menus tilt: it adds the headset's turn on top of a camera that already has it. Also found why the shotgun sits crooked in the light: the two-handed grip reads the relaxed clip's arms.
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
- **Terminal themes:** started Frequency, a new look that keeps changing station like a radio dial, from fish bones and skulls to a 1930s cartoon on an old TV and an asteroid field, with random psychedelic glitches. The whole loop plays.
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

🏆 Hard Reset draws both eyes by itself once a console setting is on, about 120 times a second each, and it compiles our own edited shader files. The eye pictures do not reach the window yet. 🔧 Alice: the shadow fix was re-worked out from the game's own shaders.

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

🔍 A new recorder showed that every part of the opening street is reached by our camera change, yet the street still looks untouched, so the cause is further down the line than thought. The game can now be walked around by the computer on its own. 🔄 Then Tefa looked in the running game: the street does tilt. It was never broken; I had misread my screenshots. A first two-eye mode was built and then seen working in the game: one frame per eye, with near and far in the right order. 🏆 Late on, the game showed up in both eyes of a headset simulator, with the menus kept flat while the world is 3D. Sharing the game's own graphics device with the headset froze the game, so the headset now gets its own.

## 2026-10-06: Alan Wake — the dead end was not a dead end

🔄 A month ago we decided our camera changes did nothing on screen. Re-reading the old pictures showed they did; the comparison had been fooled by the camera moving between runs. A new on/off key proved it live: one eye's view now shifts with proper depth. Music is muted. The game measures in metres, so a real eye distance can now be set. Then built the first two-eye mode, one frame per eye, and saw it alternate in the game. Lighting now follows each eye too, with motion blur switched off. Late on, the code was tidied into smaller files and the first headset output was built: a floating 3D screen, one picture per eye. It then worked end to end in a headset simulator. Head tracking came last, and in a headset simulator turning, nodding and tilting the head all move the view the right way in both eyes.

## 2026-10-06: Bulletstorm — two eyes in one frame

⭐ The first camera edit works in the game: the view can be slid sideways like a second eye, with near things moving more than far ones and the HUD staying put. The game now runs in a small window with the music off.

🏆 Later the same day: the game now draws two eyes in one frame, side by side, by borrowing its own split-screen mode. Next is the HUD in both eyes.

## 2026-10-06: XIII — the mystery draws were never there

🔄 One keypress in the bank level settled it: nothing is drawn flat on the screen except the HUD, so the twelve "screen-space" draws were a misreading, and the fix for it holds. A second puzzle turned out to be a units slip. Music is now muted, and the game can be quit by keyboard.

## 2026-10-06: Lanes 0.46.0 — builds by feature, originals kept

🔧 Each feature's builds now get their own folder. The game's original files are saved before a mod changes them, so a plain, working game can always be put back.

## 2026-10-06: Visceral RE2 — next jobs lined up

📋 Planned four new jobs: ladder climbing taken over from Arcade Controls, the left hand staying on the gun, quicker stops when running, and no player body showing in menus. Manual reloads wait for the new firing work.

🔧 Each feature's builds now get their own folder.


## 2026-10-05: Visceral RE2 — every gun relaxed

🔧 Leon's relaxed body pose, first made for the pistol, now goes on every gun and its upgrades: magnum, SMG, shotgun, launchers, the flamethrower group, the knife and grenades. Claire and Ada got the same on every weapon. 🎮 Worn: every weapon works, Hunk too; saved as a roll-back build. 🔧 Started a new C++ plugin for the RELOADED features; the four holster spots now take out and put away whatever is in the game's weapon shortcut. Putting grenades there broke the menus, so that was rolled back. Built from the game files alone; not worn yet.

## 2026-10-05: Visceral RE2 — the left hand and the pistol

⭐ The new straight-body animations had lost the game's own switch that keeps Leon's left hand on the gun. A new tool puts that switch back while keeping the straight body; it is in the game, waiting to be worn.

## 2026-10-04: Tidying the game folders

📋 RE Village: the colour work from the test copy now sits in the real game, and the copy is gone. 📋 RE2's old test copy is gone too; its mod files were already saved. 🏆 Visceral RE2: the shake is traced to the upper-body straightener, and with the pistol out Leon now moves exactly like with no gun, straight and smooth. The upgraded Matilda turned out to have its own aiming animations. 🔧 Lanes 0.44.0 and 0.45.0: every session summary is now saved, dated, in its own folder per project, and breakthroughs are marked IMPORTANT.

## 2026-10-04: Research sweep

⭐ Found that a Tomb Raider VR mod switches on the game's own built-in 3D mode with stand-in graphics-driver files, and that Hard Reset could be woken the same way. Two lessons that held in a second game went into the shared library. Silent Hill 2 got its first research page. A second pass covered every game: a public mod maps Death Stranding's camera on our exact version, and Condemned 2's port has a new release with field-of-view and frame-rate settings.

## 2026-10-04: Enslaved — where the camera is decided

⭐ Found the one spot each frame where the game settles where the camera looks, just before it draws.

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

🎮 On the dev PC's flat-screen copy of RE Village, the scope picture now comes up by itself when the rifle is drawn. The newer rifle-camera picture still stays dark on that PC.

## 2026-10-01: Halloween ravens, and a faster start

🔧 Ravens now sit on the treetops, take off at the first lightning strike and land back once the storm passes. Fewer lanterns, and the picture now appears in about half the time when a tab opens.

## 2026-10-01: Village gets a flat-screen copy, and Dr.BeGonE gets its grip

🔧 RE Village: a second copy of the game now runs in a window on the dev PC for flat-screen work, and the scope comes up there too. Its picture still needs a nudge at start-up.

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

⭐ Reading Hard Reset's code showed that one console setting makes it draw the scene twice, once per eye, and announce which eye each time.

## 2026-10-01: Bulletstorm, the camera hook is built

🔧 Using the game's own debug-symbols file, I found the one spot where Bulletstorm hands its finished camera to the renderer, and built a small hook there that can move the camera sideways like a second eye.

---

## 🗂️ Older months

Each month stays on this page while it is happening. When a new month starts, the whole of the
previous month moves to its own page, listed here, newest first.

- [September 2026](activity/2026-09.md): every entry of the month, as it was written
- [August 2026](activity/2026-08.md): the month it all began, with highlights and flops

*October 2026 moves here on 1 November.*
