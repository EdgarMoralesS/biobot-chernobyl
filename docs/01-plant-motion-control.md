# 1. Motion Control in Plants

[← Back to README](../README.md)

Plants are not static. They possess electrical signaling systems based on action potentials (analogous to nerve signals) that coordinate rapid movements in species such as *Dionaea muscipula* (Venus flytrap) and *Mimosa pudica*.

## Basic mechanism

- Stimulating the sensory hairs of a Venus flytrap triggers **action potentials** that fire water movement between tissue layers, releasing stored hydroelastic energy.
- The trap requires two stimulations within ~30 seconds to close — a "mechanical memory" mechanism that conserves energy.
- Electrical signaling in plants is based on voltage differences between the cell interior and exterior, mediated by rapid ionic flow across membranes.

## Demonstrated external control

| Method | Researchers | Description |
|--------|---------------|-------------|
| **Direct electrical stimulation** | Wenlong Li et al., Nanyang Technological University, Singapore | Conformable electrodes attached to Venus flytrap leaves force closure without touching sensory hairs. Response time tunable to ~1.3 s at a power input of only 10⁻⁵ W; controllable from a smartphone; the actuator can be mounted on a robotic hand to grasp thin wires and catch moving objects. Published as *"An on-demand plant-based actuator created using conformable electrodes,"* *Nature Electronics* 4, 134–142 (2021). |
| **Cyborg Botany / Elowan** | Harpreet Sareen & Pattie Maes, MIT Media Lab | Electrodes embedded in a plant's leaves and stems pick up its bioelectrical responses to light and drive a wheeled robot toward or away from the source. **Note the direction:** Elowan is plant→robot. Sareen's work also describes *phytoactuators* (software → electrode → plant movement), but we have not been able to anchor that specific project to a primary source — see [references](references.md). |
| **Plant optogenetics** | Rainer Hedrich et al., JMU Würzburg, Germany | The light-gated anion channel GtACR1 is expressed in tobacco guard cells; blue/green light pulses depolarize the membrane by 60–80 mV, opening voltage-gated K⁺ channels and closing the stomata. Published as *"Optogenetic control of the guard cell membrane potential and stomatal movement by the light-gated anion channel GtACR1,"* *Science Advances* (2021). |
| **Multi-electrode mapping** | Eleni Stavrinidou et al., Linköping University (with Columbia) | A conformable ~30-electrode array films the *propagation* of the Venus flytrap action potential across the lobe — the readout side of the same interface. *Science Advances* (2023). |
| **Directed illumination** | Controlled agriculture (indoor farming) | Local changes in light intensity and spectrum induce bending movements in plants when irradiated from different directions over time. |

## Research in plant kinematics

A study on peas (*Pisum sativum*) using 3D kinematic analysis showed that plant movement is not rigidly programmed — it is adaptive, flexible, anticipatory, and goal-directed. Plants exhibit a motor-precision mechanism similar to animals, meeting the preconditions for cognitively guided behavior.

---

Next: [2. Plants under Chernobyl-level radiation →](02-plants-under-radiation.md)
