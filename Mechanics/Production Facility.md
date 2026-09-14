# Production Facility

This page describes the satellite production facilities available in each universe. This is where players build satellites from components before launching them into orbit.

> [[Technology Tree]] | [[Currency]] | [[Gameplay Loop]] | [[Companions]] | [[Laboratory]] | [[Orbital Capacity]]

---

## Core Principle

Each universe has its own **Production Facility** where satellites are assembled from components. Players must:
1. Select components from their inventory
2. Choose satellite configuration
3. Pay production costs in coins
4. Wait for production (or use time skips)
5. Launch the completed satellite to a destination planet

The facility's appearance and available component types vary dramatically between universes.

---

## 🌍 Earth / Solar System Production Facility

> #TODO - this is hallucinated example, change eveything about it, treat as placeholders

### Facility Appearance

```
┌─────────────────────────────────────────────────────────────┐
│                  SPACE TECHNOLOGIES INC.                      │
│               "Innovating the Final Frontier"                │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  [COMPONENT BAY]              [ASSEMBLY TABLE]              │
│     ○ Standard Bus           [  Satellite Builder  ]       │
│     ○ Advanced Bus            [  Select Configuration  ]   │
│     ○ Solar Panel             [  Add: Solar Panel ☀️    ]  │
│     ○ Battery                [  Add: Battery 🔋         ]  │
│     ○ RTG Unit               [  Add: RTG ⚛️            ]  │
│     ○ Optical Camera         [  Add: Optical Camera 📷  ] │
│     ○ Spectrometer           [  Add: Spectrometer 🔬   ]  │
│     ○ Antenna               [  Add: Antenna 📡         ] │
│     ○ Landing Module         [  Add: Landing Module 🪐  ]│
│     ○ Radiation Detector     [  Add: Radiation Detector ⚠️]│
│                                                             │
│  [ROCKET DOCK]             [LAUNCH QUEUE (5)]              │
│     [Chemical Rocket]      [Satellite #1 →]                │
│     [Ion Drive Rocket]     [Satellite #2 →]                │
│     [Multi-stage Rocket]   [Satellite #3 →]                │
│     [Ready for Launch!]    [Satellite #4 →]                │
│     [Ready for Launch!]    [Satellite #5 →]                │
│                                                             │
│  💰 2,500 Coins          [LAUNCH!] [Skip: 5 Bux]          │
│  ⏳ Production: 3:45 min                                     │
└─────────────────────────────────────────────────────────────┘
```

### Available Component Types

#### Satellite Bodies (Platforms)

The main chassis that holds all components.

| Component | Cost | Production Time | Description | Tech Tier Required |
|-----------|-------|-----------------|-------------|-------------------|
| Standard Bus | 100 coins | 1 min | Basic satellite platform with minimal shielding | Tier 1 |
| Advanced Bus | 500 coins | 2 min | Reinforced hull, better power distribution | Tier 2 |
| Modular Bus | 1,000 coins | 3 min | Customizable satellite configurations | Tier 3 |
| Heat Resistant Bus | 1,500 coins | 4 min | Protected from radiation and heat | Tier 3+ |
| Cryo Storage Bus | 2,000 coins | 5 min | Preserves instruments in extreme cold | Tier 4 |
| Quantum Chassis | 5,000 coins | 8 min | Stabilizes quantum instruments | Tier 5 |
| Ancient Tech Core | 8,000 coins | 10 min | Repurposed alien technology | Tier 6 |

#### Power Components

| Component | Cost | Production Time | Description | Universe |
|-----------|-------|-----------------|-------------|----------|
| Battery | 300 coins | 1 min | Energy storage for eclipse periods | Earth |
| Solar Panel | 400 coins | 1.5 min | Converts sunlight to electricity | All |
| RTG Unit | 1,500 coins | 4 min | Radioisotope thermoelectric generator | Earth |
| RTG Advanced | 2,000 coins | 5 min | More efficient, less degradation | Earth |
| Fission Reactor | 5,000 coins | 8 min | Nuclear fission power source | Earth |
| Fusion Core | 15,000 coins | 20 min | Fusion power (requires Dyson Sphere) | Sci-Fi |
| Antimatter Pod | 50,000 coins | 30 min | High-density antimatter fuel | Sci-Fi |
| Mana Crystal | 10,000 coins | 30 min | Absorbs ambient magic | Fantasy |
| Potion of Energy | 200 coins | 1 min | Consumable power boost | Fantasy |

#### Scientific Instruments

