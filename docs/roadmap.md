# Matt's Game — Build Roadmap (idea → Steam)

## The one-sentence pitch (draft)
A space-academy JRPG where every action takes time to wind up, so allies can react mid-attack — dive in front of a hit, charge a finisher together, or lock into a beam clash — and every fight plays out like an anime set piece.

The combat system is the game. Everything below is ordered so that gets proven fun first, before money or months go into story and art.

---

## Phase 0 — Decide the scope (1 week)
- **Pick a size you can finish.** First commercial game target: 8–15 hours, 4–6 party members, 1 academy hub + 4–6 regions. Cut ideas into a "sequel" file instead of deleting them.
- **Engine: Godot 4 (free).** Your multi-turn/reaction combat is too custom for RPG Maker; Unity/Unreal are heavier than you need. Claude writes GDScript well.
- **Art style decision:** pixel art (cheapest, classic JRPG) vs. 2D illustrated vs. low-poly 3D. Pixel art is the safest solo choice.
- Deliverable: a 1-page design doc (pitch, player fantasy, core loop, scope limits).

## Phase 1 — Combat prototype, grey boxes only (3–6 weeks)
Build the combat on a timeline, not simple turns:
- Every action has a **wind-up (N ticks)** and then resolves. Faster moves = shorter wind-up; power attacks = long wind-up.
- A visible **turn-order timeline** shows everyone's pending actions, so players can see threats coming.
- **Reactions** (spend a resource, e.g. "Resolve"): Guard, Intercept (jump in front of an ally), Counter, Interrupt.
- **Charge & Combo:** allies can pour power into a charging attack; synced attacks get bonuses.
- **Beam Clash:** if an enemy is winding up a beam, a player can lock in their own beam → clash mini-contest (timing/button-mash or stat-based tug-of-war) → winner's beam goes through with bonus damage.
- Test with 3 heroes vs. 2–3 enemies, placeholder squares and numbers.
- **The goal:** is a single fight fun and readable for 10 minutes? Iterate until yes. Show it to 5 people who aren't friends-being-nice.

## Phase 2 — World & story bible (parallel with Phase 1, 2–4 weeks)
- **Premise:** civilizations reach "Tier 3" → a black-hole portal opens → humanity arrives at the Universal Center where chakra/magic is strong.
- **Element-ratio races:** periodic elements radiate from the center in different ratios by direction, so each race's body chemistry = its powers/weaknesses. (e.g., carbon-heavy humans = adaptable; silicon-heavy race = durable, slow; heavy-metal race = conductive/beam-strong.) This doubles as your **combat affinity system** — tie them together.
- **The Academy:** why are races training together? Who runs it? What's the threat that forces teamwork?
- Cast: 4–6 party members, each with a signature combo/clash role. A rival. A mentor. A villain with a sympathetic reason.
- Outline: 3 acts, ~5 chapters. Write the ending first.

## Phase 3 — Vertical slice (2–4 months)
One polished 30–45 minute chunk that looks and plays like the final game:
- Academy intro → one region → one boss with a big beam clash moment.
- Real art for that slice, basic UI, sound effects, one music track.
- This is what becomes your trailer, screenshots, and demo.

## Phase 4 — Steam page & audience (start at end of vertical slice)
- Pay the **Steam Direct fee ($100)**, set up Steamworks, tax/bank info.
- Put up a **"Coming Soon" page early** — wishlists are the #1 predictor of launch sales. Aim for 7,000–10,000+ wishlists before launch.
- Capsule art (hire a pro — it's the most important image you'll ever make), trailer (lead with a beam clash in the first 5 seconds), 5+ screenshots.
- Post clips on TikTok/YouTube Shorts/X/Reddit (r/JRPG, r/indiegaming, r/godot). Short anime-moment clips are perfect for this.
- Discord server for playtesters.
- Enter a **Steam Next Fest** with a demo.

## Phase 5 — Full production (6–18 months)
- Build content region by region, reusing systems.
- Data-driven content: skills, enemies, items in spreadsheets/JSON so adding content doesn't need new code.
- Monthly playtests. Balance pass every region.
- Save/load, settings, controller support, Steam achievements, Steam Deck check.

## Phase 6 — Launch & after
- Price: $15–25 is typical for an indie JRPG of this size.
- Launch day: all hands on bug reports, patch fast.
- Post-launch: patches, maybe a free content update, then decide on sequel/DLC.

---

## Who does what
**Claude can help with:** design docs, combat math & balance spreadsheets, writing Godot code, the story bible, dialogue drafts, quest design, Steam page copy, marketing plans, trailer scripts, playtest surveys, budgeting, a browser prototype of the combat system.

**Better done with other tools / people:**
- Pixel art & animation: Aseprite (tool) or a hired artist (itch.io, ArtStation, r/gameDevClassifieds).
- Music: a hired composer — music makes or breaks a JRPG.
- Capsule art: a professional capsule artist.
- Playtesting: real humans (Discord, friends-of-friends, Steam Playtest).

## Immediate next steps
1. Confirm scope + art style.
2. Build the combat prototype (Claude can make a browser version first so you can feel the timeline/reaction/beam-clash rules in an afternoon, then port to Godot).
3. Start the world bible: list the element-direction races.
