# 📰 Recent Activity

[← Back to the front page](README.md)

A short, dated line for every working session, newest first. It includes the days when nothing
advanced, because dead ends and corrections are part of how this work really goes. For the full
story of any project, open its repo and read `modding-notes/`.

**Key:** 🏆 breakthrough · ⭐ promising find · 🎮 hands-on test · 🔄 correction · ⚠️ something went
wrong · 🔧 tooling · 📋 housekeeping

---

## 2026-09-19

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