| Component | Cost | Production Time | Description | Planet Limit |
|-----------|-------|-----------------|-------------|-------------|
| Optical Camera | 500 coins | 2 min | High-resolution imaging | All planets |
| Spectrometer | 800 coins | 3 min | Analyzes atmospheric composition | Earth, Andromeda |
| Magnetometer | 600 coins | 2.5 min | Measures magnetic fields | All planets |
| Radiation Detector | 900 coins | 3.5 min | Monitors radiation levels | Earth |
| Geiger Counter | 400 coins | 2 min | Detects radiation exposure | Earth |
| Life Biosensor | 2,000 coins | 6 min | Detects biosignatures | Andromeda |
| Quantum Sensor | 5,000 coins | 10 min | Detects quantum phenomena | Andromeda, Sci-Fi |
| Dark Matter Detector | 15,000 coins | 15 min | Detects dark matter distribution | Sci-Fi |
| Magic Compass | 3,000 coins | 8 min | Detects magical ley lines | Fantasy |
| Wayreader Lens | 2,000 coins | 5 min | For cartography work | Fantasy |

#### Communications Equipment

| Component | Cost | Production Time | Description | Notes |
|-----------|-------|-----------------|-------------|-------|
| UHF Antenna | 300 coins | 1.5 min | Short-range comms | Earth only |
| VHF Transceiver | 500 coins | 2 min | Medium-range comms | Earth, Moon |
| S-Band Transmitter | 1,000 coins | 3 min | Long-range comms | Earth, Moon, Mars |
| X-Band Relay | 2,000 coins | 4 min | Deep space comms | Earth-Moon-Mars-Jupiter |
| Quantum Transmitter | 8,000 coins | 10 min | Inter-universe comms | Sci-Fi+ |
| Rune Beacon | 5,000 coins | 12 min | Magic navigation beacon | Fantasy |
| Wayglass Node | 10,000 coins | 15 min | Skyward Chart node | Fantasy |

#### Thrust/Propulsion (for landers)

| Component | Cost | Production Time | Description | Planet Limit |
|-----------|-------|-----------------|-------------|-------------|
| Chemical Thrusters | 800 coins | 3 min | Standard rocket propulsion | Earth, Moon, Mars |
| Cryogenic Fuel | 2,000 coins | 5 min | Extended range propellant | Mars, Jupiter |
| Ion Engines | 5,000 coins | 8 min | Efficient ion propulsion | Jupiter+ |
| Fusion Thrusters | 15,000 coins | 15 min | Powerful fusion drives | Sci-Fi+ |
| Portal Key | 5,000 coins | 12 min | Interdimensional portal travel | Fantasy |
| Dragon Egg | 3,000 coins | 60 min | Hatches into dragon rider | Fantasy |

#### Landing Systems

| Component | Cost | Production Time | Description | Planet Requirements |
|-----------|-------|-----------------|-------------|-------------------|
| Basic Landing Gear | 500 coins | 2 min | Simple landing struts | Moon, Mars |
| Heat Shield | 1,200 coins | 4 min | Protection from atmospheric heat | Mars, Venus |
| Parachute System | 600 coins | 2 min | Soft landing for atmosphere | Earth, Venus |
| Skiff Module | 2,000 coins | 5 min | Surface water operation | Earth (ocean) |
| Multi-Grip Treads | 3,000 coins | 7 min | All-terrain landing | Mars, Asteroids |
| Gravity Plates | 8,000 coins | 10 min | Anti-gravity descent | Sci-Fi |
| Teleport Circle | 10,000 coins | 15 min | Instant arrival (Fantasy) | Fantasy |

---

### Satellite Configurations

Players combine components to create specific satellite types:

#### Earth-Specific Configurations

| Configuration | Components Required | Cost | Production Time | Best For |
|---------------|---------------------|------|-----------------|----------|
| Earth Sentinel (Optical) | Advanced Bus, Solar Panel, Battery, Optical Camera | 2,200 coins | 4 min | Surface mapping, general observation |
| Atmos Probe | Spectrometer, Solar Panel, RTG, Pressure Sensor | 3,100 coins | 6 min | Atmospheric research |
| Magnet Surveyor | Magnetometer, Solar Panel, Battery, Magnetometer | 1,900 coins | 4 min | Magnetic field studies |
| Radiation Monitor | Radiation Detector, Geiger Counter, RTG, Shielding | 4,000 coins | 7 min | Van Allen belt monitoring |
| Resource Scanner | Spectrometer, Resource Scanner, Solar Panel, Landing Gear | 4,500 coins | 8 min | Surface mining |
| Orbital Relay | X-Band Transmitter, Solar Panel, Battery (high capacity) | 3,500 coins | 6 min | Communication relay |
| Climate Observer | Infrared Sensor, Radar Altimeter, Microwave Radiometer | 5,000 coins | 9 min | Climate monitoring |

#### Expansion Configurations

