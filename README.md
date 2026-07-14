# biobot-chernobyl

**Plant biorobotics for extreme radiation environments.**

> A robot with not a single semiconductor, based on living plant-tissue actuators, capable of operating in radiation zones where no conventional electronic robot survives.

This repo is a public, dated record of the concept — released openly (CC0, see [LICENSE](LICENSE)) so that anyone can pick it up, build on it, or prove it wrong. If someone runs with this before we do, that's a win.

## Thesis

Conventional electronic robots fail in high-radiation environments (Chernobyl, Fukushima) because ionizing radiation destroys semiconductor logic. Plants don't have semiconductors — they signal electrically through ionic flow, and there's emerging evidence that radiation *amplifies* that signaling instead of destroying it. A robot built on living plant (or fungal) tissue as its actuator/sensor layer might survive, or at least outlast, environments where silicon dies.

## Contents

1. [Plant motion control](docs/01-plant-motion-control.md) — how plants already move via electrical signaling (Venus flytrap, Mimosa), and how researchers control it externally.
2. [Plants under Chernobyl-level radiation](docs/02-plants-under-radiation.md) — survival mechanisms, and the key finding that radiation amplifies plant electrical signals rather than destroying them.
3. [Conventional robots vs. radiation](docs/03-conventional-robots-vs-radiation.md) — why every electronic robot sent into Chernobyl and Fukushima eventually failed.
4. [The hybrid robot-plant proposal](docs/04-hybrid-robot-plant-proposal.md) — architecture, advantages, honest limitations, and the most viable application niche.
5. [Research & development angles](docs/05-research-angles.md) — five concrete directions, from cheap proof-of-concept experiments to publishable signal/noise modeling.
6. [Related work](docs/06-related-work.md) — existing research that overlaps with this idea (Cornell's fungal-mycelium robots, Russian radiobiology on plant signaling under radiation), and the gap nobody has filled yet.
7. [Why this matters beyond nuclear](docs/07-why-it-matters-beyond-nuclear.md) — space, fusion maintenance, and other domains with the same semiconductor-vs-radiation problem.
8. [References](docs/references.md) — sources cited throughout.

## Status

Exploratory concept. No hardware built yet. The cheapest proof of concept (Mimosa pudica + electrodes + a radiation source, documenting actuator response at increasing doses) is described in [docs/05-research-angles.md](docs/05-research-angles.md#51-pure-biorobotics--experimental-characterization).

## Contributing

This is an open idea, released so someone can take it further — whether that's us or not. If you work in biohybrid robotics, radiation biology, nuclear decommissioning, or mycology and find this interesting: open an issue, fork it, or just run with it.

The single most valuable near-term contribution would be access to a controlled radiation source (a university cobalt-60 or similar) to run the Phase 0 characterization experiment described in [docs/05-research-angles.md](docs/05-research-angles.md#51-pure-biorobotics--experimental-characterization) — nobody has published a direct dose-vs-functionality comparison between a plant/fungal actuator and an equivalent servomotor.

## License

[CC0 1.0](LICENSE) — public domain. No permission needed, no attribution required. Take it and run.

---

*"A robot that recharges its biological batteries from the same environment that destroys conventional robots."*

**Origin:** concept and research direction by Edgar, developed with Claude (Anthropic) for search, synthesis, and angle development. July 2026.
