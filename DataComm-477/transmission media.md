## Transmission Media

- The simplest transmission medium consists of a **pair of conductors**.
- In inter-equipment communication, it often takes the form of a **flat ribbon cable** containing several lines and a common return wire.
- This cable is extremely susceptible to **inductive or capacitively induced noise signals** from neighboring lines.
- Much better noise immunity is obtained by using **pairs of wires twisted together**.
- When carrying an **analogue signal**, it is necessary to insert **amplifiers to boost the signal every 5 or 6 km**.

## Baud Rate

- The **baud rate** refers to the signaling rate at which data is sent through a channel and is measured in **electrical transitions per second**.
- In the **EIA232 serial interface standard**, at most one signal transition occurs per bit, so the **baud rate and bit rate are identical**.
- In this case, a rate of **9600 baud** corresponds to a transfer of **9,600 data bits per second**, with a bit period of **104 microseconds** (\(1/9600\) sec).

## Data Rate, Bandwidth, and Noise

- The **data rate** of a channel is often specified by its **bit rate** (often erroneously thought to be the same as baud rate).
- An equivalent measure of **channel capacity** is **bandwidth**.
- In general, the maximum data rate a channel can support is:
  - **Directly proportional** to the channel's bandwidth.
  - **Inversely proportional** to the channel's noise level.

## Communications Protocol

- A **communications protocol** is an agreed-upon convention that defines the **order and meaning of bits** in a serial transmission.
- It may also specify a procedure for exchanging messages.
- A protocol will define:
  - How many data bits compose a message unit.
  - The framing and formatting bits.
  - Any error-detecting bits that may be added.
  - Other information that governs control of the communications hardware.

## Channel Efficiency

- **Channel efficiency** is determined by the **protocol design** rather than by digital hardware considerations.
- There is a tradeoff between **channel efficiency** and **reliability**:
  - Protocols that provide greater immunity to noise by adding error-detecting and error-correcting codes must necessarily become **less efficient**.

## Asynchronous vs. Synchronous Transmission

- Serialized data is not generally sent at a uniform rate through a channel.
- Instead, there is usually a **burst of regularly spaced binary data bits**, followed by a pause, after which the data flow resumes.
- Packets of binary data are sent in this manner, possibly with variable-length pauses between packets, until the message has been fully transmitted.

### Synchronization

- For the receiving end to know the proper moment to read individual binary bits from the channel, it must know:
  - Exactly when a packet begins.
  - How much time elapses between bits.
- When this timing information is known, the receiver is said to be **synchronized** with the transmitter, and accurate data transfer becomes possible.
- Failure to remain synchronized throughout a transmission will cause data to be **corrupted or lost**.

### Two Basic Synchronization Techniques

- In **synchronous systems**, separate channels are used to transmit **data** and **timing information**.
- The timing channel transmits **clock pulses** to the receiver.
- Upon receipt of a clock pulse, the receiver reads the data channel and latches the bit value found on the channel at that moment.
- The data channel is not read again until the next clock pulse arrives.
- Because the transmitter originates both the data and the timing pulses, the receiver reads the data channel only when told to do so by the transmitter (via the clock pulse), and synchronization is guaranteed.