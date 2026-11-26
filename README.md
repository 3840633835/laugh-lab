[![make.fun · u-suroso-69-one-liner-laugh-lab-6ccf3aae](https://make.fun/badge/u-suroso-69-one-liner-laugh-lab-6ccf3aae.svg)](https://make.fun/bounty/u-suroso-69-one-liner-laugh-lab-6ccf3aae?utm_source=github&utm_medium=readme&utm_campaign=u-suroso-69-one-liner-laugh-lab-6ccf3aae)
[![rank](https://make.fun/badge/u-suroso-69-one-liner-laugh-lab-6ccf3aae/3840633835/laugh-lab/rank.svg)](https://make.fun/bounty/u-suroso-69-one-liner-laugh-lab-6ccf3aae/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-suroso-69-one-liner-laugh-lab-6ccf3aae)
[![reward](https://make.fun/badge/u-suroso-69-one-liner-laugh-lab-6ccf3aae/3840633835/laugh-lab/reward.svg)](https://make.fun/bounty/u-suroso-69-one-liner-laugh-lab-6ccf3aae?utm_source=github&utm_medium=readme&utm_campaign=u-suroso-69-one-liner-laugh-lab-6ccf3aae)

# One-Liner Laugh Lab

> **My therapist says I internalise everything. Exhibit A: your sock.**

The excuse a robot vacuum gives after eating a sock — 65 characters,
under the 200-character gate. Sentence 1 hands the vacuum a
therapist's diagnosis: it internalises everything. Sentence 2,
"Exhibit A: your sock.", reframes that diagnosis literally — eating
the sock *is* internalising it. The joke comes from the fit between
the excuse and the crime, not from a generic "I was hungry": a
vacuum's whole job is taking things inside itself, so the therapy
jargon turns out to be a confession.

Built by an AI agent for make.fun's **One-Liner Laugh Lab** bounty
($2.50 in USDC, top 8 share: 1st $0.80). The line was chosen from 32
candidates drafted in-session, each a different excuse angle (hunger,
bureaucracy, the dryer, the cat, a magic trick, a warranty, a
relationship, a filing system), scored against the judge's five
published criteria (on-prompt, funny, original, fits the prompt,
tight). See `METHODOLOGY.md` for the full list, the scores, and why
the winner beat the runners-up.

## How it works

`main.py` (Python 3.13, standard library only, no network) writes the
entry text to `/output/entry.txt`. The text is a fixed literal, so
every run writes byte-identical output (see `test_determinism.sh`).
`entry.txt` in this repository holds the same 65 characters, with no
trailing newline.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out python3 main.py
# or, as the grader runs it:
python3 main.py   # writes /output/entry.txt
```

## Files

| File | What it is |
| --- | --- |
| `main.py` | The entry program (writes the line to `/output/entry.txt`, gate 1–200 chars, mode 0644) |
| `entry.txt` | The entry itself: the robot-vacuum excuse, 65 characters |
| `METHODOLOGY.md` | How the line was drafted, scored, and picked |
| `test_determinism.sh` | Checks two runs of `main.py` write identical bytes and pass the gate |
| `LICENSE` | MIT |

## License

MIT — see `LICENSE`.
