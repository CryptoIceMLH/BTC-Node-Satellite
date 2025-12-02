# BitSatRelay Ground Station - Off-Grid Terminal

**Decentralized satellite communications for Bitcoin & Nostr**

Hardware designs and documentation for Terminal-1 off-grid satellite communication units.

---

## 🔗 Related Repositories - Integrated System

This is part of a three-component integrated system. Each repository handles a different part of the BitSatRelay network:

| Repository | Purpose | Description |
|------------|---------|-------------|
| **[BitSatRelay](https://github.com/CryptoIceMLH/BitSatRelay)** | Terminal-HQ Bridge | Main codebase - Nostr to satellite bridge |
| **[BitSatRelay-Ground-Station](https://github.com/CryptoIceMLH/BitSatRelay-Ground-Station)** | Off-Grid Terminals | Terminal-1 kits for off-grid satellite TX/RX (this repo) |
| **[lnbits-bitsatcredit](https://github.com/CryptoIceMLH/lnbits-bitsatcredit)** | Payment System | LNbits extension for Lightning micropayments |

**All three components work together** to create the complete BitSatRelay network.

---

## 💜 Support This Project

If you wish to support my work you can donate with BTC:

⚡ **BTC Lightning**: `cryptoice@walletofsatoshi.com`

⚡ **BTC Onchain**: `347ePgUhyvztUWVZ4YZBmBLgTn8hxUFNeQ`

---

> **⚠️ WORK IN PROGRESS**
>
> This repository contains hardware prototypes and design documentation. Complete build guides and software integration instructions are being prepared.
>
> **Current Status**: Hardware design finalized, documentation in progress

---

## What is Terminal-1?

Terminal-1 is an off-grid satellite communication unit that allows Bitcoin nodes and Nostr relays to communicate independently of centralized Internet Service Providers.

**Key Features:**
- 🛰️ Full satellite TX/RX capability
- 🔋 Solar-powered for off-grid operation
- 📡 Amateur geostationary satellite (2.4 GHz uplink / 10.489 GHz downlink)
- 💻 Raspberry Pi 4 based controller
- 🌐 Local WiFi access point for user devices
- 📶 Optional LoRa mesh networking

---

## Purpose

Bitcoin and Nostr must be prepared for all possible attack vectors - including loss of centralized communications infrastructure.

Terminal-1 provides:
- **Communication independence** from ISPs
- **Censorship resistance** via satellite
- **Off-grid capability** with solar power
- **Emergency communications** during internet outages
- **Geographic redundancy** for critical infrastructure

---

## Hardware Components

### Off-the-Shelf Parts

**Core Controller:**
- Raspberry Pi 4 (4GB+ RAM recommended)
- 64GB+ microSD card
- Official Raspberry Pi power supply or solar setup

**Satellite Equipment:**
- HSModem or compatible satellite modem
- 2.4 GHz transmitter (13cm amateur band)
- 10.489 GHz receiver (Ku band)
- Satellite dish with dual-band feed
- LNAs (Low Noise Amplifiers)
- Coax cables and RF connectors

**Power System:**
- Solar panels (50W+)
- Charge controller
- 12V battery bank
- DC-DC converters for Pi and modem

**Networking:**
- USB WiFi adapter (access point mode)
- Optional: LoRa modules for mesh networking

---

## System Architecture

```
┌─────────────────────────────────────────┐
│         Terminal-1 Unit                 │
│                                         │
│  ┌──────────────┐    ┌──────────────┐  │
│  │ Raspberry Pi │◄──►│   HSModem    │  │
│  │      +       │    │              │  │
│  │   strfry     │    │  2.4 GHz TX  │──┼──► Satellite
│  │   relay      │    │ 10.489 GHz RX│◄─┼──┐
│  └───────┬──────┘    └──────────────┘  │  │
│          │                              │  │
│      WiFi AP ◄───► User Devices         │  │
│     (Local)         (Phones/Laptops)    │  │
│                                         │  │
│  ┌──────────────┐                       │  │
│  │ Solar Power  │                       │  │
│  │  + Battery   │                       │  │
│  └──────────────┘                       │  │
└─────────────────────────────────────────┘  │
                                             │
        Satellite Downlink ◄─────────────────┘
```

### Data Flow

**Outbound (User → Satellite):**
1. User device connects to Terminal-1 WiFi
2. User posts to local strfry relay
3. Terminal-1 relays message to HSModem
4. HSModem transmits via 2.4 GHz to satellite
5. Satellite broadcasts globally

**Inbound (Satellite → User):**
1. HSModem receives 10.489 GHz downlink
2. Oscar software decodes message
3. Terminal-1 posts to local strfry relay
4. User devices receive via local WiFi

---

## Hardware Prototypes

Below are images of the R&D process and final design iterations:

### Ground Station Hardware

![Ground Station Overview](Gh-JM2kWIAArmzZ.jpg)

### Terminal-1 Assembly

![Terminal Assembly 1](IMG_20241122_160301.jpg)

![Terminal Assembly 2](IMG_20241122_160236.jpg)

### RF Components

![RF Setup 1](IMG_20241115_125529.jpg)

![RF Setup 2](IMG_20241114_113744.jpg)

### ESP Miner Satellite Integration

![ESP Miner SAT](espminer%20SAT2.jpg)

---

## Software Integration

Terminal-1 units run a local strfry Nostr relay and connect to Terminal-HQ for satellite bridging.

**Software Stack:**
- Raspberry Pi OS (64-bit)
- strfry (local Nostr relay)
- HSModem control software
- Oscar (satellite RX decoder)
- WiFi access point configuration

**For complete software setup**, see the main [BitSatRelay repository](https://github.com/CryptoIceMLH/BitSatRelay).

---

## Use Cases

### 1. Emergency Communications
When internet goes down due to natural disaster, Terminal-1 provides satellite connectivity.

### 2. Off-Grid Bitcoin Nodes
Run a Bitcoin node in remote locations without ISP dependency.

### 3. Censorship Resistance
Communicate on Nostr even if your government blocks internet access.

### 4. Maritime/Aviation
Stay connected while at sea or in the air.

### 5. Remote Operations
Research stations, rural communities, expeditions.

---

## Build Status

**Current Phase**: Hardware design finalized

**Coming Soon:**
- Complete parts list with supplier links
- Step-by-step assembly guide
- Software installation tutorial
- Antenna tuning guide
- Solar power sizing calculator
- Weatherproofing instructions

---

## Community

This is a wild time we live in - Bitcoin must be prepared for all possible attack vectors, including loss of centralized communications infrastructure.

My name is [CryptoIce](https://x.com/MolonLabeVC), and I'm a proud Bitcoin tech nerd. Join me on this journey into true decentralization!

With your continued support, I can expedite the R&D process and deliver complete documentation faster.

---

## Contributing

Contributions welcome! Areas where help is needed:
- Hardware testing and feedback
- Documentation improvements
- Alternative component suggestions
- Power system optimization
- Antenna design improvements

---

## License

GPL-3.0 - see [LICENSE.txt](LICENSE.txt) for details

---

## Contact

- **Nostr**: `npub14uee3fwxjwq7m25gsyqguv2t6v8ft69jax4lvs3skfpa8u7thdsqpu7gam`
- **X/Twitter**: [@MolonLabeVC](https://x.com/MolonLabeVC)
- **Main Project**: [BitSatRelay](https://github.com/CryptoIceMLH/BitSatRelay)
- **Website**: https://bitsat.molonlabe.holdings

---

**BitSatRelay: Communications that can't be stopped.**

🛰️ **Freedom. Privacy. Resilience.** ⚡
