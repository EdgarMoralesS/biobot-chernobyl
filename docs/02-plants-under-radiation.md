# 2. Plants Under Chernobyl-Level Radiation

[← Back to README](../README.md) · [← Previous: Plant motion control](01-plant-motion-control.md)

## Survival where animals cannot

- Plants have continued growing even in the most contaminated areas of the Chernobyl Exclusion Zone for nearly 40 years.
- Unlike animals, plants do not develop metastatic cancer. Every plant cell is locked inside a rigid cellulose wall, so cells cannot detach and migrate; plants also lack a circulatory system to carry them. Plant tumours therefore stay put and are rarely lethal (Doonan & Sablowski, *"Walls around tumours — why plants do not develop cancer,"* *Nature Reviews Cancer*, 2010).
- Chernobyl *Arabidopsis* populations pass heritable resistance to their progeny, but the mechanism reported is **DNA hypermethylation and genome stabilization** — a lockdown response — rather than upregulated DNA repair (Kovalchuk et al., *Plant Physiology*, 2004).
- Endemic plant communities have adapted to survive in radioactively contaminated soil.

> **Radiation tolerance is not uniform across plants, and the obvious poster child is the wrong one.** It is tempting to point at the pines of the Exclusion Zone, but *Pinus sylvestris* is in fact one of the **most radiosensitive** plants known — the ICRP uses it as a reference organism for radiation protection of biota precisely for that reason (its large genome makes it a big target). Studies of Chernobyl pine populations in the remote period find persistent oxidative stress, cytogenetic abnormalities, abortive seeds, suppressed radial growth and loss of apical dominance, *alongside* genuine adaptive signatures: sustained redox and ion-balance control, transcriptomic and epigenomic shifts. The accurate summary is **partial radioadaptation without escaping the damage** — not the emergence of a radiation-proof conifer. Species selection matters enormously for anything built on this. See Geras'kin et al. in [references](references.md).

## Exception: acute initial exposure

The pines closest to the Chernobyl reactor suffered radiation poisoning — their needles turned red and the trees died (the famous "Red Forest"). Acute initial exposure is lethal even for plants. Survival occurs under chronic, lower-intensity exposure.

## Effect on electrical signaling

Key finding: **ionizing radiation does not destroy plant electrical signaling. The signal is the part of the plant that responds most strongly to it.**

- **Chronic irradiation, wheat** (*Triticum aestivum*): Plants grown under chronic irradiation (dose rate 31.3 μGy/h, accumulated dose ~11.3 mGy) showed an **increase in amplitude** of variation potentials (VPs). The identified mechanism was a **decrease in expression of the SKOR potassium channel gene** — and blocking that channel pharmacologically in *control* plants reproduced the same amplitude increase, which is what makes the mechanism credible rather than correlational. Notably, expression of the calcium (TPC1), anion (ALMT1, CLC1), other potassium (AKT1), H⁺-ATPase and NADPH-oxidase genes did *not* change. SKOR was the specific lever. (*Biochemistry (Moscow), Suppl. Series A*, 2024.)
- **Acute irradiation, wheat — the strongest result we have** (Grinberg et al., *International Journal of Radiation Biology*, March 2026): Dry seeds were irradiated with 3 MeV accelerated electrons at 25, 50, 75, 100, 200 and 400 Gy. **Electrical signal parameters differed significantly from control at the lowest dose tested — 25 Gy — while morphometric and physiological parameters only crossed threshold at 50–75 Gy.** The conclusion is that electrical signaling is the *most radiosensitive parameter in the plant*, more so than growth or photosynthesis.
- **Cross-talk between systems**: The influence of ionizing radiation on physiological processes occurs mainly through **dysregulation of activity**, due to cross-talk between signaling systems: ROS, calcium, hormonal, and electrical.

## Two honest gaps in the evidence chain

The results above point our way. But between "radiation amplifies plant electrical signalling" and "therefore plants make good actuators in a reactor" there are two soft links, and we would rather name them than have a reviewer find them.

### Gap 1: sensitivity is not amplification

- The chronic study shows **amplification** — bigger VP amplitude under sustained low dose rate, with a named molecular mechanism (SKOR).
- The 2026 acute study shows **sensitivity** — the electrical channel is the first thing to move as dose climbs. A parameter that responds early is not automatically a parameter that responds *usefully*. An early, strong response to radiation could just as well be read as the signal being the most easily **perturbed** part of the plant.

### Gap 2: the amplified signal may not be the one an actuator needs

This one is sharper, and we have not seen it discussed anywhere.

Plants have (at least) two distinct long-distance electrical signals, with different triggers and different mechanisms:

| Signal | Triggered by | Role |
|---|---|---|
| **Action potential (AP)** | Non-damaging stimuli — touch, cooling | The fast, all-or-nothing signal. **In *Mimosa pudica* this is what collapses the pulvinus and moves the leaf.** |
| **Variation potential (VP)** | Damaging stimuli — wounding, heat | A slower, graded wound signal |

**Every radiation result cited above — the SKOR mechanism, the amplitude increase, the 25 Gy response — is about variation potentials.**

But the signal a robot would use to *issue a command* is the action potential. It is the AP that fires when you touch a Mimosa and the leaf folds. **Nobody has checked whether radiation's effect on VPs transfers to APs at all**, and there is no a priori reason it must: they run on different channels.

So the honest state of the evidence is: **radiation is known to amplify a plant signal. It is not known to amplify the plant signal we would actually build on.** That is a real hole, it sits directly under the thesis, and closing it is cheap — see [research angle 5.1](05-research-angles.md#51-pure-biorobotics--experimental-characterization).

Related: as far as we can find, **no one has ever irradiated a fast-moving plant — *Mimosa pudica* or *Dionaea muscipula* — and measured its electrical signals at all.** The electrophysiology of both is well studied, and plant radiobiology is well studied, but the two literatures have not been crossed. Every radiation result we have comes from wheat, tobacco or *Arabidopsis* — none of which move.

## Implication for control

The electrical signaling machinery is not destroyed under radiation — it is amplified. But the system becomes "noisy" and less predictable due to internal dysregulation. Analogous to controlling an electronic circuit with constant interference: it works, but with more errors and unexpected behavior. Whether there is a dose window where the amplification buys more than the dysregulation costs is, as far as we can tell, an open question — and it is the single most interesting question this repo raises. See [research angle 5.3](05-research-angles.md#53-signaling--signalnoise-modeling-under-radiation).

---

Next: [3. Conventional robots vs. radiation →](03-conventional-robots-vs-radiation.md)
