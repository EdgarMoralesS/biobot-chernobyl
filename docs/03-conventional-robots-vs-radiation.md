# 3. Conventional Robots vs. Radiation: A History of Failures

[← Back to README](../README.md) · [← Previous: Plants under radiation](02-plants-under-radiation.md)

## Chernobyl (1986)

- ~60 remote-controlled robots deployed (many designed for lunar exploration or police work).
- **All failed** in the highest-radiation zones. Ionization at levels of 10,000–15,000 R/h fried every robot's control circuits.
- Batteries drained quickly and radio communications failed due to ionization.
- Valery Legasov: *"Where radiation was very high, the robot stopped being a robot — the electronics stopped working."*
- The "solution": 3,828 **"bio-robots"** (people) cleared 90% of the radioactive debris from the roof, with shifts of 90 seconds maximum.

## Fukushima (2011)

- It took **six years** for robots to capture the first images of the melted fuel.
- Previously designed robots failed due to high radiation or got stuck in confined spaces.
- Toshiba's "Little Sunfish" (the size of a loaf of bread) finally managed to enter through 5.5-inch pipes.
- The most radiation-hardened robots became unusable in as little as **one hour**.

## Why does electronics fail?

- Ionizing radiation generates electron-hole pairs in semiconductors that corrupt digital logic.
- It damages chips' crystal structures.
- It degrades plastics and insulating materials.
- It causes random bit-flips in memory.
- A KUKA robotic arm withstood only **164.55 Gy** before failing.

## The scale of the problem

| Application | Required dose |
|-----------|----------------|
| Space electronics | 100–300 Gy over 3 years |
| Robot in nuclear reactor | >500 kGy over 6 months |
| **Factor** | **~1,000x more than space** |

## Current state

- Boston Dynamics' **Spot** currently operates in Chernobyl near Reactor 4, but in tolerable radiation zones — not directly in the corium.
- The nuclear robotics market was valued at USD 13,450 million in 2024 and is expected to reach USD 24,870 million by 2032.
- Current trend: cheap, disposable commercial off-the-shelf (COTS) hardware, or specialized radiation-hardened ASIC chips (e.g., Magics, derived from the ITER project).

---

Next: [4. The hybrid robot-plant proposal →](04-hybrid-robot-plant-proposal.md)