| Configuration | Components Required | Cost | Production Time | Best For |
|---------------|---------------------|------|-----------------|----------|
| Lunar Rover | Modular Bus, Chemical Thrusters, Heat Shield, Cameras | 4,000 coins | 8 min | Lunar exploration |
| Mars Colonist | Heat Resistant Bus, Landing Module, Oxygen Generator | 6,500 coins | 12 min | Mars colonization |
| Io Volcano Watch | Thermal Imager, RTG, Heat Shield, Spectrometer | 4,200 coins | 8 min | Volcanic activity monitoring |
| Gas Giant Observer | Cryo Storage Bus, Magnetometer, Fusion Receiver | 8,000 coins | 15 min | Jupiter/Saturn observations |

---

### Production Mechanics

#### Component Inventory

Players collect components through:
- Purchasing at the component bay - OK
- Research rewards - OK 
- Mission rewards - IDK about that
- Companion gifts - OK?
- Event drops - OK

**Inventory Display**:
```
Satellite Bodies:
  ○ Standard Bus x 5
  ○ Advanced Bus x 3

Power:
  ○ Solar Panel x 8
  ○ Battery x 4
  ○ Solar Panel x 8
  ○ RTG Unit x 2

Instruments:
  ○ Optical Camera x 6
  ○ Spectrometer x 4
```

#### Production Queue

The facility can only build N satellites at once:

```
Production Slot 1: [Building...] 45% - Standard Bus with Solar
Production Slot 2: [Ready]       - Satellite Alpha
Production Slot 3: [Building...] 20% - Advanced Bus with Camera
Production Slot 4: [Waiting]     - On queue (ready to produce)
Production Slot 5: [Waiting]     - On queue
```

New slots can be bought with currency or extended with reserach #TBD

Players can:
- Add new satellites to queue (limited to 10 in queue) - ideally no queue and notifications when satellites are done #TBD
- Remove from queue to reuse components
- Time-skip production with premium currency

#### Component Costs by Universe

Component costs scale with universe progression:

| Tier          | Earth Costs        | Andromeda Costs     | Sci-Fi Costs         |
| ------------- | ------------------ | ------------------- | -------------------- |
| Basic         | 100-500 coins      | 200-1,000 coins     | 500-2,000 coins      |
| Advanced      | 500-2,000 coins    | 1,000-5,000 coins   | 2,000-10,000 coins   |
| Specialized   | 1,500-5,000 coins  | 5,000-15,000 coins  | 5,000-25,000 coins   |
| Advanced Tech | 5,000-15,000 coins | 15,000-50,000 coins | 25,000-100,000 coins |

Cost scaling reflects:
- Increased complexity
- Rare materials availability
- Specialized manufacturing required

---

## 🌌 Andromeda Galaxy Production Facility

> #TODO - this is hallucinated example, change eveything about it, treat as placeholders

### Facility Appearance

```
┌─────────────────────────────────────────────────────────────┐
│               ANDROMEDA DRONE INDUSTRIES                     │
│          "Expanding Humanity Among the Stars"               │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  [COMPONENT BAY]              [DRONE ASSEMBLER]             │
│     ○ Basic Drone Chassis     [   Select Config    ]       │
│     ○ Xeno-Composite Chassis   [  Choose Drone Type   ]     │
│     ○ Solar Array             [  Choose Power System ]     │
│     ○ Fission Reactor         [  Add: Fission ⚛️         ] │
│     ○ Quantum Sensor          [  Add: Quantum Sensor 🔮  ] │
│     ○ Plasma Shield           [  Add: Plasma Shield  ⚡    ]│
│     ○ Atmospheric Analyzer    [  Add: Analyzer 🔬      ]  │
│     ○ Artifact Probe          [  Add: Artifact Probe 🏛️  ]│
│     ○ Life Detector           [  Add: Life Detector 👁️ ] │
│     ○ Isotope Extractor        [  Add: Extractor 💎      ] │
│     ○ Colony Supply Pod         [  Add: Supply Pod 📦   ] │
│                                                             │
│  [LAUNCH BAY]                  [DRONE FLEET]               │
│     [Wormhole Array]           [Drone #1 →]                │
│     [Gravity Elevator]         [Drone #2 →]                │
│     [Mag-Lev Transport]        [Drone #3 →]                │
│     [Ready to Launch!]        [Drone #4 →]                │
│     [Ready to Launch!]        [Drone #5 →]                │
│                                                             │
│  💰 5,000 Coins              [LAUNCH!] [Skip: 15 Bux]      │
│  ⏳ Production: 5:23 min                                       │
└─────────────────────────────────────────────────────────────┘
```

### Unique Features

