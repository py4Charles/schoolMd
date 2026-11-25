# Satellite Communication

## Overview

- A communication satellite is, in effect, a **microwave relay station**.
- It is used for both **point-to-point** and **broadcast** transmission.
- Ground stations can transmit signals to the satellite, and the satellite can retransmit signals to many receiving stations.
- The satellite receives a transmission on the **uplink frequency** and retransmits it on the **downlink frequency**.

## Frequency Considerations

- Ideally, satellite communication frequencies should be between **1 GHz and 10 GHz**.
- Atmospheric absorption and attenuation increase significantly **above 10 GHz**.
- However, higher frequencies are increasingly used because the ideal frequency range is becoming congested.

## Problems Affecting Satellite Transmission

- **High launch cost:** Placing a satellite correctly into orbit is expensive.
- **High power requirements:** The satellite needs sufficient power to relay signals back to Earth.
- **Large ground antennas:** Earth stations require high-gain dish antennas to receive weak satellite signals.
- **Transmission delay:** The long transmission path causes a delay of about **240–300 milliseconds**.
  - This delay is noticeable in ordinary telephone conversations.
  - It can also cause problems in digital data transmission.
- **Doppler shift:** In Low Earth Orbit (LEO) satellite systems, the movement of satellites causes a shift in carrier frequency as they pass over a receiving station.

## Low Earth Orbit (LEO) Satellites

- There has been significant interest in LEO satellites for commercial communication systems.
- A LEO system consists of many satellites operating in circular orbits.
- Typical orbital heights range from about **500 km to 1,600 km**.
- Advantages of LEO satellites include:
  - Lower launching costs
  - Reduced transmission delay
  - Lower power requirements
- A major challenge is **Doppler shift**, caused by the satellite’s movement relative to the receiving station.

## Transmission Waveform

- Satellite communication transmits digital information as a waveform representing binary data:
  - `1`
  - `0`

# RF Propagation

## Types of RF Propagation

There are three main types of radio frequency propagation:

1. **Ground wave propagation**
2. **Ionospheric propagation**
3. **Line-of-sight (LOS) propagation**

## Ground Wave Propagation

- Ground waves follow the curvature of the Earth.
- They operate at carrier frequencies up to **2 MHz**.
- **AM radio** is an example of ground wave propagation.

## Ionospheric Propagation

- Ionospheric propagation occurs when signals bounce off the Earth’s ionosphere in the upper atmosphere.
- It is sometimes called **double-hop propagation**.
- It operates mainly in the frequency range of **30–85 MHz**.
- Because it depends on the ionosphere, its performance changes with:
  - Weather conditions
  - Time of day
- The signal travels from the transmitter, reflects off the ionosphere, and returns to Earth.
- AM radio can also operate in this range.

## Line-of-Sight Propagation

- Line-of-sight (LOS) propagation transmits signals directly between two stations that can “see” each other.
- The receiving station must be within the visible range of the transmitting station.
- It is also called:
  - **Space wave propagation**
  - **Tropospheric propagation**
- It is limited by the curvature of the Earth.
- For ground-based stations, the practical range is approximately **100 km from horizon to horizon**.
- Reflected waves can cause interference and signal problems.
- Examples include:
  - FM radio
  - Microwave communication
  - Satellite communication

# Radio Frequencies

## Electromagnetic Spectrum

| Radiation Type | Approximate Frequency |
|---|---:|
| Gamma rays | \(10^{19}\) Hz and above |
| X-rays | \(10^{17}\) Hz |
| Ultraviolet light | \(7.5 \times 10^{15}\) Hz |
| Visible light | \(4.3 \times 10^{14}\) Hz |
| Infrared light | \(3 \times 10^{11}\) Hz |

## Radio Frequency Bands

