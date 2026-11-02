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

#### 1. Simplex Channel

* **Direction:** Unidirectional (unchanging).

* **Role:** One end is strictly the transmitter; the other is strictly the receiver.

* **Example:** Commercial broadcast radio stations (transmit only to listeners).

#### 2. Half-Duplex Channel

* **Direction:** Bi-directional, but **not simultaneous**.

* **Operation:** Uses a single physical channel where the direction of transmission can be reversed.

* **Example:** Standard telephone conversation or walkie-talkie (one party speaks while the other listens; speaking simultaneously leads to garbled signals).

#### 3. Full-Duplex Channel

* **Direction:** Simultaneous bi-directional communication.

* **Structure:** Typically composed of two logical or physical simplex channels (a forward channel and a reverse channel) linking the same two points.

* **Asymmetry:** The reverse channel may operate at a lower transmission rate if used solely for flow control/acknowledgments.

## Serial vs. Parallel Communications

Because digital messages are usually longer than a few bits, transmitting all bits simultaneously over long distances is cost-prohibitive. Thus, messages are divided into smaller segments for sequential transfer.

| Feature | Bit-Serial Transmission | Byte-Serial (Parallel) Transmission | 
| ----- | ----- | ----- | 
| **Mechanism** | Conveys a message **one bit at a time** over a single channel. | Conveys **eight bits at a time** over eight parallel channels. | 
| **Speed** | Baseline transfer rate. | Raw transfer rate is up to **8x faster**. | 
| **Cost** | Lower hardware & infrastructure cost. | Up to **8x more expensive** due to extra physical lines. | 
| **Use Case** | Long-distance communications. | Short-distance connections requiring high data rates (e.g., legacy Centronics printer interface). | 

Stopped at slide 10