- **Fusion Technology**: Unlocks Kilopower-style compact fission reactors
- **Wormhole Launch**: Special launch method for long distances
- **Artifact Recovery**: Drones equipped for ancient alien artifact activation

### Available Component Types

#### Drone Chassis

| Component | Cost | Production Time | Description | Tech Tier |
|-----------|-------|-----------------|-------------|-----------|
| Basic Drone | 300 coins | 2 min | Simple reconnaissance drone | Tier 1 |
| Explorer Drone | 1,000 coins | 4 min | Long-range exploration capability | Tier 2 |
| Recovery Drone | 1,500 coins | 5 min | Artifact recovery and analysis | Tier 3 |
| Colony Drone | 2,000 coins | 6 min | Supports human colony operations | Tier 4 |
| Mining Drone | 2,500 coins | 7 min | Resource extraction specialist | Tier 4 |
| Quantum Drone | 10,000 coins | 12 min | Advanced quantum sensor platform | Tier 5 |
| Artifact Drone | 15,000 coins | 15 min | Specialized for artifact interaction | Tier 6 |

#### Power Systems

| Component | Cost | Production Time | Description | Notes |
|-----------|-------|-----------------|-------------|-------|
| Compact Solar Array | 500 coins | 2 min | Optimized for space conditions | Andromeda+ |
| Kilopower Fission | 5,000 coins | 8 min | Compact nuclear fission (tested by NASA) | Universal |
| Fusion Battery | 15,000 coins | 20 min | Miniaturized fusion power | Sci-Fi+ |
| Quantum Power Cell | 25,000 coins | 25 min | Self-sustaining quantum power | Sci-Fi |
| Mana Battery | 8,000 coins | 15 min | Stores ambient magical energy | Fantasy (via portal) |

#### Scientific Instruments

| Component | Cost | Production Time | Description | Planet Compatibility |
|-----------|-------|-----------------|-------------|---------------------|
| Atmospheric Scanner | 1,000 coins | 4 min | Analyzes exoplanet atmospheres | All exoplanets |
| Surface LIDAR | 2,000 coins | 6 min | Creates 3D surface maps | Rocky planets |
| Quantum Resonance | 8,000 coins | 10 min | Detects ancient artifacts | Artifact sites only |
| Life Biosignature | 5,000 coins | 8 min | Detects biosignatures in atmosphere | Habitable zone |
| Dark Matter Mapper | 15,000 coins | 15 min | Maps dark matter distribution | All regions |
| Exoplanet Spectrograph | 3,000 coins | 7 min | Detailed atmospheric analysis | All planets |

#### Special Equipment

| Component | Cost | Production Time | Description | Usage |
|-----------|-------|-----------------|-------------|-------|
| Artifact Decryption | 10,000 coins | 15 min | Decodes alien technology | Artifact sites |
| Colony Support Pod | 4,000 coins | 8 min | Emergency supply delivery | Colony planets |
| Relay Beacon | 2,000 coins | 5 min | Communication relay node | Network expansion |
| Shield Generator | 3,000 coins | 6 min | Protects from radiation/storms | High-radiation zones |
| Artifact Beacon | 8,000 coins | 12 min | Summons artifacts to location | Ancient path |

---

## 🚀 Sci-Fi Future World Production Facility

> #TODO - this is hallucinated example, change eveything about it, treat as placeholders

### Facility Appearance

```
┌─────────────────────────────────────────────────────────────┐
│              QUANTUM DYSON CONSTRUCTION CO.                 │
│          "Building Tomorrow in Today's Stars"              │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  [COMPONENT BAY]              [QUANTUM FABRICATION]         │
│     ○ Base Satellite Frame    [   Select Config    ]       │
│     ○ Dyson Panel Segment     [  Choose Power System ]     │
│     ○ Fusion Collector        [  Add: Fusion Core ⚛️      ]│
│     ○ Antimatter Generator    [  Add: Antimatter ⚡       ] │
│     ○ Quantum Processor       [  Add: Quantum CPU 🔮      ]│
│     ○ Entanglement Node       [  Add: Entanglement 🌀     ]│
│     ○ Data Storage Unit       [  Add: Storage 💾         ] │
│     ○ Construction Drone      [  Add: Drone Controller 🤖 ]│
│     ○ Energy Extractor        [  Add: Energy Collector 💠 ]│
│     ○ Time Synchronizer       [  Add: Time Sensor ⏰      ]│
│     ○ Defense Array           [  Add: Shield Module 🛡️   ] │
│     ○ Starship Module         [  Add: Module 🚀          ] │
│                                                             │
│  [STAR SYSTEM MAP]         [QUANTUM MANUFACTORY]           │
│     [Select System]          [   Build Time Progress   ]   │
│     [   ⭐ System Alpha      ]  ████████████░░░░░ 75%     │
│     [   ⭐ System Beta       ]  ██████████░░░░░░░ 50%     │
│     [   ⭐ System Gamma     ]  ░░░░░░░░░░░░░░░░░   10%    │
│     [   ⭐ Dyson Core       ]  ████████████████░░░ 85%    │
│     [   ⭐ Quantum Hub      ]  █████████████████ 95%     │
│                                                             │
│  💰 20,000 Coins           [QUANTUM LAUNCH] [Skip: 50 Bux] │
│  ⏳ Production: 12:30 min                                     │
└─────────────────────────────────────────────────────────────┘
```

