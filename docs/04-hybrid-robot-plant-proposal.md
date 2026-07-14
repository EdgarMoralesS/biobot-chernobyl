# 4. The Proposal: Hybrid Robot-Plant

[← Back to README](../README.md) · [← Previous: Conventional robots vs. radiation](03-conventional-robots-vs-radiation.md)

## Thesis

A biorobotic system based on living plant-tissue actuators could **outlast** conventional electronic robots in a radiation environment, because:

1. Plant actuation mechanisms (ionic flow, water movement, hydroelastic energy) **are not vulnerable** to the same failure modes as semiconductors.
2. Plants have **DNA self-repair mechanisms** that electronics lack. **This is the load-bearing claim** — see below.
3. Rigid cell walls **prevent the spread** of cellular damage.
4. Ionizing radiation **amplifies** rather than destroys at least one class of plant electrical signal (the variation potential). ⚠️ *Whether this transfers to the action potential — the signal an actuator would actually use — is [unverified](02-plants-under-radiation.md#gap-2-the-amplified-signal-may-not-be-the-one-an-actuator-needs).*

## The advantage is time, not dose

It is tempting to say "plants tolerate more radiation than electronics." **The numbers do not support that, and the repo would be dishonest to imply it:**

| System | Fails around |
|---|---|
| Cheap COTS electronics | ~100 Gy |
| KUKA LBR800 (optical encoder) | 164 Gy |
| Radiation-tolerant commercial parts | up to ~1,000 Gy |
| **Plant: serious acute physiological damage** | **50–100 Gy** |
| **Plant: typical seed LD50** | **100–500 Gy** |

**They fail in the same range.** There is no order-of-magnitude advantage in acute dose. A head-to-head "irradiate both until one dies" test could plausibly be **won by the servo**.

The advantage, if it exists, is not in total dose. It is in **dose rate and time**:

- Electronics accumulate damage **monotonically and irreversibly**. Every gray that lands, stays. There is no repair.
- Plants **repair**. Under low dose rate and chronic exposure, repair competes with damage and the system can reach an equilibrium rather than a death spiral. This is precisely the regime in which the Chernobyl pines have been alive for forty years.

So the defensible claim is not *"the plant survives more dose."* It is:

> **The plant survives more *time* at low dose rate, because it repairs and silicon does not.**

That single sentence reframes the target niche — see below.

## Proposed architecture

```
                        RADIATION BOUNDARY
                              ║
  [Control Station]           ║         [Biohybrid Unit]
  ┌─────────────────┐         ║         ┌──────────────────────┐
  │ All computation  │         ║         │ Zero semiconductors  │
  │ All intelligence │◄═══cable═══════►  │                      │
  │ Signal processing│         ║         │ ┌──────────────────┐ │
  │ Data storage     │         ║         │ │ Fungal mycelia    │ │
  │                  │         ║         │ │ (sensing + signal)│ │
  └─────────────────┘         ║         │ └────────┬─────────┘ │
                              ║         │ ┌────────▼─────────┐ │
                              ║         │ │ Plant tissue      │ │
                              ║         │ │ (actuation)       │ │
                              ║         │ └────────┬─────────┘ │
                              ║         │ ┌────────▼─────────┐ │
                              ║         │ │ Radiotrophic      │ │
                              ║         │ │ fungal shielding  │ │
                              ║         │ │ (energy harvest?) │ │
                              ║         │ └──────────────────┘ │
                              ║         │                      │
                              ║         │ Mechanical/hydraulic │
                              ║         │ chassis (no PCBs)    │
                              ║         │                      │
                              ║         │ Analog sensors:      │
                              ║         │ - Film camera        │
                              ║         │ - Chemical dosimeter │
                              ║         └──────────────────────┘
                              ║
```

**Key characteristics:**
- Zero semiconductors in the radiation zone.
- Wired control (not radio — ionization interferes with wireless communications).
- Biological actuators controlled by direct electrical stimulation.
- Possible layer of melanized fungi as a biological shield. ⚠️ *Melanized fungi demonstrably thrive under chronic irradiation; whether they can **harvest energy** from gamma remains an [unproven hypothesis](05-research-angles.md#52-materials--radiotrophic-fungi-as-shield-and-energy-source), not a finding.*

## Where each approach actually wins

Written honestly, including the rows where we lose.

| Aspect | Conventional robot | Plant-robot |
|---------|-------------------|--------------|
| **Acute dose tolerance** | ~100 Gy (COTS) to ~1 MGy (rad-hard ASIC) | 50–500 Gy. **We lose this row** — and against rad-hard silicon we lose it badly |
| **Damage accumulation** | Monotonic, irreversible. Every gray stays | **Repairs.** Can reach equilibrium at low dose rate |
| **Endurance at low dose rate** | Degrades until dead | **The whole case rests here** |
| Self-repair | None | DNA repair, cellular regeneration |
| Cost | High (rad-hard programme = years + millions) | Low (a Mimosa is a houseplant) |
| Force | High | **Very low — grams** |
| Speed | High | **Very slow. 0.05–1.25 cm/s signal propagation. Hard ceiling** |
| Precision | High | **Low, noisy, and coherence under dose is unmeasured** |
| Power in a radioactive zone | Degrading batteries | Melanized fungi *possibly* — unproven |

Five of nine rows go to the conventional robot, and one of the two we win is speculative. **That is the honest scorecard.** The case for this idea does not rest on a broad superiority; it rests on two rows — *damage accumulation* and *endurance at low dose rate* — plus cost. If those two do not hold up, nothing else here saves it.

## Honest limitations

- **Force.** A Venus flytrap trap closes with force on the order of grams. It cannot move reactor debris, and no amount of engineering changes that by three orders of magnitude.
- **Speed — and this is a hard ceiling, not an engineering problem.** Electrical signals in *Mimosa pudica* propagate at **3–75 cm/min**, i.e. 0.05–1.25 cm/s. A machine whose signal bus runs at a centimetre per second has latencies of seconds to tens of seconds at any useful scale. **A plant robot will never be a fast robot**, no matter how clean the signal.
- **Acute dose.** At corium-level dose rates (tens of Sv/h), radiolysis of intracellular water generates free radicals faster than the plant can repair. It collapses. **The corium is not the niche and never was** — everything dies there, plants included.
- **No dose-tolerance advantage.** See the table above. Plants and cheap electronics fail in the same acute range.
- **The actuator-signal gap.** The amplification result is about variation potentials; an actuator runs on action potentials. Unverified whether the effect transfers. This is the biggest open question in the whole proposal.
- **Precision.** Control precision degrades due to cross-talk dysregulation between signalling systems. And nobody has yet measured whether the signal stays *coherent* — the literature reports amplitude only.

## Most viable application niche

Not the corium. Not speed. Not force. **Endurance.**

**Long-duration monitoring in chronic, moderate contamination** — the environments where a conventional robot works fine on day one and is dead by month six, having accumulated dose it cannot repair. A biological system in that regime is not trying to survive a huge dose; it is trying to reach equilibrium with a small continuous one, which is a thing living tissue does and silicon cannot.

Concretely: a cheap, semiconductor-free, wired probe that sits or crawls slowly through a contaminated zone for months, sensing and actuating at low bandwidth, and **repairing itself** — where the alternative is either a rad-hard system costing orders of magnitude more, or a disposable one you keep replacing.

The measurable goal remains the same, but the axis has changed: **not "survive a bigger dose than a servo," but "still be working after the servo has stopped."**

---

Next: [5. Research & development angles →](05-research-angles.md)
