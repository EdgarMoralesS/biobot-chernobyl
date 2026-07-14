# biobot-chernobyl

**Plant biorobotics for extreme radiation environments.**

> A robot with not a single semiconductor, based on living plant-tissue actuators, capable of operating in radiation zones where no conventional electronic robot survives.

This repo is a public, dated record of the concept — released openly (MIT, see [LICENSE](LICENSE)) so that anyone can pick it up, build on it, or prove it wrong. If someone runs with this before we do, that's a win.

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
8. [References](docs/references.md) — sources cited throughout, with DOIs.

## Status

Exploratory concept. No hardware built yet. The cheapest proof of concept (Mimosa pudica + electrodes + a radiation source, documenting actuator response at increasing doses) is described in [docs/05-research-angles.md](docs/05-research-angles.md#51-pure-biorobotics--experimental-characterization).

## Sourcing

Every citation here was read against its primary source before publication, and the claims are pitched at what those sources actually support — no further. **The honest version is less exciting than the pitch, and these are the places where:**

- **Plants have no dose-tolerance advantage over electronics.** Cheap COTS electronics fail around 100 Gy; a plant takes serious acute damage at 50–100 Gy. **They fail in the same range.** A head-to-head "irradiate both until one dies" could plausibly be won by the servo. The plant's advantage, if it exists, is not dose but **dose *rate* and time** — plants repair, silicon doesn't. That reframes the target from corium proximity to **long endurance in chronic moderate contamination** ([§4](docs/04-hybrid-robot-plant-proposal.md#the-advantage-is-time-not-dose)).
- **The amplified signal may not be the signal we need.** Every radiation result in the literature — the SKOR mechanism, the amplitude increase, the 25 Gy response — is about **variation potentials** (wound signals). The signal an actuator would use is the **action potential** (the one that folds a Mimosa leaf). Different channels, different mechanism. **Nobody has checked whether the effect transfers**, and there's no a priori reason it must. This hole sits directly under the thesis ([§2](docs/02-plants-under-radiation.md)).
- **Rad-hardened silicon is genuinely good now.** Magics ships ITER robotics chips rated to ~1 MGy, *above* what a reactor-interior robot needs. A plant robot does **not** win on radiation hardness; the semiconductor industry has largely solved that ([§3](docs/03-conventional-robots-vs-radiation.md#what-this-means-for-our-argument)).
- **Cornell never proposed fungal robots for radioactive sites.** Neither the *Science Robotics* abstract nor Cornell's press release mentions radiation, nuclear, or hazardous sites — the only application named is agricultural soil chemistry. The radiation framing came from secondary science journalism. This *widens* the gap this repo points at rather than narrowing it ([§6.1](docs/06-related-work.md)).
- **"Radiotrophic" fungi are not proven to eat gamma rays.** Melanized fungi demonstrably *thrive* under chronic irradiation — that much is solid. Energy *harvesting* from gamma remains an unclosed hypothesis, flagged as such rather than used as a load-bearing assumption ([§5.2](docs/05-research-angles.md)).
- **Radiation tolerance is species-specific.** Scots pine, the obvious Chernobyl poster child, is actually one of the *most* radiosensitive plants known — an ICRP reference organism for precisely that reason ([§2](docs/02-plants-under-radiation.md)).

**The strongest evidence for the thesis** is Grinberg et al., *International Journal of Radiation Biology* (March 2026): in wheat, electrical signalling is the **most radiosensitive parameter in the plant**, responding at 25 Gy where growth and photosynthesis only respond at 50–75 Gy ([§6.2](docs/06-related-work.md)).

**The strongest argument against it** is the first bullet above. We think the time-not-dose reframing survives it. We could be wrong, and the experiment in [§5.1](docs/05-research-angles.md#51-pure-biorobotics--experimental-characterization) is designed to find out cheaply rather than expensively.

If you find a citation that doesn't survive contact with its source, open an issue.

## Contributing

This is an open idea, released so someone can take it further — whether that's us or not. If you work in biohybrid robotics, radiation biology, nuclear decommissioning, or mycology and find this interesting: open an issue, fork it, or just run with it.

**The single most valuable contribution is access to a research-grade cobalt-60 irradiator** (25–400 Gy, dose-controllable — *not* an industrial food-sterilisation plant, which runs 7–16 kGy and is a hundred times too hot). The experiment needs **under an hour of machine time**.

It would be the first time anyone has irradiated a plant that actually moves. As far as we can find, **nobody has ever put a *Mimosa pudica* or a Venus flytrap in a gamma field and recorded its electrical signals** — the electrophysiology literature and the radiobiology literature have simply never been crossed. Everything we know about radiation and plant signalling comes from wheat, tobacco and *Arabidopsis*, none of which move.

Three things would be measured for the first time:

1. **Coherence, not amplitude** — latency, jitter, propagation velocity. The literature reports how *big* the signal gets under radiation. Nobody has reported whether it still arrives *on time and reliably*, which is the only thing that matters for a control system.
2. **Whether the effect reaches the action potential** — the signal an actuator actually runs on, as opposed to the variation potential every existing study measures.
3. **A head-to-head dose-vs-functionality curve** against a servomotor in the same field, same session.

If you have a beam and an hour, we have the protocol.

## License

[MIT](LICENSE) — do whatever you want with it, just keep the copyright notice.

---

*"A robot that recharges its biological batteries from the same environment that destroys conventional robots."*

**Origin:** concept and research direction by Edgar, developed with Claude (Anthropic) for search, synthesis, and angle development. July 2026.