### Unique Features

- **Dyson Sphere Construction**: Build solar panel megastructures
- **Quantum Computing**: Research and data processing satellites
- **Antimatter Technology**: Experimental high-energy propulsion
- **Multi-Stage Quantum**: Satellites that can transit between alternate universes

### Available Component Types

#### Satellite Frames

| Component | Cost | Production Time | Description | Requirements |
|-----------|-------|-----------------|-------------|--------------|
| Standard Frame | 1,000 coins | 3 min | Basic spacecraft hull | Any |
| Quantum Stabilized | 5,000 coins | 6 min | Reduces quantum decoherence | Quantum Computing |
| Dyson Segment Base | 10,000 coins | 10 min | Solar panel mounting frame | Dyson Sphere |
| Antimatter Hull | 30,000 coins | 20 min | Withstands extreme radiation | Fusion/Antimatter |
| Time-Anchor Frame | 50,000 coins | 30 min | Stable across time streams | Quantum Gateway |

#### Power Systems

| Component | Cost | Production Time | Description | Notes |
|-----------|-------|-----------------|-------------|-------|
| Mini-Solar Array | 800 coins | 3 min | Compact solar for inner systems | Systems 1-3 |
| Dyson Collector | 50,000 coins | 30 min | Solar panel for Dy Sphere | Dyson Tier 1 |
| Fusion Reactor | 20,000 coins | 12 min | Compact fusion power | Fusion Tech |
| Antimatter Generator | 100,000 coins | 45 min | Creates antimatter from matter | Dyson Sphere Complete |
| Zero-Point Engine | 200,000 coins | 60 min | Taps vacuum energy | Quantum Max |

#### Scientific Instruments

| Component | Cost | Production Time | Description | Usage |
|-----------|-------|-----------------|-------------|-------|
| Quantum Sensor | 5,000 coins | 8 min | Detects quantum phenomena | Standard |
| Data Recorder | 2,000 coins | 4 min | Stores research data | All missions |
| Entanglement Scanner | 15,000 coins | 12 min | Maps quantum entanglement | Quantum missions |
| Chronometer | 8,000 coins | 10 min | Measures time dilation | Time research |
| Dimension Detector | 30,000 coins | 15 min | Detects interdimensional portals | Interdimensional |
| Fusion Analyzer | 12,000 coins | 10 min | Studies fusion reactions | Fusion research |

#### Construction Equipment

| Component | Cost | Production Time | Description | Usage |
|-----------|-------|-----------------|-------------|-------|
| Construction Drone | 3,000 coins | 5 min | Builds orbital structures | Dyson |
| Placement Laser | 8,000 coins | 8 min | Precisely places modules | Dyson |
| Material Scanner | 4,000 coins | 6 min | Analyzes building materials | All |
| Nano-Assembler | 25,000 coins | 15 min | Builds at molecular level | Advanced |

#### Special Equipment

| Component | Cost | Production Time | Description | Usage |
|-----------|-------|-----------------|-------------|-------|
| Quantum Transmitter | 20,000 coins | 15 min | Communicates across realities | Quantum comms |
| Teleporter Module | 100,000 coins | 30 min | Sends matter between universes | Quantum Leap |
| Starship Module | 50,000 coins | 25 min | Personnel transport vessel | Exploration |
| Anomaly Defender | 35,000 coins | 18 min | Protects research ships | Hazard zones |

---

## 🐉 Magic Fantasy World Production Facility

> #TODO - this is hallucinated example, change eveything about it, treat as placeholders

### Facility Appearance

