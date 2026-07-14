# 5. Research and Development Angles

[← Back to README](../README.md) · [← Previous: The hybrid robot-plant proposal](04-hybrid-robot-plant-proposal.md)

## 5.1 Pure biorobotics — Experimental characterization

Test Venus flytrap actuators under increasing radiation and document at what dose they lose functionality versus an equivalent servomotor. **No one has done this direct comparative experiment**, as far as we've found — see [related work](06-related-work.md) for the closest existing efforts.

**Cheap proof of concept:** Mimosa pudica + electrodes + Arduino outside the zone + long cable + cobalt-60 source in a university lab. Documenting the biological actuator's response to different doses = original, unpublished data.

## 5.2 Materials — Radiotrophic fungi as shield and energy source

Radiotrophic fungi discovered on the walls of Chernobyl's Reactor 4 use **melanin to convert gamma radiation into chemical energy** — "photosynthesis" with gammas. Combining actuating plant tissue with a radiotrophic fungus layer: a system that not only resists radiation but **feeds on it**.

## 5.3 Signaling — Signal/noise modeling under radiation

Variation potentials in plants are propagating electrical signals based on ionic flow, not electronic conduction. Model the propagation of action potentials in plant tissue under radiation as a **signal-to-noise problem**: radiation increases amplitude but introduces dysregulation. Is there an optimal regime where the signal is amplified without losing coherence? This has potential for publication as a paper.

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
