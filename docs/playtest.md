# Playtest kit (Combat Lab 1.6, round 1)

Goal: 3–5 people who aren't friends-being-nice play one fight (5–10 min), then answer 5 questions.

## How it works
- The game is `index.html`, hosted on GitHub Pages: https://nerdpractitioner.github.io/sol-academy/
- After each fight, a **Give feedback** button appears under the game. It opens a Google Form with a stats line already filled in (fights, wins, minutes, mouse or touch, which moves/reactions they used, clash wins and taps).
- The button stays hidden until `PLAYTEST.feedbackUrl` is set at the top of the script in `index.html`.
- Stats are counted per build. Bump `PLAYTEST.build` for each new round so numbers don't mix.

## One-time setup: the Google Form (about 10 minutes)
1. Go to forms.google.com → Blank form. Title: "Combat Lab playtest".
2. Add these questions (paragraph answers unless noted):
   1. Could you tell what was about to happen, and when?
   2. Did you ever feel forced to react, or was reacting a fun choice?
   3. Was the beam clash exciting, or a chore after the third time? (If you never got one, say so.)
   4. Where were you bored or confused?
   5. What did you want to do that you couldn't?
   6. Overall, how much did you enjoy it? (Linear scale 1–5)
   7. **Stats** (short answer). Description: "Filled in automatically, please leave as is."
3. Click the three-dot menu (⋮) → **Get pre-filled link**. Type the word `STATS` into the Stats answer, leave everything else blank, click **Get link** → **Copy link**.
4. Paste that link into `PLAYTEST.feedbackUrl` in `index.html` (or give it to Claude to do).
5. In the form's Responses tab, you can link a Google Sheet to see all answers in one table.

## Message to send testers
> Hey! I'm making a space-academy JRPG and I'm testing the combat system before anything else. Would you play one fight (5–10 minutes, runs in your browser) and answer 5 quick questions after? Honest is way more useful than nice. "I was bored" is great feedback.
> https://nerdpractitioner.github.io/sol-academy/
> Works best on a computer. There's a feedback button under the game when the fight ends.

## Tips
- Don't explain the game first. Confusion is the data you want.
- If you can watch someone play (screen share), note where they hesitate. Say nothing.
- After round 1, write the top 3 problems in `docs/project-tracker.md` before changing anything.