```
┌─────────────────────────────────────────────────────────────┐
│                      AETHER MAGE ACADEMY                   │
│       "Where Magic Meets Mapping in the Sky"              │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  [INCUBATION CHAMBERS]           [DRAGON TRAINING GROUNDS] │
│     ○ [Incubation Pod 1] 🥚     [   Dragon Handler  ]     │
│     ○ [Incubation Pod 2] 🥚     [   Select Dragon Type  ]│
│     ○ [Incubation Pod 3] 🥚     [  Choose Trait to Train ]│
│     ○ [Incubation Pod 4] 🥚     [  Train: Flight Speed   ]│
│     ○ [Incubation Pod 5] 🥚     [  Train: Magic Affinity ]│
│     ○ [Incubation Pod 6] 🥚     [  Train: Loyalty        ]│
│     ○ [Incubation Pod 7] 🥚     [  Train: Intelligence   ]│
│     ○ [Incubation Pod 8] 🥚     [  Train: Endurance      ]│
│     ○ [Incubation Pod 9] 🥚     [  Train: Agility        ]│
│     ○ [Incubation Pod 10] 🥚    [  Train: Combat Skill    ]│
│     ● [Hatched!] 🐉            [   Hatched!         ]     │
│                                                             │
│  [WAYREADER ACADEMY]          [WIZARD'S STUDY]             │
│     ○ Apprentice Wayreader     [   Select Spellbook    ] │
│     ○ Journeyman Wayreader     [   Learn: Pathfinding  ]│
│     ○ Artisan Wayreader        [   Learn: Coordinate  ] │
│     ○ Rune-Smith              [  Craft: Navigation Rune ]│
│     ○ Master Runemaster       [  Craft: Portal Rune     ]│
│     ○ Wayreader Navigator     [  Learn: Map Making     ]│
│     ○ Astromancer            [  Learn: Star Charts     ]│
│     ○ Cartographer           [  Craft: Maps           ]│
│     ○ Map Commission Agent   [  Hire: Clients        ]│
│                                                             │
│  [BEACON NETWORK]            [PORTAL CIRCLE]               │
│     ● [Beacon: City of Lights]  [   Activate Portal    ]│
│     ● [Beacon: Whispering Trees][   Select Destination ]│
│     ● [Beacon: Stone Ring]     [   Pay Mana Cost     ]│
│     ● [Beacon: Sky Peak]       [   Duration: 10 min   ] │
│     ● [Beacon: Ancient Ruins]  [   Duration: 15 min   ] │
│     ● [Beacon: Sacred Grove]   [   Duration: 20 min   ] │
│                                                             │
│  💰 8,000 Coins               [PROCEED] [Skip: 20 Bux]     │
│  ⏳ Incubation: 30-120 min                                   │
│  ⏳ Beacon Delivery: 5-15 min                               │
│  ⏳ Wayreader Training: 15-60 min                           │
└─────────────────────────────────────────────────────────────┘
```

### Unique Features

- **Dragon Breeding**: Hatch dragons from eggs with randomized traits
- **Dragon Training**: Train dragons in specific skills through sessions
- **Rune Crafting**: Craft magical runes for beacon placement
- **Map Commissions**: Hire clients to commission specific regions
- **No Permanent Damage**: Dragons don't die, they just sleep and age

### Dragon Types (The "Satellites")

Different dragon types excel at different tasks:

| Dragon Type | Best For | Base Traits | Production Time | Cost |
|-------------|----------|-------------|-----------------|------|
| Earth Dragon | Forests, Mountains | Ground adaptation | 60 min | 3,000 coins |
| Fire Dragon | Volcanoes, Lava Fields | Heat resistance | 60 min | 3,500 coins |
| Water Dragon | Oceans, Lakes | Water adaptation | 60 min | 3,000 coins |
| Air Dragon | Clouds, Sky | Flight capability | 90 min | 4,000 coins |
| Ice Dragon | Frozen Regions | Cold adaptation | 60 min | 3,500 coins |
| Storm Dragon | Storm Areas | Weather adaptation | 90 min | 4,500 coins |
| Shadow Dragon | Dark Places | Stealth capability | 90 min | 5,000 coins |
| Sun Dragon | Bright Areas | Sunlight sensitivity | 60 min | 3,500 coins |
| Beast Dragon | Wildlife Areas | Animal intuition | 60 min | 3,500 coins |
| Metal Dragon | Mining Areas | Metal affinity | 60 min | 3,500 coins |
| Dream Dragon | Dream Realm | Dream traversal | 120 min | 8,000 coins |
| Void Dragon | Void Realm | Void resistance | 150 min | 15,000 coins |

### Dragon Breeding System

Instead of buying components, you breed dragons:

#### Breeding Mechanics

