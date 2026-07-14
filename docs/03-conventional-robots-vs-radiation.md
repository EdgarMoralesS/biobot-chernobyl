# 3. Conventional Robots vs. Radiation: A History of Failures

[← Back to README](../README.md) · [← Previous: Plants under radiation](02-plants-under-radiation.md)

## Chernobyl (1986)

- ~60 remote-controlled robots deployed (many designed for lunar exploration or police work).
- **All failed** in the highest-radiation zones. Reported roof dose rates vary by location and source, from ~10,000 R/h up to 30,000 R/h in the worst spots — enough to destroy every robot's control circuits.
- Batteries drained quickly and radio communications failed due to ionization.
- Valery Legasov, first deputy director of the Kurchatov Institute, 1987: *"We learned that robots are not the great remedy for everything. Where there was very high radiation, the robot ceased to be a robot — the electronics quit working."*
- The "solution": 3,828 **"bio-robots"** (people) cleared 90% of the radioactive debris from the roof, in shifts commonly cited at 90 seconds and capped between roughly 40 and 120 seconds depending on the sector's dose rate.

## Fukushima (2011)

- It took **six years** for robots to capture the first images of the melted fuel. Toshiba's "Little Sunfish" — a submersible the size of a loaf of bread, with five propellers, two cameras and a dosimeter — finally reached the Unit 3 primary containment vessel in July 2017 and imaged lava-like fuel debris.
- Earlier robots failed from radiation or got stuck in confined spaces. Radiation inside the reactor was estimated at **650 Sv/h** at one spot.
- A cleaning robot sent in ahead of TEPCO's "Scorpion" probe was rated for a **1,000 Sv** cumulative dose and planned for a 10-hour mission. **Two of its cameras were dead after two hours** and it had to turn back. The Scorpion itself aborted shortly after, unable to move through the debris.

The relevant lesson is not merely that the electronics died — it is that they died *on a schedule short enough to make the mission fail*. A robot that survives two hours cannot do six years of exploratory work.

## Why does electronics fail?

- Ionizing radiation generates electron-hole pairs in semiconductors that corrupt digital logic.
- It damages chips' crystal structures.
- It degrades plastics and insulating materials.
- It causes random bit-flips in memory.
- Under a 20 TBq cobalt-60 source, a KUKA LBR800 arm stopped operating after a cumulative **164.55 ± 1.09 Gy** to its end effector, over 16.8 hours. The failing component was a single **optical encoder**.

> **We are obliged to state what the KUKA source actually concludes, because it is not what this number is usually used to imply.** Zhang et al. (*Frontiers in Robotics and AI*, 2020) read their own result as *encouraging*: the arm "displayed significant radiation tolerance," the failure was localized to one component rather than a cascading electronics death, KUKA's own software detected it and locked the arm into a safe state, and the authors conclude that force-torque arms are "potentially viable for nuclear waste processing applications." The honest framing is not "electronics are pathetically fragile" — it is that **164 Gy is three to four orders of magnitude short of the >500 kGy a reactor-interior robot would need**, and that the gap is one of scale, not of principle. Rad-hardened parts exist and are getting better (see below). Our argument has to beat that trajectory, not a strawman.

## The scale of the problem

| Application | Required dose |
|-----------|----------------|
| Space electronics | 100–300 Gy over 3 years |
| Robot in nuclear reactor | >500 kGy over 6 months |
| **Factor** | **~1,000x more than space** |

## Current state

- Boston Dynamics' **Spot** was trialled at Chernobyl near Reactor 4 in **2020**, carrying a collimated radiation sensor for the UK Atomic Energy Authority and Bristol, to build radiation maps inside the New Safe Confinement. It worked in "medium level contaminated" space — areas where humans can already go, just at unnecessary risk. It has not been near the corium, and at the time of that trial the researchers had not yet established Spot's radiation tolerance limit at all. This was a one-off deployment, not an ongoing operation.
- **Radiation-hardened silicon is the state of the art, and it is good.** Magics Technologies (a KU Leuven / SCK CEN spin-off) supplies rad-hard ASICs for ITER robotics — motion control, position sensing, imaging — rated to roughly **1 MGy (100 Mrad) TID**, with single-event-effect immunity above LET 62.5 MeV·cm²/mg. That is *above* the >500 kGy a reactor-interior robot needs. The other live trend is the opposite bet: cheap, disposable commercial off-the-shelf (COTS) hardware you simply expect to lose.
- The nuclear robotics market is sometimes quoted at USD 13,450M (2024) → USD 24,870M (2032). **Treat that figure with suspicion:** it comes from a single market-research vendor, and other firms put the 2024 market anywhere from ~USD 1,600M to 13,500M — an order of magnitude of disagreement. There is a real and growing market; the specific number is not a fact.

## What this means for our argument

The Chernobyl and Fukushima failure histories are real and damning, but they describe **1986 and 2011 electronics**. Anyone making the case for a biological alternative in 2026 has to reckon with the fact that the semiconductor industry has already solved a large part of this problem: chips rated to 1 MGy exist and fly in ITER. A plant-based robot does not win on radiation hardness alone.

Where it could still win is on the axes rad-hard silicon does *not* address: **cost** (a rad-hard ASIC programme is a multi-year, multi-million-euro undertaking; a Mimosa is a houseplant), **disposability**, **self-repair**, and the possibility of a system that *harvests* energy from the environment that is destroying everything else. That is a narrower and more defensible claim than "electronics can't do this," and it is the one we should be making.

---

Next: [4. The hybrid robot-plant proposal →](04-hybrid-robot-plant-proposal.md)
