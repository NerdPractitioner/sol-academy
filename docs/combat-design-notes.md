# Combat design notes (derived from prototype v0.6)

Source of truth for numbers is `CONFIG` in `index.html`. This doc explains the rules.

## Core loop
Real-time tick clock (450 ms/tick), 12-tick visible timeline. Every action has a wind-up and resolves at `resolveAt`. The battle pauses whenever a hero can act or react. Heroes regain 2 chakra at the start of each of their turns.

## Resources
- **Chakra** (per hero): pays for charges, beams (per tick) and assists.
- **Resolve** (shared, 0–10, start 3): +1 when a hero takes a hit, +1 when a 3t+ attack lands, +2 on a clash win. Spent on reactions (Dive In 2, Brace 1).

## Moves
Hero: Strike (2t, 14, +3 chakra), Power Charge (4t, 34, 6 ck), Arc Beam (2–4t), Solar Lance (3–6t), Nova Cannon (4–8t), Guard (take 50%), Bodyguard (auto-absorb hits on an ally at 25% reduction), Assist, Grapple, Wait.
Enemy: Jab, Crush (targets lowest HP), Gravity Beam (4–7t).
Beams: power = base + perTick × ticks; chakra = costPerTick × ticks.

## Reactions (when an enemy hit ≥ 15 damage is about to land)
Dive In (another hero takes it, −30% dmg), Brace (−50%), Fire Early (release charge at ×0.8), Abort Charge (refund 50% chakra), Take the Hit. Reactions are never free: idle heroes lose turn time, charging heroes lose charge power. Getting hit while charging (3t+) can "shake focus" (chance = damage × 2.5%, max 85%: −25% power, +1t).

## Team mechanics
- **Assist:** infuse an ally's charge/beam with the helper's element (+16 power, 3 ck, 1t). Different infusions stack a combo bonus (+10 each). Burn (4/tick for 5t), Lattice Shell (charger takes 40% less, can't lose focus), Arc Shock (delay target 2t, clash head start).
- **Grapple:** run in and pin the target of an ally's attack. Pinned enemy is frozen and takes +25%; grappler eats 20% splash; a hit ≥ 20 breaks the grip.
- **Beam clash:** when an enemy beam is winding up, a hero can lock a beam of matching timing to it (or redirect an already-charging beam). Resolved as a 3.5 s mash-to-push contest, starting position biased by power difference. Win = strong hit plus 30% of the enemy beam thrown back; lose = take 30–80% of the enemy beam (never the full hit). Allies can Assist a clash.

## Heroes (placeholders)
Kai (human, carbon, Solar Burn), Rook (silicate, silicon, Lattice Shell, grapple/bodyguard), Vex (ferric, iron, Arc Shock, Arc Beam). Enemies: 2 Drones, Void Warden boss.

## Roadmap items not yet built
Interrupt reaction, Counter reaction, more synced-combo bonuses, enemy AI beyond fixed patterns, a proper HTML host page/build pipeline, save of tuning presets.

## Playtest questions to ask
1. Could you tell what was about to happen and when?
2. Did you ever feel forced to react, or was reacting a fun choice?
3. Was the beam clash exciting or a chore after the third time?
4. Where were you bored or confused?
5. What would you want to do that you couldn't?
