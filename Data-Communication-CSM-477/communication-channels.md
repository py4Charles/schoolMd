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

## Bit-Serial vs. Parallel Transmission

As another example, it is common practice to use a **16-bit-wide data bus** to transfer data between a microprocessor and memory chips.

- This provides the equivalent of **16 parallel channels**.
- On the other hand, when communicating with a timesharing system over a modem, only a **single channel** is available, and **bit-serial transmission** is required.

This figure illustrates these ideas:

- Each bit represents a part of the message.
- The individual bits are then reassembled at the destination to compose the message.

In general, **one channel will pass only one bit at a time**.

- Thus, **bit-serial transmission** is necessary in data communications if only a single channel is available.
- Bit-serial transmission is normally just called **serial transmission** and is the chosen communications method in many computer peripherals.