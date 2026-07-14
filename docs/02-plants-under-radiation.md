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

## An honest distinction: sensitivity is not amplification

These two results point the same way but are not the same claim, and it's worth keeping them apart before someone else does it for us:

- The chronic study shows **amplification** — bigger VP amplitude under sustained low dose rate, with a named molecular mechanism.
- The 2026 acute study shows **sensitivity** — the electrical channel is the first thing to move as dose climbs. A parameter that responds early is not automatically a parameter that responds *usefully*: an early, strong response to radiation could just as well be read as the signal being the most easily *perturbed* part of the plant.

Both are good news for the thesis of this repo — a signaling system that radiation makes louder, and that is measurably the plant's most radiation-responsive channel, is exactly the substrate you would want to build a radiation-zone actuator on. But "radiation amplifies plant signaling, therefore plants make good robots in reactors" is a chain with a soft link in the middle, and we should say so rather than let a reviewer find it.

## Implication for control

The electrical signaling machinery is not destroyed under radiation — it is amplified. But the system becomes "noisy" and less predictable due to internal dysregulation. Analogous to controlling an electronic circuit with constant interference: it works, but with more errors and unexpected behavior. Whether there is a dose window where the amplification buys more than the dysregulation costs is, as far as we can tell, an open question — and it is the single most interesting question this repo raises. See [research angle 5.3](05-research-angles.md#53-signaling--signalnoise-modeling-under-radiation).

---

Next: [3. Conventional robots vs. radiation →](03-conventional-robots-vs-radiation.md)
