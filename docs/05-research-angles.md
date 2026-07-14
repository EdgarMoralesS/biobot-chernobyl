# 5. Research and Development Angles

[← Back to README](../README.md) · [← Previous: The hybrid robot-plant proposal](04-hybrid-robot-plant-proposal.md)

## 5.1 Pure biorobotics — Experimental characterization

**Do this one first. It is cheap, it fits in under an hour of irradiator time, and it is a kill-test: if it fails, everything else in this repo is dead and you found out for the price of a houseplant.**

Searched July 2026: **no one has ever irradiated a fast-moving plant — *Mimosa pudica* or *Dionaea muscipula* — and measured its electrical signals.** The electrophysiology of both is thoroughly documented (Volkov and others); plant radiobiology is thoroughly documented (Grinberg, Vodeneev and others); **the two literatures have never been crossed.** Every radiation result available comes from wheat, tobacco or *Arabidopsis* — none of which move. (Absence of prior art can't be proven by search; this is "we looked and didn't find it.")

That leaves the experiment original along three axes at once:

1. **New organism** — a plant that is actually an actuator, not just a signal source.
2. **New measurement** — *coherence*, not amplitude. See [5.3](#53-signaling--signalnoise-modeling-under-radiation).
3. **New comparison** — head-to-head against a servomotor in the same field, same session. Nobody has published a dose-vs-functionality curve for a biological actuator against an electromechanical one.

**The experiment must measure two signals, not one.** In *Mimosa*, touch produces an **action potential** and damage produces a **variation potential** — different mechanisms. Every radiation result in the literature is about VPs; the signal an actuator needs is the AP. Measure only APs and a null result is uninterpretable; measure only VPs and you get a pretty result that is useless for robotics. See [the gap in §2](02-plants-under-radiation.md#gap-2-the-amplified-signal-may-not-be-the-one-an-actuator-needs).

**Cheap proof of concept:** *Mimosa pudica* + surface Ag/AgCl electrodes + a solenoid for repeatable mechanical stimulus + a camera for mechanical ground truth + amplifier and DAQ **outside the shielding** + a long cable + a research cobalt-60 irradiator. Dose sweep 25–400 Gy, following Grinberg et al. (2026) so the numbers are directly comparable.

Note that the rig **is** the architecture: living tissue inside the radiation zone, every semiconductor outside it, a cable in between. The proof of concept and the machine are the same object.

## 5.2 Materials — Radiotrophic fungi as shield and energy source

Melanized fungi (*Cladosporium sphaerospermum*, *Wangiella dermatitidis*, *Cryptococcus neoformans*) were found growing on the walls of Chernobyl's Reactor 4. Dadachova et al. (2007) showed that these fungi **increase in biomass and accumulate acetate faster** in radiation fields ~500× background, that gamma exposure changes melanin's electronic properties within 20–40 minutes, and that melanin-mediated electron transfer rates rise three- to four-fold. Melanized cells outgrow non-melanized ones after irradiation.

**What is *not* established: that any of this constitutes energy harvesting.** "Radiotrophy" — melanin functioning as a gamma analogue of chlorophyll, converting ionizing radiation into metabolically usable chemical energy — remains a **hypothesis**, and a contested one. What has been demonstrated is enhanced growth correlated with altered melanin electron transfer. The causal step from "melanin changes and the fungus grows better" to "the fungus is eating the gammas" has not been closed.

We flag this loudly because it is the most seductive idea in this repo and the one most likely to make us look credulous. **Do not write "a robot that feeds on radiation" as though it were settled.** The defensible version is: melanized fungi demonstrably *thrive* under chronic irradiation, which alone makes them an interesting shielding and structural material; whether they can also be an energy source is an open question — and an outstanding thing to test, since anyone who closed it would have a genuinely major result.

Combining actuating plant tissue with a melanized fungal layer therefore has one confirmed benefit (a biological material that grows rather than degrades under radiation) and one speculative one (energy harvest). Keep them separate.

## 5.3 Signaling — Signal/noise modeling under radiation

**This is the strongest angle in the repo, and the one we'd pursue first.**

Variation potentials in plants are propagating electrical signals based on ionic flow, not electronic conduction. Model the propagation of action potentials in plant tissue under radiation as a **signal-to-noise problem**: radiation increases amplitude (chronic exposure, via SKOR downregulation) but also introduces dysregulation through cross-talk between the ROS, calcium, hormonal and electrical systems.

The question nobody has answered: **is there a dose window where the amplification buys more than the dysregulation costs?** An SNR curve as a function of dose rate would be a publishable result on its own, independent of whether anyone ever builds the robot.

Two findings make this tractable rather than speculative:

- The chronic-irradiation wheat study gives a **named molecular mechanism** (SKOR potassium channel downregulation), confirmed pharmacologically — you can block SKOR in an unirradiated plant and reproduce the amplitude increase. That means the amplification is a lever you can reason about, not a black box.
- Grinberg et al. (2026) establish that **electrical signalling is the plant's most radiosensitive parameter**, responding at 25 Gy where growth and photosynthesis need 50–75 Gy. Whatever curve exists, the electrical channel is where it will show up first and most clearly.

What is missing from both: a **coherence** measurement. The existing literature reports amplitude. Nobody, as far as we can find, has reported whether the *timing, propagation velocity, and reproducibility* of the signal survive at those doses — and for a control system, coherence is the whole ballgame. An amplified but jittery signal is a worse actuator than a weak, reliable one.

## 5.4 Plant computing — Radiation-hardened biological processor

Plant cells are orders of magnitude more radiation-resistant than neurons. A "plant processor" would not run pathfinding algorithms, but could implement **tropism logic**: chemical or electrical signals that guide movement toward or away from a stimulus — exactly what is needed for basic navigation in a hostile environment. Potential connection to research on biological organoids (e.g., FinalSpark Neuroplatform).

## 5.5 Practical engineering — Robot without semiconductors

Ground-up design of a robotic system that eliminates all semiconductors from the operating zone:
- Mechanical/hydraulic chassis.
- Biological actuators (plant tissue).
- Analog sensors (photographic film, chemical indicators).
- Wired control from a safe station.
- All computational "intelligence" stays outside the radiation zone.

---

Next: [6. Related work →](06-related-work.md)
