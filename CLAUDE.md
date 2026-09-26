# Sol Academy (working title) — Claude Code project guide

Solo indie JRPG for Steam, made under the **Nerd Practitioner** brand. GitHub: `NerdPractitioner/sol-academy`.
The owner (Matt) is a non-professional game dev who wants Claude to help at every step from idea to Steam launch. Budget is tight: prefer free tools, and say plainly when a paid tool or a human (artist, composer) would do a job better.

## The game in one paragraph
A space-academy JRPG where every action takes ticks to wind up, so allies can react mid-attack: dive in front of a hit, brace, charge a finisher together (Assist infusions), grapple-pin an enemy, or lock into a **beam clash**. The combat system IS the game; prove it's fun before investing in story/art.

## Story/world (premise)
Civilizations reach "Tier 3", a black-hole portal opens, and humanity is taken to the center of the universe where chakra/magic is potent. Periodic elements radiate outward from the center in different ratios by direction, so races from different sides are made of different things (carbon = human/adaptable, silicon = durable/slow, iron/heavy metals = conductive/beam-strong). Body chemistry doubles as the combat affinity system. Setting: an academy where races train together against a threat that forces teamwork.

## Where things stand (2026-09-26)
- Phase 1 combat prototype exists: `index.html` at the repo root (Combat Lab 1.6, imported from the claude.ai artifact). Self-contained: loads Phaser 3.80.1 from cdnjs and Google fonts, all game code inline. Open it directly in a browser to play. All tunables live in `CONFIG` at the top of the script. Naming is inconsistent (page says 1.6, code header says v0.6); pick one scheme when convenient.
- **Not yet playtested by outside humans.** That is the top priority.
- Roadmap features not yet in the prototype: Interrupt, Counter, more synced-combo bonuses.
- Story bible and visual style bible were drafted in an earlier chat (Sept 1) but never saved. If Matt has them, add to `docs/`.
- Engine is undecided: roadmap suggested Godot 4, but Matt is testing by feel (Phaser browser prototype first, Godot not yet tried). Don't port until he decides.

## Open decisions (ask Matt, don't assume)
1. Art style: pixel vs 2D illustrated vs low-poly 3D (pixel is the safest solo choice)
2. Phaser vs Godot as the real engine
3. Faction branding vs elemental-vector color on characters
4. AI companion identity (too close to Jarvis)
5. Studio name = channel name (Nerd Practitioner)?

## How to work with Matt
- Warm, friendly, a little chaotic; he has ADHD-friendly needs: give small concrete next steps and quick wins, keep momentum visible.
- Explain choices in plain language; he's learning as he builds. Show the real numbers, including bad ones.
- Make changes runnable so he can *feel* them (browser first). Keep balance numbers in data/config, not scattered through code.
- Save durable decisions into `docs/` (update `docs/project-tracker.md` as you go).

## Docs
- `docs/roadmap.md` — phases 0–6, idea to Steam
- `docs/project-tracker.md` — status table, open decisions, suggested focus
- `docs/combat-design-notes.md` — how the current prototype's rules work, plus tuning knobs
- `docs/nerd-practitioner-brand-brief.md` — brand, mission, voice, revenue ladder
- `docs/HANDOFF.md` — setup steps and first-session prompts

## Suggested next 1–2 weeks
1. Get 3–5 non-friend people to play Combat Lab for 10 minutes and note confusion/boredom.
2. Save story bible + style bible into `docs/`.
3. Write the 1-page design doc (pitch, player fantasy, core loop, scope limits: 8–15 hrs, 4–6 party members).
4. Check the Nerd Practitioner name (USPTO tmsearch.uspto.gov) and grab handles before any logos.
