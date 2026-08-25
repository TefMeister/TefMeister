### Hi, I'm working on VR reverse-engineering of older flatscreen games

Personal, non-commercial fan modding: reverse-engineering flat 3D games I already
own into VR (stereo rendering, head tracking, and where possible motion controls),
one engine at a time. Every project requires owning a legitimate copy of the game
and redistributes no original assets — see each project's `CONTRIBUTING.md` /
`CREDITS.md` for the full terms and every source credited.

**Looking for a specific game and don't see it below?** It's probably not started
yet — check the two shared-knowledge repos at the bottom first; a lot of the
technique material there (generic drivers, engine-agnostic core, per-engine
landscape notes) applies even to games with no dedicated project.

---

## How this is organized

Every game project gets **six repos**, same suffixes every time, so you can jump
straight to what you need instead of digging through one giant repo:

| Suffix | What's there |
| --- | --- |
| `-mod` | The mod itself — releases only |
| `-dev-archive` | Full messy in-progress history: snapshots, probes, dead ends |
| `-modding-notes` | Readable field notes / progress ledger, one dated entry per session |
| `-engine-research` | Distilled current truth: engine dossier + the reusable VR-RE playbook |
| `-external-research` | Public-research leads (prior art, techniques) gathered separately from hands-on modding |
| `-staging` | 🔒 private — unverified work-in-progress, not for browsing |

A `-mod` repo's release notes always carry a disclaimer of what the mod is/isn't,
plus a motion-sickness caution while a project is unfinished.

## Projects

