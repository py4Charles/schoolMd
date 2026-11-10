# Data Communications Notes

## Fundamental Rules & Objectives

### Theoretical Constraints

As a general rule, the maximum permissible transmission rate of a message increases with signal power and decreases with channel noise.

It is the ultimate aim of any communications system to provide the **highest possible transmission rate** at the **lowest possible power** and with the **least possible noise**.

## Communications Channels

* **Definition:** A communications channel is a pathway over which information can be conveyed.

  * **Physical Media:** Guided wires (e.g., copper cables, optical fibers).

  * **Radiated Media:** Unguided wireless signals (e.g., radio, laser, infrared).

* **Source & Destination:** Information sent through a channel originates from a single **source** and is delivered to a **destination**.

  * Although information originates from one source, there may be multiple destinations depending on the number of receiving stations and the signal energy.

* **Data Representation & Encapsulation:**

  * In a digital channel, information is represented as individual bits.

  * Bits are encapsulated into multi-bit units (e.g., a **byte** consists of 8 bits).

  * Collections of bytes can be further grouped into higher-level units like **frames** or **packets** to facilitate handling in complex networks.

### Transmission Modes (Directionality)

```
Simplex:       [Tx]  ---------------------->  [Rx]
Half-Duplex:   [Tx/Rx]  <=================>  [Tx/Rx]  (One direction at a time)
Full-Duplex:   [Tx/Rx]  <----------------->  [Tx/Rx]  (Simultaneous bi-directional)
                        ----------------->

```