| Band | Full Name | Frequency Range | Examples |
|---|---|---:|---|
| EHF | Extremely High Frequency | 30–300 GHz | Radar |
| SHF | Super High Frequency | 3–30 GHz | Satellite and microwave communication |
| UHF | Ultra High Frequency | 300 MHz–3 GHz | UHF television, Channels 14–83 |
| VHF | Very High Frequency | 30–300 MHz | FM radio, TV Channels 2–13 |
| HF | High Frequency | 3–30 MHz | Short-wave radio |
| MF | Medium Frequency | 300 kHz–3 MHz | AM radio |
| LF | Low Frequency | 30–300 kHz | Navigation |
| VLF | Very Low Frequency | 3–30 kHz | Submarine communication |
| VF | Voice Frequency | 300 Hz–3 kHz | Audio |
| ELF | Extremely Low Frequency | Below 300 Hz | Power transmission |

## Common Frequency Units

- **kHz** = kilohertz = \(10^3\) Hz
- **MHz** = megahertz = \(10^6\) Hz
- **GHz** = gigahertz = \(10^9\) Hz

## Radio Frequency Range

- Radio frequencies commonly used in communication range from about **300 kHz to 10 GHz**.
- Wireless LANs are an emerging technology that may use:
  - Radio frequencies to connect workstations
  - Infrared technology for short-range communication

# Microwave Transmission

## How It Works

- Microwave transmission is a form of **line-of-sight transmission**.
- The transmitting station must have a clear, visible path to the receiving station.
- The Earth’s curvature limits the line-of-sight distance to approximately **50 km to the horizon**.
- Repeater stations are therefore placed between distant locations so that signals can “hop” across long distances.

## Frequency and Capacity

- Microwaves typically operate at frequencies between **3 GHz and 10 GHz**.
- Their high operating frequencies provide large bandwidth.
- This allows microwave systems to carry large quantities of data.

## Advantages

- No need to acquire right-of-way land between transmission towers.
- Can carry large amounts of information because of high operating frequencies.
- Low land cost, since each tower occupies only a small area.
- High-frequency, short-wavelength signals require relatively small antennas.

## Disadvantages

- Signals can be attenuated by:
  - Solid objects
  - Buildings
  - Birds
  - Rain
  - Snow
  - Fog
- Signals can be reflected by flat surfaces such as:
  - Water
  - Metal
- Signals can be diffracted, or split, around solid objects.
- Signals can be refracted by the atmosphere, causing the beam to be directed away from the receiver.

# Satellite Systems

## Satellite as a Transponder

- A satellite acts as a **transponder**.
- A transponder receives a signal on one frequency and retransmits it on another frequency.
- Communication satellites are commonly placed in **geostationary orbit** directly above the equator.

## Geostationary Orbit

- A geostationary satellite orbits at approximately **36,000 km** above the Earth’s surface.
- At this altitude:
  - The gravitational pull of the Earth
  - The centrifugal force caused by the Earth’s rotation
  
  are balanced.
- This allows the satellite to appear stationary relative to a fixed point on Earth.

## Uplink and Downlink

- The **uplink** is the transmission of data from an Earth station to the satellite.
- The **downlink** is the transmission of data from the satellite back to an Earth station.
- Uplinks and downlinks are also called **Earth stations** because they are located on the Earth.

## Satellite Footprint

- The **footprint** is the area of the Earth’s surface that can receive signals from a satellite.
- It is sometimes described as the “shadow” of the satellite’s transmission coverage.
- Any station located within the footprint can receive the satellite signal.

# Iridium Telecom System

## Overview

- The Iridium Telecom System is a major satellite-based mobile telecommunications system.
- It was designed to compete with cellular phone systems.
- It uses satellites in **Low Earth Orbit (LEO)**.

## Satellite Configuration

- The system uses satellites in a polar, non-stationary orbit.
- The satellites orbit at an altitude of approximately **900 km to 10,000 km**.
- **66 satellites** were planned for the system.

## Key Features

- User handsets require less power than traditional cellular phones.
- The handsets are expected to be cheaper than cellular phones.
- The system provides **100% global coverage** of the Earth.

continue slide 127