```
┌─────────────────────────────────────────────────────────────┐
│              DRAGON BREEDING FACILITY                        │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  SELECT PARENT DRAGONS:                                     │
│     Mother: [Fire Dragon] [Fire] [Loyalty: 50] [Flight: 40] │
│     Father: [Earth Dragon] [Earth] [Loyalty: 70] [Flight: 30]│
│                                                             │
│  BREEDING RESULT:                                           │
│     [🥚 Dragon Egg]                                         │
│     Expected Traits:                                        │
│       - 50% chance for Fire or Earth affinity              │
│       - Loyalty: 60 (average of parents)                    │
│       - Flight: 35 (weighted by base type)                 │
│                                                             │
│     INCUBATION: 60 minutes                                 │
│                                                             │
│     [BREED] [Cancel]                                       │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

#### Trait Inheritance

| Parent Trait                | Inheritance Chance   | Notes                                     |
| --------------------------- | -------------------- | ----------------------------------------- |
| Elemental Affinity          | 50/50 from parents   | Can be Fire, Earth, Water, Air, Ice, etc. |
| Skill (Flight, Magic, etc.) | Average of both      | Sometimes slightly higher/lower           |
| Personality                 | Random from range    | Affects quest compatibility               |
| Loyalty #TBD                | Average + randomness | Affects dragon service quality            |

#### Breeding Costs

| Action | Cost | Notes |
|--------|------|-------|
| Purchase Egg | 3,000-15,000 coins | Price varies by base type |
| Breeding Energy | 100 per cycle | Drains from dragon mana |
| Incubation Mana | 500 per egg | Paid in mana or coins |
| Training Session | 50 per session | For skill training |

#### Breeding Facilities

Levels of breeding infrastructure:

| Facility Level | Slots | Cost to Unlock | Cost to Upgrade |
|----------------|-------|----------------|-----------------|
| Basic Nursery | 5 slots | Quest 1 | 1,000 coins |
| Expanded Nursery | 15 slots | Quest 2 | 3,000 coins |
| Advanced Breeding | 25 slots | Quest 3 | 5,000 coins |
| Grand Breeding | 50 slots | Endgame | 10,000 coins |

---

### Wayreader Training

Wayreaders are the "satellite controllers" in Fantasy - they're the humans who ride dragons and draw maps:

#### Wayreader Ranks

| Rank | Required | Training Time | Special Perks |
|------|----------|---------------|---------------|
| Apprentice | Start | Instant | Basic navigation |
| Journeyman | Level 5 | 15 min | Faster map drawing |
| Artisan | Level 10 | 30 min | High quality maps |
| Master | Level 20 | 60 min | Expert navigation |
| Grandmaster | Level 50 | 90 min | Perfectionist maps |

#### Training Options

| Training Type | Cost | Duration | Effect |
|---------------|------|---------|--------|
| Pathfinding | 50 coins | 10 min | Better route planning |
| Coordinate Work | 50 coins | 10 min | More accurate placement |
| Map Drafting | 50 coins | 10 min | Faster map creation |
| Portal Knowledge | 100 coins | 20 min | Better portal navigation |
| Speed Training | 75 coins | 15 min | Faster map completion |

---

### Wayglass Beacon System

Wayglass Beacons are magical runes that create permanent navigation points:

#### Beacon Crafting

```
┌─────────────────────────────────────────────────────────────┐
│                  WAYGLASS BEacon CRAFTING                   │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  SELECT ENTITY TO NAME:                                    │
│     [☑️ City] [☑️ Mountain] [☑️ Forest] [☑️ River]         │
│     [☑️ Castle] [☑️ Temple] [☑️ Ruin] [☑️ Cave]            │
│     [☐ Other]                                                │
│                                                             │
│  SELECT RUNE TO PLACE:                                     │
│     [○ Navigation Rune]        [○ Portal Rune]              │
│     [○ Marker Rune]           [○ Boundary Rune]            │
│     [○ Anchor Rune]           [○ Compass Rune]             │
│                                                             │
│  SELECT DRAGON:                                            │
│     Choose delivery dragon from your dragons              │
│     Required: [✓] Can fly to target                        │
│     Required: [✓] Has sufficient mana                     │
│                                                             │
│  TARGET LOCATION:                                          │
│     Latitude:  [____] °N/S                                │
│     Longitude: [____] °E/W                                │
│     Altitude:  [____] meters (above ground)               │
│                                                             │
│  PREVIEW:                                                  │
│     (Shows where beacon will appear on the map)          │
│                                                             │
│  MANA COST: 500 runes                                      │
│  DRAGON COST: 500 coins                                    │
│  [CRAFT AND DELIVER BEACON]                                 │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

#### Beacon Types

| Rune Type | Purpose | Duration | Mana Cost | Notes |
|-----------|---------|----------|-----------|-------|
| Navigation | Quick travel to named location | Permanent | 100 runes | Fastest route via portals |
| Waypoint | Marker for your map | Permanent | 50 runes | Shows on player's map |
| Portal | Instant travel to/from | Degradable | 200 runes | Connects two locations |
| Anchor | Stabilizes nearby portals | Permanent | 300 runes | Prevents portal drift |
| Boundary | Marks realm boundary | Permanent | 400 runes | Shows realm edges |
| Compass | Points to nearest hub | Permanent | 150 runes | Navigation aid |

