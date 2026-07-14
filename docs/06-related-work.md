# 6. Related Work

[← Back to README](../README.md) · [← Previous: Research angles](05-research-angles.md)

This idea doesn't exist in a vacuum. Two active research lines overlap with it directly. Neither one has been combined with the third piece — deployment in a nuclear-accident environment — as far as we've been able to find. Claims below are fact-checked against primary and secondary sources; caveats are noted where the sourcing is weaker than the headline claim.

## 6.1 Biohybrid robots controlled by fungal mycelium (Cornell, 2024)

**Confirmed.** Anand Mishra (first author), under Prof. Rob Shepherd (Cornell Mechanical & Aerospace Engineering), with University of Florence collaborators, published *"Sensorimotor control of robots mediated by electrophysiological measurements of fungal mycelia"* in **Science Robotics**, August 2024 (DOI: [10.1126/scirobotics.adk8019](https://www.science.org/doi/10.1126/scirobotics.adk8019)).

- Mycelium of king oyster mushroom (*Pleurotus eryngii*) was used as a living electrical interface.
- The system reads the mycelium's spontaneous and light-induced electrophysiological spikes, filters them, and converts them into control signals.
- Two robots were built: a soft pneumatic walker (five-pointed, star/spider-shaped) and a wheeled platform. Both moved in response to the mycelium's electrical activity, including light-triggered responses.

**Caveat on the radiation/hazard-site angle:** Cornell's own press release ([news.cornell.edu](https://news.cornell.edu/stories/2024/08/biohybrid-robots-controlled-electrical-impulses-mushrooms)) does **not** mention radiation resistance or hazardous-site deployment — it frames near-term applications around agricultural soil chemistry sensing. The claim that mycelium's radiation resistance makes these robots candidates for hazardous or space environments comes from secondary science journalism (e.g., Discover Wildlife, Interesting Engineering) that appears to paraphrase the paper's discussion section. We could not access the full paper text (paywalled) to confirm the exact wording. **Treat "Cornell explicitly proposed this for radioactive sites" as unconfirmed** until someone checks the primary source directly.

## 6.2 Radiation amplifies plant electrical signaling (Institute of Applied Physics, Russian Academy of Sciences)

**Confirmed, but check for duplication.** Marina Grinberg (IAP RAS, with co-author Vodeneev, a regular collaborator on plant electrophysiology) has published on how increased ionizing radiation strengthens rather than weakens electrical signaling in plants, via a hormesis effect mediated by reactive oxygen species (ROS):

- Grinberg et al., *"Effect of Increased Ionizing Radiation and Near-Null Magnetic Field on Electrical Signals of Plants,"* *Radiophysics and Quantum Electronics* (2025) — already cited in [docs/02-plants-under-radiation.md](02-plants-under-radiation.md).
- Grinberg & Vodeneev, *"The role of signaling systems of plants in responding to key astrophysical factors,"* *Planta* (2025).
- Russian science press (iz.ru, dated 2026-07-02) covered what's described as a study published "about two weeks" prior, with the same core finding (low-dose radiation → hormesis → amplified electrical signaling via ROS) and a stated application angle toward space biology (breeding radiation-adapted plant varieties).

**Caveat:** it's unclear whether the July 2026 press coverage refers to a genuinely new paper or is late/secondary coverage of the 2025 work already cited. **Before presenting this as two separate findings, find the exact DOI of the July 2026 piece and confirm it's distinct from the 2025 papers.**

## 6.3 The gap

Nobody, as far as we've found, has proposed combining:

1. Living tissue as robot actuator/sensor (demonstrated — Cornell, fungal mycelium)
2. Radiation as a signal amplifier rather than destroyer (demonstrated — Grinberg et al., plant electrophysiology)
3. Deliberate deployment in a nuclear-accident environment (Chernobyl/Fukushima-style corium proximity)

This is a claim about absence of prior art, which by nature can't be proven by search — only "we looked and didn't find it." Treat it as our best current read of the field, not an established fact.

---

Next: [7. Why this matters beyond nuclear →](07-why-it-matters-beyond-nuclear.md)
