# 6. Related Work

[← Back to README](../README.md) · [← Previous: Research angles](05-research-angles.md)

This idea doesn't exist in a vacuum. Two active research lines overlap with it directly. Neither one has been combined with the third piece — deployment in a nuclear-accident environment — as far as we've been able to find.

Every claim below was checked against the primary source (July 2026). Where the popular account of a piece of work differs from what the work actually says, we go with what the work says — even when that costs us.

## 6.1 Biohybrid robots controlled by fungal mycelium (Cornell, 2024)

**Confirmed.** Anand Kumar Mishra, Jaeseok Kim, Hannah Baghdadi, Bruce R. Johnson, Kathie T. Hodge and Robert F. Shepherd (Cornell Mechanical & Aerospace Engineering, with Jaeseok Kim at the University of Florence) published *"Sensorimotor control of robots mediated by electrophysiological measurements of fungal mycelia"* in **Science Robotics** 9(93), 28 August 2024 (DOI: [10.1126/scirobotics.adk8019](https://www.science.org/doi/10.1126/scirobotics.adk8019)).

- Mycelium of king oyster mushroom (*Pleurotus eryngii*) was used as a living electrical interface.
- The system reads the mycelium's spontaneous and light-induced action-potential-like spiking voltages, shields them from vibration and electromagnetic interference, and converts them into control signals.
- The controller is inspired by **central pattern generators** — the rhythmic neural circuits behind animal gait.
- Two robots were built: a soft pneumatic walker and a wheeled platform. Both moved in response to the mycelium's electrical activity, and UV stimulation could be used to augment the robots' gaits.

### ⚠️ The radiation angle is not Cornell's — it is journalism's

You will find it widely repeated that Cornell proposed these robots for hazardous or space environments on account of mycelium's radiation resistance. **That claim does not survive contact with the source:**

- The paper's **abstract makes no mention** of radiation, radiation resistance, hazardous sites, nuclear environments, or space. Its stated motivation is that living tissue has been held back by "limitations in life span, sensitivity to environmental factors, and stringent culture procedures," and that mycelia are an easy-to-use, robust alternative.
- **Cornell's own press release** (28 Aug 2024) mentions none of those things either. The single application Shepherd names is sensing **soil chemistry in row crops** to time fertilizer application and mitigate algal blooms.
- The strongest adjacent statement anywhere in the primary material is that mycelia are "robust" and can "thrive in harsh environments" — a general claim about fungal hardiness, not a proposal to send them into a reactor.

The framing appears to originate in **secondary science journalism** (Discover Wildlife, Interesting Engineering and others) extrapolating past the source. The full discussion section is paywalled and unchecked, so we cannot say the words appear *nowhere* — but two of the three primary sources say no, and nobody should be citing this as though Cornell endorsed the application.

**This is good news for the argument here, not bad:** it means the radiation-deployment idea is *less* trodden than the coverage suggests. Nobody at Cornell planted a flag on it. The gap described in §6.3 is wider than it looks from the outside.

## 6.2 Radiation and plant electrical signaling (Grinberg, Vodeneev et al. — IAP RAS / Lobachevsky University)

**Confirmed, and stronger than we previously claimed.** Marina Grinberg and Vladimir Vodeneev have published a sustained line of work showing that ionizing radiation acts on plants primarily *through* their signaling systems, mediated by reactive oxygen species:

- Grinberg et al., *"Effect of Increased Ionizing Radiation and Near-Null Magnetic Field on Electrical Signals of Plants,"* **Radiophysics and Quantum Electronics** 67(10), 788–798 (2025) — [DOI: 10.1007/s11141-025-10418-y](https://link.springer.com/article/10.1007/s11141-025-10418-y). Increased ionizing radiation *strengthens* electrical signals; a near-null magnetic field *weakens* them. Both are attributed to a single shared lever: ROS concentration.
- Grinberg & Vodeneev, *"The role of signaling systems of plant in responding to key astrophysical factors: increased ionizing radiation, near-null magnetic field and microgravity,"* **Planta** 261, art. 31 (11 Jan 2025) — [DOI: 10.1007/s00425-025-04610-7](https://link.springer.com/article/10.1007/s00425-025-04610-7). A review; plants perceive these factors without dedicated receptors, via primary physicochemical reactions and secondary messengers (ROS, Ca²⁺).

### ✅ The strongest result: signalling is the plant's most radiosensitive parameter

Russian science press (iz.ru, 2 July 2026) covered this work in a way that could easily be mistaken for late coverage of the 2025 papers above. It isn't. It refers to a distinct and more recent study, and it is the best citation in this repo:

> Grinberg, M., Ivanova, A., Nemtsova, Y., Pirogova, P., Skamnitskiy, D. & Vodeneev, V. — **"Comparative radiosensitivity of morphometric, physiological and signaling parameters in wheat plants."** *International Journal of Radiation Biology*, published online 23 March 2026. [DOI: 10.1080/09553002.2026.2645916](https://doi.org/10.1080/09553002.2026.2645916)

Dry wheat seeds were irradiated with 3 MeV accelerated electrons at six doses: 25, 50, 75, 100, 200, 400 Gy. The team then tracked shoot and root growth, photosynthetic parameters, pigment content, and electrical signal propagation.

**The result: electrical signal parameters differed significantly from control at the lowest dose tested — 25 Gy — while morphometric and physiological parameters only responded at 50–75 Gy.** Electrical signaling is the *most radiosensitive parameter in the plant*, ahead of growth and photosynthesis. The authors note the effect had not been previously described in radiobiology.

**Read the caveat on this caveat, though.** This is *acute* seed irradiation demonstrating **sensitivity**, which is not the same claim as chronic exposure producing **amplification** — see [the distinction drawn in §2](02-plants-under-radiation.md#an-honest-distinction-sensitivity-is-not-amplification). Both results point our way. Neither one, on its own, establishes that a radiation-soaked plant makes a *controllable* actuator. Do not merge them into a single sentence in a grant application.

## 6.3 The gap

Nobody, as far as we've found, has proposed combining:

1. Living tissue as robot actuator/sensor (demonstrated — Cornell, fungal mycelium)
2. Radiation as a signal amplifier rather than destroyer (demonstrated — Grinberg, Vodeneev et al., plant electrophysiology)
3. Deliberate deployment in a nuclear-accident environment (Chernobyl/Fukushima-style corium proximity)

Piece 1 exists and works. Piece 2 exists and is well established. **Piece 3 is genuinely unclaimed ground** — and note that the Cornell group never made the radiation claim at all (§6.1), so this is not something already half-said in someone's discussion section and waiting to be picked up. It is open.

This is a claim about absence of prior art, which by nature can't be proven by search — only "we looked and didn't find it." Treat it as our best current read of the field, not an established fact. If you find prior art, please open an issue; being wrong about this is more useful to us than being right and unaware.

---

Next: [7. Why this matters beyond nuclear →](07-why-it-matters-beyond-nuclear.md)