| Game | Engine | Status | Repos |
| --- | --- | --- | --- |
| **Psychonauts** (2005) | Bespoke Double Fine engine (D3D9, Lua) | Core VR (stereo + 6DOF head tracking) **working in a real headset**; active dev | [mod](https://github.com/TefMeister/psychonauts-vr-mod) · [notes](https://github.com/TefMeister/psychonauts-vr-modding-notes) · [dev-archive](https://github.com/TefMeister/psychonauts-vr-dev-archive) · [engine](https://github.com/TefMeister/psychonauts-vr-engine-research) · [research](https://github.com/TefMeister/psychonauts-vr-external-research) |
| **XIII** (2003) | Unreal Engine 2 (D3D8) | Milestone 1 (VR head-look) **verified in a real headset**; native stereo in progress | [mod](https://github.com/TefMeister/XIII2003-vr-mod) · [notes](https://github.com/TefMeister/XIII2003-vr-modding-notes) · [dev-archive](https://github.com/TefMeister/XIII2003-vr-dev-archive) · [engine](https://github.com/TefMeister/XIII2003-vr-engine-research) · [research](https://github.com/TefMeister/XIII2003-vr-external-research) |
| **Far Cry 2** (2008) | Dunia Engine (D3D9) | VR bridge **confirmed working on real headset hardware**; head tracking next | [mod](https://github.com/TefMeister/far-cry-2-vr-mod) · [notes](https://github.com/TefMeister/far-cry-2-vr-modding-notes) · [dev-archive](https://github.com/TefMeister/far-cry-2-vr-dev-archive) · [engine](https://github.com/TefMeister/far-cry-2-vr-engine-research) · [research](https://github.com/TefMeister/far-cry-2-vr-external-research) |
| **Unreal Gold** (1998) | Unreal Engine 1 (OldUnreal 227k) | From-scratch native D3D11 render device; world rendering playtested; stereo next | [mod](https://github.com/TefMeister/unreal-gold-vr-mod) · [notes](https://github.com/TefMeister/unreal-gold-vr-modding-notes) · [dev-archive](https://github.com/TefMeister/unreal-gold-vr-dev-archive) · [engine](https://github.com/TefMeister/unreal-gold-vr-engine-research) · [research](https://github.com/TefMeister/unreal-gold-vr-external-research) |
| **The Evil Within** (2014) | id Tech 5 "STEM" (D3D11) | Pre-release — building the stereo 6DOF core, no headset output yet | [mod](https://github.com/TefMeister/the-evil-within-vr-mod) · [notes](https://github.com/TefMeister/the-evil-within-vr-modding-notes) · [dev-archive](https://github.com/TefMeister/the-evil-within-vr-dev-archive) · [engine](https://github.com/TefMeister/the-evil-within-vr-engine-research) · [research](https://github.com/TefMeister/the-evil-within-vr-external-research) |
| **Visceral — RE2 VR** | RE Engine (via praydog's REFramework) | Ground-up interaction-overhaul rebuild, design phase | [mod](https://github.com/TefMeister/visceral-re2-vr-mod) · [notes](https://github.com/TefMeister/visceral-re2-vr-modding-notes) · [dev-archive](https://github.com/TefMeister/visceral-re2-vr-dev-archive) · [engine](https://github.com/TefMeister/visceral-re2-vr-engine-research) · [research](https://github.com/TefMeister/visceral-re2-vr-external-research) |
| **RE Village — VR scope** | RE Engine (native REFramework plugin) | In-progress picture-in-picture sniper scope; VR path researching render-target GPU backing | [mod](https://github.com/TefMeister/re-village-scope-vr-mod) · [notes](https://github.com/TefMeister/re-village-scope-vr-modding-notes) · [dev-archive](https://github.com/TefMeister/re-village-scope-vr-dev-archive) · [engine](https://github.com/TefMeister/re-village-scope-vr-engine-research) · [research](https://github.com/TefMeister/re-village-scope-vr-external-research) |
| **Enslaved: Odyssey to the West** | Unreal Engine 3 (NTEngine, D3D9) | Early — repos scaffolded, work just starting | [mod](https://github.com/TefMeister/enslaved-vr-mod) · [notes](https://github.com/TefMeister/enslaved-vr-modding-notes) · [dev-archive](https://github.com/TefMeister/enslaved-vr-dev-archive) · [engine](https://github.com/TefMeister/enslaved-vr-engine-research) · [research](https://github.com/TefMeister/enslaved-vr-external-research) |
| **Mad Max** (2015) | Avalanche/Apex Engine | Early — repos scaffolded, work just starting | [mod](https://github.com/TefMeister/mad-max-vr-mod) · [notes](https://github.com/TefMeister/mad-max-vr-modding-notes) · [dev-archive](https://github.com/TefMeister/mad-max-vr-dev-archive) · [engine](https://github.com/TefMeister/mad-max-vr-engine-research) · [research](https://github.com/TefMeister/mad-max-vr-external-research) |
| **Prince of Persia** (2008) | Proprietary Ubisoft Montreal engine | Early — repos scaffolded, work just starting | [mod](https://github.com/TefMeister/prince-of-persia-2008-vr-mod) · [notes](https://github.com/TefMeister/prince-of-persia-2008-vr-modding-notes) · [dev-archive](https://github.com/TefMeister/prince-of-persia-2008-vr-dev-archive) · [engine](https://github.com/TefMeister/prince-of-persia-2008-vr-engine-research) · [research](https://github.com/TefMeister/prince-of-persia-2008-vr-external-research) |
| **Alice: Madness Returns** (2011) | Unreal Engine 3 | Early — repos scaffolded, work just starting | [mod](https://github.com/TefMeister/alice-madness-returns-vr-mod) · [notes](https://github.com/TefMeister/alice-madness-returns-vr-modding-notes) · [dev-archive](https://github.com/TefMeister/alice-madness-returns-vr-dev-archive) · [engine](https://github.com/TefMeister/alice-madness-returns-vr-engine-research) · [research](https://github.com/TefMeister/alice-madness-returns-vr-external-research) |
| **Burnout Paradise** (Remastered) | Criterion in-house engine (D3D11) | Early — repos scaffolded; the active front, first-look reverse-engineering starting now | [mod](https://github.com/TefMeister/burnout-paradise-vr-mod) · [notes](https://github.com/TefMeister/burnout-paradise-vr-modding-notes) · [dev-archive](https://github.com/TefMeister/burnout-paradise-vr-dev-archive) · [engine](https://github.com/TefMeister/burnout-paradise-vr-engine-research) · [research](https://github.com/TefMeister/burnout-paradise-vr-external-research) |
| **Alan Wake** (2010) | Proprietary Remedy engine (pre-Northlight) | Early — repos scaffolded, work just starting | [mod](https://github.com/TefMeister/alan-wake-vr-mod) · [notes](https://github.com/TefMeister/alan-wake-vr-modding-notes) · [dev-archive](https://github.com/TefMeister/alan-wake-vr-dev-archive) · [engine](https://github.com/TefMeister/alan-wake-vr-engine-research) · [research](https://github.com/TefMeister/alan-wake-vr-external-research) |
| **Manhunt** (2003) | RenderWare (D3D8) | Early — DRM-remnant bug root-caused, windowed mode queued next | [mod](https://github.com/TefMeister/manhunt-2003-vr-mod) · [notes](https://github.com/TefMeister/manhunt-2003-vr-modding-notes) · [dev-archive](https://github.com/TefMeister/manhunt-2003-vr-dev-archive) · [engine](https://github.com/TefMeister/manhunt-2003-vr-engine-research) · [research](https://github.com/TefMeister/manhunt-2003-vr-external-research) |
| **DOOM** (2016) | id Tech 6 | Early — repos scaffolded, work just starting | [mod](https://github.com/TefMeister/doom-2016-vr-mod) · [notes](https://github.com/TefMeister/doom-2016-vr-modding-notes) · [dev-archive](https://github.com/TefMeister/doom-2016-vr-dev-archive) · [engine](https://github.com/TefMeister/doom-2016-vr-engine-research) · [research](https://github.com/TefMeister/doom-2016-vr-external-research) |
| **Arcade Controls for RE2 VR** *(closed)* | RE Engine (via REFramework) | Shipped on Nexus through v1.5.0; **superseded by Visceral — RE2 VR**, kept as frozen study material | [mod](https://github.com/TefMeister/arcade-controls-re2-vr-mod) · [notes](https://github.com/TefMeister/arcade-controls-re2-vr-modding-notes) · [dev-archive](https://github.com/TefMeister/arcade-controls-re2-vr-dev-archive) · [engine](https://github.com/TefMeister/arcade-controls-re2-vr-engine-research) |

## Shared knowledge (applies across every project, and to games with no project yet)

- **[flat-to-vr-cross-engine-research](https://github.com/TefMeister/flat-to-vr-cross-engine-research)** — a public, engine-agnostic library of *publicly-available* flat→VR modding knowledge: an engine landscape index, generic-driver options (vorpX, geo-11), engine-agnostic core patterns, and worked case studies. Every source credited in its `ATTRIBUTION.md`.
- **[flat-to-vr-RE-toolkit](https://github.com/TefMeister/flat-to-vr-RE-toolkit)** — battle-tested tools, skills, and the reusable VR reverse-engineering playbook used to start every project above.

---

*All reverse-engineering here targets legitimately-owned copies of each game for personal,
non-commercial modding. No original game assets or engine source are redistributed in any
repo above. Corrections/removal requests from actual rights holders are honoured promptly —
contact details are in each repo's `CONTRIBUTING.md`.*
