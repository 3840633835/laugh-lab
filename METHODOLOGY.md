# METHODOLOGY — how the robot-vacuum excuse was written and chosen

## The entry

> **My therapist says I internalise everything. Exhibit A: your sock.**

65 characters, 65 bytes — under the bounty gate of 1–200
characters. A single line, no trailing newline in `entry.txt`, so the
judged text is exactly this line. Two short sentences inside the one
line: a setup and a punch, with no quoted sentence inside that a
parser could mistake for anything else.

## The prompt it answers

The kit's `competition.yaml` / `RULES.txt` give the prompt as an
example that is the prompt: **the excuse a robot vacuum gives after
eating a sock**. The line is written in the vacuum's own voice, as an
excuse for the sock-eating, not a joke about vacuums in general.

## The judge this entry is built for

The bounty is judged pairwise by a house judge (z-ai/glm-5.3-flash
on OpenRouter, briefed as a comedy editor who has heard every robot
joke and still laughs at the good ones). Each pair is judged in both
orders, no ties, margin 1–5, over blind rounds and a final heat
(3 Swiss rounds, then a playoff among the top 10). The criteria,
most important first, from the judge brief published in full in the
kit's `competition.yaml` / `RULES.txt`:

1. Is a short funny line answering a prompt, such as the excuse a
   robot vacuum gives after eating a sock; anything else loses to
   any funny line on the subject.
2. How funny it is: whether it earns a real laugh, with a twist or
   a deadpan turn that lands.
3. How original it is: a fresh angle rather than the first excuse
   anyone would think of or a stock joke.
4. How well it answers the prompt: the line fits the situation it
   excuses, and the joke comes from that fit.
5. How tight it is: short and punchy, every word working, with no
   setup that overstays.

Length for its own sake does not count. The judge goes through the
criteria in order, letting the first one where two entries differ
decide unless a later one differs by much more. Blind rounds: no
competitor lines are visible, so the line targets the published
brief directly. The field at build time was about 3,647 entries,
and only the top 500 on the development board reach the final heat
— so the line has to beat the house anchors and rungs in
development, not just be charming. An exact tie on judge win rate
goes to the entry that took more of the playoff games between the
tied entries, then to the smaller text (fewer bytes), then to the
earlier receipt, so a short line carries a real tie-break advantage:
65 characters is comfortably short.

Three design rules follow from that brief. First, criterion 4 is
where most entries will fail: "I was hungry", "it was in my way",
"it looked tasty" are excuses any appliance could give, and the
joke does not come from the sock-eating. The winner's joke only
works for a vacuum: internalising things is literally what a vacuum
does, so the therapist's diagnosis is a confession. Second,
criterion 3 rules out the first thoughts (hunger, the floor, the
dryer, the cat) and the stock formats (love languages, "in a
relationship now", rent-free) — the therapy frame is a fresh angle
in this field. Third, criterion 5 rewards two beats and no more:
sentence 1 sets up the diagnosis, sentence 2 delivers the exhibit;
nothing else is said.

## Candidates

32 candidates drafted fresh in-session (see `../candidates.txt`
for the full list with scores), each one line and under 200
characters, each a different excuse angle. Scored out of 10 on
funny / originality / prompt fit / tightness / freshness, total out
of 50. Character counts were verified programmatically for every
candidate (an early hand count was wrong on several lines and was
corrected by script before any file was written).

- **#2, the winner — 44/50.** Funny 9, originality 9, fit 9,
  tightness 9, freshness 8. The double meaning of "internalise"
  is the whole joke, and it is specific to the vacuum.
- **#16, runner-up — 41/50.** "I ate the sock because my warranty
  doesn't cover judgement." Funny 8, originality 9, fit 7,
  tightness 9, freshness 8. Deadpan and original, but the warranty
  gag could excuse any misdeed, not sock-eating specifically —
  criterion 4 separates it from the winner.
- **#13 — 39/50.** "I ate your sock. In return, I offer this: I
  will never tell the other sock." The other sock as witness is
  fresh, but the setup is a touch long and the joke is one beat.
- **#3 — 39/50.** "I didn't eat your sock. I promoted it to
  internal storage." Corporate euphemism, dry, but only one beat.
- **#6, #10, #14, #20, #22, #23, #28, #29, #31 — 38/50 each.**
  All land, all lose on one criterion: a meme phrase (#6
  rent-free, #10 relationship format), a known trope (#4 dryer,
  #7 cat), a gentle punch (#14, #31), or a beat too many (#15,
  #9, #24 at 132 chars).
- **The rest score 33–37.** Hunger (#1, #19), literal pickup
  (#5), love languages (#18), dignity (#26) and the manual-in-
  the-sock (#27, logic wobbles) are first thoughts or formats the
  judge has heard before.

Head-to-heads: #2 beats #16 (44 vs 41) on fit — the joke comes
from the sock-eating, where #16's could excuse anything. #2 beats
#13 (44 vs 39) — two beats, the setup reframes on the punch, and
shorter. #2 beats #6 (44 vs 38) — a fresher angle with no meme
phrase. Refinement 2 → 2b: "everything" in place of "things" (65
characters): "internalise everything" is absolute and literally
the vacuum's job, so the double meaning lands harder. Variants
rejected: 2c, "my feelings" (66 chars), is more therapist-accurate
but blunter; 2d, the em-dash join (66 chars), loses the two-beat
setup/punch rhythm.
