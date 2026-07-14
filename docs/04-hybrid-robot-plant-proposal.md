# 4. The Proposal: Hybrid Robot-Plant

[← Back to README](../README.md) · [← Previous: Conventional robots vs. radiation](03-conventional-robots-vs-radiation.md)

## Thesis

A biorobotic system based on living plant-tissue actuators could operate in extreme radiation environments where conventional electronic robots fail, because:

1. Plant actuation mechanisms (ionic flow, water movement, hydroelastic energy) **are not vulnerable** to the same failure modes as semiconductors.
2. Ionizing radiation **amplifies** electrical signals in plants instead of destroying them.
3. Plants have **DNA self-repair mechanisms** that electronics lack.
4. Rigid cell walls **prevent the spread** of cellular damage.

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
- Possible layer of radiotrophic fungi (melanin) as a biological shield that also feeds on gamma radiation.

## Advantages over conventional robots

| Aspect | Conventional robot | Plant-robot |
|---------|-------------------|--------------|
| Radiation failure mode | Bit-flips, crystal degradation, total failure | Signal amplification, gradual dysregulation |
| Self-repair | None | DNA repair, cellular regeneration |
| Power in radioactive zone | Degrading batteries | Potentially radiotrophic fungi |
| Cost | High (rad-hardened chips) | Low (biological tissue) |
| Force | High | Very low (grams) |
| Speed | High | Slow |
| Precision | High | Low, noisy |

## Honest limitations

- The force of a Venus flytrap trap is on the order of grams — it cannot move reactor debris.
- Speed is orders of magnitude lower than servomotors.
- At corium-level doses (tens of Sv/h), radiolysis of intracellular water generates free radicals faster than the plant can repair — it eventually collapses.
- Control precision degrades due to cross-talk dysregulation between signaling systems.

## Most viable application niche

**Lightweight sensing and exploration.** A small, disposable probe-type plant-robot that navigates into high-radiation zones to take readings or images with analog sensors (film camera, chemical dosimeters). Goal: outlast an equivalent electronic robot in the same zone.

---

Next: [5. Research & development angles →](05-research-angles.md)
