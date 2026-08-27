# BYRSA — read-only fork provenance

This fork is **read-only** for the BYRSA workspace. No code in this repository
is modified; this file is the entire diff.

The BYRSA workspace forks five repositories on the instruction to *"pin the
version, mine one idea each"*. This records the pin and the idea, so a later
session can tell what was borrowed and check it against the source.

| | |
|---|---|
| **Pinned commit** | `daef9de823119cf930237dfadc1ac4f98234361f` (`daef9de`, 2019-05-15) |
| **Idea mined** | **The bounding-bot roster, and the reporting shape.** Hanabi's roster runs from BlindBot (plays randomly) to CheatBot (deliberately sees hidden information to establish an upper bound). Neither is a \"good player\" — both are measuring devices. BYRSA's roster is built on that principle: NullBot is the floor, MaxBot the ceiling, CheatBot the yardstick, and the gap between CheatBot and BeliefBot is the value of hidden information in BYRSA. The report shape — a table of bot x player-count, one number per cell, no prose in the table — is also Hanabi's. |
| **Where it landed** | `byrsa-sim/byrsa_sim/agents/` Tiers 0–3, and every table in `byrsa-sim/reports/` |
| **Cited in** | `01` §1 and §4; `02` §6 |

## Why pinning matters

A borrowed idea that drifts with upstream is an unrecorded dependency. The BYRSA
corpus requires every finding to carry a git SHA and seed range; a technique
borrowed from a moving target would break that chain. This fork is not tracked
for updates — if the idea needs revisiting, it is revisited against **this**
commit.

## What was NOT taken

No rule from any bundled game, ever. BYRSA's rules live in exactly one place:
A2 of the corpus, implemented by `byrsa-sim/byrsa_sim/rules.py`. What is
borrowed here is *methodology* — how to structure a bot roster, how to shape a
report, how to parameterise a strategy — never a mechanic.