---

## Universal Component System

Some components are shared across universes:

### Premium Currency Purchases

| Component               | Price      | Description               | Available In |
| ----------------------- | ---------- | ------------------------- | ------------ |
| Standard Time Skip      | 10 Bux     | Skip 1 production minute  | All          |
| Instant Production Pass | 50 Bux     | Skip all production queue | All          |
| Satellite Skin Pack     | 50-200 Bux | Cosmetic appearance       | All          |
| Station Theme           | 100 Bux    | Base visual customization | All          |
| Expansion Credits       | 250 Bux    | Buy extra orbital slots   | All          |
| Bux Recharge (small)    | 100 Bux    | 1,000 credits             | All          |
| Bux Recharge (large)    | 500 Bux    | 5,000 credits             | All          |

### Shared Technologies

Some technologies unlock systems across multiple universes:

| Technology | Earth Effect | Andromeda Effect | Sci-Fi Effect | Fantasy Effect |
|------------|--------------|-----------------|---------------|----------------|
| Advanced Optics | Better cameras | Better scanners | Better sensors | Better map detail |
| Heat Protection | Heat shielding | Plasma shield | Fusion cooling | Fire resistance |
| Power Efficiency | Better batteries | Better fission | Better fusion | Lower mana cost |
| Launch Optimization | Faster rockets | Better wormholes | Faster quantum | Easier portaling |

---

## Launch Facilities

Each universe has unique launch methods:

### Earth / Andromeda / Sci-Fi

#### Chemical Rocket
- **Cost**: 100-3,000 coins (by planet)
- **Capacity**: 5 satellites per launch
- **Transit Time**: 5-30 min (by planet)
- **Drawback**: High fuel consumption, slow

#### Ion Drive
- **Cost**: 150-5,000 coins
- **Capacity**: 3 satellites per launch
- **Transit Time**: 30-60 min
- **Advantage**: Very fuel efficient

#### Wormhole (Andromeda)
- **Cost**: 10,000-1,000 coins
- **Capacity**: 10 satellites per launch
- **Transit Time**: 1-5 min
- **Availability**: After Colony Discovery

#### Quantum Teleporter (Sci-Fi)
- **Cost**: 20,000-5,000 coins
- **Capacity**: 50 satellites per launch
- **Transit Time**: Instant
- **Availability**: After Dyson Sphere

### Fantasy

#### Dragon Riders
- **Cost**: 500 coins per dragon + rider
- **Capacity**: 1 per launch
- **Transit Time**: Instant
- **Special**: Can cross realms without portal network

#### Wayglass Portals
- **Cost**: 500-1,000 coins per beacon setup
- **Capacity**: Unlimited (after beacons built)
- **Transit Time**: Instant
- **Special**: Must build beacon network first

---

## Production Queue Management

### Facility Slots

The Production Facility has limited slots:

| Universe | Production Slots | Queue Slots |
|----------|------------------|-------------|
| Earth | 5 | 10 |
| Andromeda | 5 | 10 |
| Sci-Fi | 7 | 15 |
| Fantasy | 10 (incubation) + 5 (delivery) | 20 |

### Queue Strategy Tips

1. **Build basics first**: Stock up on basic components for standard satellites
2. **Plan ahead**: Check mission requirements before producing
3. **Prioritize critical tech**: Build satellites that unlock new content
4. **Time skip strategically**: Use Bux during idle time
5. **Retire strategically**: Remove end-of-life satellites to free slots

---

## Linking to Other Mechanics

This page links to:

- **[[Technology Tree]]**: Component unlock progression
- **[[Currency]]**: Component purchase costs
- **[[Gameplay Loop]]**: How production fits into the loop
- **[[Orbital Capacity]]**: Where satellites go after production
- **[[Missions]]**: What to do with satellites
- **[[Satellite Durability]]**: How satellites age over time
- **[[Companions]]**: Help with production decisions
- **[[Laboratory]]**: Research for better components

---

## Future Expansions (TODO)

- [ ] Add rare component crafting (chances based on events)
- [ ] Add component merging (combine basics into advanced)
- [ ] Add salvage system (break satellites for components)
- [ ] Add special component vendors (event-only items)
- [ ] Add component trading (between players)
- [ ] Add prestige component resets
- [ ] Add more fantasy dragon types
- [ ] Add more alien artifact types
- [ ] Add more Sci-Fi instrument types

---

## See Also

- [[Satellite Durability]] - How satellites degrade
- [[Companions]] - Companions available in Production
- [[Currency]] - How to earn coins for components
- [[Technology Tree]] - How to unlock better components