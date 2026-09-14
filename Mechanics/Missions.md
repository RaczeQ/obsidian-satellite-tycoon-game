# Missions

This page describes the mission system across all universes. Missions are delivered by satellites stationed at planets/celestial bodies, and are the primary way players earn rewards.

> [[Gameplay Loop]] | [[Technology Tree]] | [[Power Systems]] | [[Orbital Capacity]] | [[Currency]] | [[Achievements]]

---

## Core Principle

Each planet/celestial body in each universe has its own **mission board**. Satellites stationed at that location can accept missions from its board. When a mission is completed, the satellite returns with rewards and becomes available for the next mission.

**Key Mechanics**:
- **Multiple missions available** - each planet has several active missions simultaneously
- **Mission duration** - scales with planet difficulty **and** satellite degradation (see [[#Mission Duration Formula]])
- **No mission pool timer** - unlimited missions, limited only by orbital/stable capacity
- **No permanent satellite destruction** - satellites degrade (perform worse), not die (see [[Satellite Durability]])
- **Multiple satellites needed** for coverage missions and quest chains
- **Reward scales with difficulty** - higher-tier planets pay more
- **Mission selection** - automatically sorted by estimated completion time (fastest first)
- **Optional filter** - "Hide degraded/parked" satellites

**Fantasy Unique System** ([[Magic Fantasy World]]):
- **Stables** - per-realm housing capacity for dragons (paid slot purchases, not research-based)
- **Riders (Wayreaders)** - global pool of riders who coordinate dragons in flight (research progression) #TBD
- **Dragons never die** - they just age and sleep when power is low
- **Capacity split is separate** from quest progression (see [[Orbital Capacity]] for Fantasy-specific notes)

**Currency Rules**:
- **Normal currency (Coins)** - **siloed per universe** (Earth, Andromeda, Sci-Fi, Fantasy each have their own)
- **Premium currency (Bux)** - **shared across all universes**
- **Bux uses**: Time skips and cosmetics only (skins, station themes)
- **No content locked behind premium** - all progression is grindable

---

## Mission Duration Formula

Mission duration is **not fixed** - it dynamically scales based on two factors:

### Base Duration
Each mission type has a **base duration** that scales by planet/region difficulty:

| Mission Type | Base Duration (Easy Planet) | Multiplier for Hard Planet |
|--------------|---------------------------|---------------------------|
| Surface Mapping | 3 min | +100% |
| Atmosphere Monitoring | 5 min | +100% |
| Magnetic Field Studies | 4 min | +100% |
| Radiation Monitoring | 6 min | +100% |
| Resource Collection | 10 min | +100% |
| Communication Relay | ∞ | ∞ |
| Climate Monitoring | 15 min | +100% |

**Planet Difficulty Scale**:
- Easy: Mercury/Venus, Moon, First Realm
- Medium: Earth, Mars, Second Realm
- Hard: Jupiter, Third Realm
- Extreme: Outer Planets, Gas Giants, Sky Realm

**Base duration ranges by mission type**:
- **Quick missions** (1-5 min): Space Debris Tracking, Colon Support, Beacon Placement
- **Standard missions** (5-15 min): Mapping, Atmos Monitoring, Magnetic Studies
- **Medium missions** (15-30 min): Radiation, Astrology, Training, Client Quests
- **Long missions** (30-60+ min): Resource Collection, Dyson Assembly, Quantum Assistance
- **Persistent missions** (∞): Communication Relay, Portal Maintenance, Quantum Network

### Degradation Penalty
As satellites degrade (health decreases), their **mission completion time increases**:

#TDB - prorably steeper curve than this

| Health % | Degradation Penalty Per Mission |
| -------- | ------------------------------- |
| 100-75%  | 0% (fresh satellite)            |
| 74-51%   | 2% duration increase            |
| 50-26%   | 5% duration increase            |
| 25-1%    | 8% duration increase            |
| 0-25%    | very slow                       |

**Maximum degradation impact**: **8% per mission** (cannot exceed this)  
**Capped at**: **+200% total duration increase** (satellite can't be 5× slower)

### Critical Events
Rarely (~3-5% chance per mission), a critical event can cause **extra damage beyond normal wear**:
- Solar flares / Coronal Mass Ejections (Earth)
- Micrometeorite strikes
- Geomagnetic storms
- Quantum decoherence (Sci-Fi)
- Dragon exhaustion (Fantasy - triggers early retirement option)

These cause **extra health loss** (e.g., a "High risk" mission might hit for 25% instead of 10-18%), which indirectly increases effective duration by forcing you to wait longer between missions if the satellite gets disabled.

### **Duration Calculation Formula**
```
Total Duration = Base Duration × (1 + Degradation Penalty)
Degradation Penalty = (25% - Current Health %) × 0.04
Clamped: Min 0%, Max 20% per mission, 200% total
```

**Example**: A Mars mission (base 8 min) on a 40% health satellite:
- Degradation penalty: (25 - 40) × 0.04 = -0.6% → Clamped to 0% minimum
- Actual duration: 8 min (no bonus for being faster)

**Example**: A Mars mission (base 8 min) on a 20% health satellite:
- Degradation penalty: (25 - 20) × 0.04 = 0.2% per mission
- Total duration: 8 × 1.002 = ~8 min (minimal impact)

**Example**: A Mars mission (base 8 min) on a 5% health satellite:
- Degradation penalty: (25 - 5) × 0.04 = 0.8% per mission
- Total duration: 8 × 1.008 = ~8 min (still minimal)

**Example**: A Mars mission (base 8 min) on a 10% health satellite (near retirement threshold):
- Degradation penalty: (25 - 10) × 0.04 = 0.6% per mission
- Total duration: 8 × 1.006 = ~8 min

The formula is designed to be **very forgiving** - degradation has minimal impact until health drops below 25%, where it starts having a small effect. Most satellites complete 50-100 missions before needing a patch or retirement.

### **Summary: Low-Stress Design**
- Fresh satellites (100-75% health): Normal speed
- Degraded satellites (74-1% health): Slightly slower (+0-8% per mission)
- Near retirement (<25% health): Enters patch queue (no new missions assigned)
- **No urgent timers** - you can wait indefinitely for missions to complete
- **Retirement is always optional** - retirement bonus (coins) offsets the "lost" missions

---

## 🌍 Earth / Solar System

### Power Sources
All missions require **solar-powered satellites** (see [[Power Systems]]). Solar panels generate power based on distance from the Sun (inverse-square law). Solar efficiency drops significantly past Mars, making nuclear power (RTG) necessary for outer planets.

### Standard Mission Types

#### 1. Surface Mapping (Optical)
- **Description**: Satellite captures high-resolution images of the planet's surface
- **Required Instruments**: Optical Camera
- **Duration**: 3-8 min (varies by planet)
- **Base Difficulty**: Easy
- **Description for Player**: *"Capture images of this planet's surface for geological analysis."*
- **Special Requirements**: None
- **Power Source**: Solar Panels + Battery

#### 2. Atmosphere Monitoring
- **Description**: Satellite analyzes atmospheric composition and weather patterns
- **Required Instruments**: Spectrometer, Atmospheric Sensor
- **Duration**: 5-12 min
- **Base Difficulty**: Medium
- **Description for Player**: *"Study the planet's atmosphere for scientific research."*
- **Special Requirements**: None
- **Power Source**: Solar Panels + Battery

#### 3. Magnetic Field Studies
- **Description**: Satellite measures the planet's magnetic field strength and orientation
- **Required Instruments**: Magnetometer
- **Duration**: 4-10 min
- **Base Difficulty**: Medium
- **Description for Player**: *"Measure the planet's magnetic field properties."*
- **Special Requirements**: None
- **Power Source**: Solar Panels + Battery

#### 4. Radiation Monitoring
- **Description**: Satellite monitors radiation levels in the planet's magnetosphere or space
- **Required Instruments**: Radiation Detector, Geiger Counter
- **Duration**: 6-15 min
- **Base Difficulty**: Hard
- **Description for Player**: *"Monitor radiation belts for space weather research."*
- **Special Requirements**: None
- **Power Source**: Solar Panels + Battery (or RTG for outer planets)

#### 5. Resource Collection
- **Description**: Satellite identifies and extracts valuable surface resources
- **Required Instruments**: Spectrometer, Resource Scanner, Landing Module
- **Duration**: 10-25 min (harvesting time)
- **Base Difficulty**: Very Hard
- **Description for Player**: *"Collect rare minerals from this planet's surface."*
- **Special Requirements**: Landing module (consumes fuel faster)
- **Power Source**: Solar Panels + Battery + Fuel Tank

#### 6. Communication Relay
- **Description**: Satellite acts as a relay station for communication between locations
- **Required Instruments**: Antenna, Transmitter, Battery (high capacity)
- **Duration**: Continuous (until destroyed by eclipse)
- **Base Difficulty**: Easy
- **Description for Player**: *"Maintain a communication relay network."*
- **Special Requirements**: Must stay in line-of-sight, survives eclipses better
- **Note**: This is a **persistent mission** - satellites assigned here stay until they fail
- **Power Source**: Solar Panels + Battery (high capacity battery required)

#### 7. Space Debris Tracking
- **Description**: Satellite tracks and catalogs space debris orbiting the planet
- **Required Instruments**: Optical Camera, Radar
- **Duration**: 2-5 min
- **Base Difficulty**: Easy
- **Description for Player**: *"Catalog space debris for the Spaceguard Observatory."*
- **Special Requirements**: None
- **Power Source**: Solar Panels + Battery

#### 8. Climate Monitoring
- **Description**: Satellite tracks long-term climate changes and ocean temperatures
- **Required Instruments**: Infrared Sensor, Radar Altimeter, Microwave Radiometer
- **Duration**: 15-45 min (long observation period)
- **Base Difficulty**: Very Hard
- **Description for Player**: *"Monitor global climate patterns for environmental research."*
- **Special Requirements**: Requires continuous monitoring (returns data every 1-3 min during mission)
- **Power Source**: Solar Panels + Battery + Communication Link

### Power Source Notes
- **Inner planets** (Mercury, Venus, Earth, Mars): Solar + Battery works well
- **Outer planets** (Jupiter+): Solar becomes inefficient due to inverse-square law → must unlock RTG
- **See [[Power Systems]]** for detailed recharge times by planet
- **Eclipse effect**: Satellites passing through a planet's shadow drain their battery briefly

### Visual Indicators
- **Solar satellites**: Sun icons showing panel efficiency (1-3 filled)
- **Battery icon**: Shows charge level (0-100%)
- **Low battery warning**: Appears when battery <15%

### Earth-Specific Quest Lines

See [[#Earth Quest Lines]] for detailed quest progression tied to mission completion.

---

## 🌌 Andromeda Galaxy

### Power Sources
All missions require **solar or nuclear-powered satellites** (see [[Power Systems]]). Solar works in the Andromeda's central bright region (very bright - Andromeda's core is billions of times brighter than the Sun!), but nuclear power (Fission/Kilopower) is required for deep space exploration beyond the central bright region.

### Standard Mission Types

#### 1. Atmosphere Scanning
- **Description**: Satellite analyzes the exoplanet's atmosphere for habitability
- **Required Instruments**: Spectrometer, Atmospheric Sensor
- **Duration**: 5-15 min (scales by planet difficulty and degradation)
- **Base Difficulty**: Easy (terrestrial planets) to Extreme (gas giants)
- **Description for Player**: *"Scan the atmosphere of this exoplanet for colonisation viability."*
- **Special Requirements**: None
- **Power Source**: Solar Panels + Battery (inner galaxy) or Fission (deep space)

#### 2. Surface Exploration
- **Description**: Satellite explores and maps the surface of the exoplanet
- **Required Instruments**: Optical Camera, LIDAR, Surface Scanner
- **Duration**: 10-25 min (scales by planet distance from sun, not size)
- **Base Difficulty**: Medium-Hard
- **Description for Player**: *"Explore this planet's surface and create a detailed map."*
- **Special Requirements**: Needs heat shielding (beyond inner galaxy)
- **Power Source**: Solar Panels + Battery + Heat Shielding (Fission recommended for outer planets)

#### 3. Ancient Artifact Recovery
- **Description**: Satellite activates and samples ancient alien artifacts
- **Required Instruments**: Quantum Sensor, Archaeological Scanner, Energy Shield
- **Duration**: 20-40 min (artifact activation varies in complexity)
- **Base Difficulty**: Hard to Extreme (higher risk)
- **Description for Player**: *"Locate and reactivate an ancient alien artifact using quantum resonance."*
- **Special Requirements**:
  - Must have "Quantum Sensor" technology unlocked (see [[Technology Tree]])
  - Artifacts can damage the satellite (20-30% health loss on critical events)
  - Some artifacts require multiple visits (quest chain)
- **Power Source**: Fission Reactor required (quantum tech is too power-intensive for solar)

#### 4. Life Detection
- **Description**: Satellite searches for biosignatures in the exoplanet's atmosphere
- **Required Instruments**: Spectrometer, Biosensor, Mass Spectrometer
- **Duration**: 15-30 min
- **Base Difficulty**: Hard
- **Description for Player**: *"Search for signs of life in this planet's atmosphere."*
- **Special Requirements**: Biosensor technology (unlocked via research)
- **Power Source**: Fission Reactor (too sensitive for solar at distances beyond inner galaxy)

#### 5. Dark Matter Mapping
- **Description**: Satellite attempts to detect and map dark matter distribution
- **Required Instruments**: Quantum Sensor, Dark Matter Detector
- **Duration**: 30-60 min (very long scan time)
- **Base Difficulty**: Extreme
- **Description for Player**: *"Detect and map dark matter concentration in this galactic region."*
- **Special Requirements**: Requires "Quantum Computing" research tier
- **Power Source**: Fission Reactor (requires sustained, stable power)

#### 6. Resource Mining
- **Description**: Satellite extracts rare minerals from asteroids or exoplanet surface
- **Required Instruments**: Resource Scanner, Mining Drill, Energy Shield
- **Duration**: 20-50 min (harvesting time)
- **Base Difficulty**: Very Hard
- **Description for Player**: *"Mine rare isotopes from this asteroid belt."*
- **Special Requirements**: Mining equipment research unlocked
- **Power Source**: Fission Reactor (requires high power output)

#### 7. Relay Station Maintenance
- **Description**: Satellite maintains communication relay network for the colony
- **Required Instruments**: Antenna, Transmitter, Battery (high capacity)
- **Duration**: Continuous (until power fails or sabotage)
- **Base Difficulty**: Medium
- **Description for Player**: *"Maintain the colony's communication relay network."*
- **Special Requirements**: Must survive radiation bursts, sabotage events
- **Power Source**: Solar Panels + Battery (high capacity) or Fission

#### 8. Colony Support
- **Description**: Satellite provides supply drops and support to the human colony
- **Required Instruments**: Cargo Bay, Communication Relay, Medical Scanner
- **Duration**: 2-10 min (resupply missions)
- **Base Difficulty**: Easy-Medium
- **Description for Player**: *"Deliver emergency supplies to the Andromeda colony."*
- **Special Requirements**: Cargo capacity, fuel efficiency bonuses
- **Power Source**: Fission Reactor (for deep space delivery)

### Power Source Notes
- **Inner Galaxy planets**: Solar + Battery works excellently (Andromeda core is very bright)
- **Deep Space / Outer Galaxy**: Must unlock Fission (Kilopower technology)
- **See [[Power Systems]]** for distance-based power requirements
- **See [[Technology Tree]]** for instrument unlock progression

### Visual Indicators
- **Solar satellites**: Sun icons (bright in inner galaxy, may show as dim or locked in deep space)
- **Fission satellites**: Fission icon with energy bar (degrades slowly due to fuel decay)
- **Hybrid satellites**: Both Solar and Fission icons (for flexible power management)

### Andromeda-Specific Quest Lines

See [[#Andromeda Quest Lines]] for detailed quest progression tied to mission completion.

---

## 🚀 Sci-Fi Future World

### Power Sources
All missions require **solar or fusion-powered satellites** (see [[Power Systems]]). Antimatter technology requires completing the Dyson Sphere (see [[Technology Tree]]). Fusion provides the most stable power for high-tech operations.

### Standard Mission Types

#### 1. Construction Contracts
- **Description**: Satellite builds and maintains orbital infrastructure (satellites, towers, relays)
- **Required Instruments**: Drone Controller, Construction Laser, Material Scanner
- **Duration**: 10-30 min (scales by sector difficulty and degradation)
- **Base Difficulty**: Easy-Medium
- **Description for Player**: *"Build this satellite network at the designated location."*
- **Special Requirements**: Drone construction tech, material delivery drones
- **Power Source**: Solar Panels + Battery (inner sector) or Fusion (outer sectors)

#### 2. Data Collection
- **Description**: Satellite gathers scientific data from the alternate universe
- **Required Instruments**: Quantum Sensor, Data Recorder, Universal Translator
- **Duration**: 5-15 min
- **Base Difficulty**: Easy-Medium
- **Description for Player**: *"Collect data from this alternate reality for analysis."*
- **Special Requirements**: Quantum sensor required, stable quantum connection
- **Power Source**: Solar Panels + Battery or Fusion (quantum tech requires stable power)

#### 3. Dyson Sphere Assembly
- **Description**: Satellite places and maintains solar panel segments for the Dyson Sphere
- **Required Instruments**: Solar Collector, Placement Drone, Fusion Injector
- **Duration**: 30-60 min (very long, many segments required)
- **Base Difficulty**: Hard
- **Description for Player**: *"Add this segment to the Dyson Sphere construction."*
- **Special Requirements**:
  - Must complete earlier Dyson Sphere quests (quest chain progression)
  - Requires Solar Panels at star orbit research
  - Multiple satellites needed for large segments (mega-quest mechanic)
- **Power Source**: Fusion Reactor required (must be on star orbit or use zero-point energy)

#### 4. Quantum Computer Assistance
- **Description**: Satellite maintains quantum computer nodes across the universe
- **Required Instruments**: Quantum Processor, Entanglement Sensor, Cooling System
- **Duration**: Continuous (until quantum decoherence)
- **Base Difficulty**: Medium-Hard
- **Description for Player**: *"Maintain the quantum network computing core."*
- **Special Requirements**: Quantum computer research completed
- **Note**: **Persistent mission** - high reward, satellites work faster than normal
- **Power Source**: Fusion Reactor or Zero-Point Energy (Dyson Sphere)

#### 5. Energy Harvesting
- **Description**: Satellite collects energy from the Dyson Sphere or star
- **Required Instruments**: Energy Collector, Fusion Taps
- **Duration**: 20-40 min
- **Base Difficulty**: Very Hard
- **Description for Player**: *"Harvest energy from this star system."*
- **Special Requirements**: Dyson Sphere must be partially complete
- **Power Source**: Fusion Reactor or Zero-Point Energy (Dyson Sphere)

#### 6. Interdimensional Research
- **Description**: Satellite probes the boundaries of different universes
- **Required Instruments**: Quantum Portal Scanner, Dimension Detector
- **Duration**: 25-50 min
- **Base Difficulty**: Extreme
- **Description for Player**: *"Probe the interdimensional membrane for data."*
- **Special Requirements**: Quantum computing research unlocked
- **Power Source**: Fusion Reactor or Quantum Zero-Point Energy

#### 7. Starship Escort
- **Description**: Satellite protects research starships from hostile anomalies
- **Required Instruments**: Defense Array, Energy Shield, Thrusters
- **Duration**: 15-40 min (variable based on enemy spawns)
- **Base Difficulty**: Very Hard
- **Description for Player**: *"Escort the research starship through this danger zone."*
- **Special Requirements**: Defense systems research
- **Power Source**: Fusion Reactor or Energy Shield (for shielded satellites)

#### 8. Time Dilation Study
- **Description**: Satellite measures time flow differences across the universe
- **Required Instruments**: Time Sensor, Chronometer
- **Duration**: 10-20 min
- **Base Difficulty**: Medium-Hard
- **Description for Player**: *"Study time dilation effects in this region."*
- **Special Requirements**: Time research branch
- **Power Source**: Fusion Reactor or Quantum Zero-Point Energy

### Power Source Notes
- **Inner Galaxy**: Solar + Fusion works
- **Outer Galaxy**: Fusion required (solar too weak)
- **Event Horizon / Core Zone**: Must unlock Fusion or Zero-Point Energy (via Dyson Sphere)
- **See [[Power Systems]]** for detailed power requirements per sector
- **See [[Technology Tree]]** for instrument unlock progression
- **See [[Currency]]** for Dyson Sphere completion rewards

### Sci-Fi-Specific Quest Lines

See [[#Sci-Fi Quest Lines]] for detailed quest progression tied to mission completion.

---

## 🐉 Magic Fantasy World

### Unique Fantasy Mechanics
- **No orbital slots** - Fantasy uses **Stables** instead (per-realm dragon housing)
- **Dragons don't take permanent damage** - they just sleep when power is low or age over time
- **No research tree** - progression through companion training (Dragon Handler → Wayreader) and stable expansion
- **Bux uses** - Same as other universes (time skips, cosmetics)
- **Coins** - Siloed per realm

### Capacity System

Fantasy has a **two-tier capacity system**:

#### 1. Stables (Per-Realm, Paid Slots)
- Each realm has its own separate stable capacity
- Stables house dragons between missions
- **Expanded via paid purchases** (buy slots with coins), not research
- Different starting capacity per realm:
  - First Realm: 5 slots
  - Second Realm: 10 slots
  - Third Realm: 15 slots (after Skyward Chart)
  - Fourth Realm: 20 slots (after Skyward Chart)
  - Fifth Realm: 25 slots (after Skyward Chart)
  - Sky Realm: 50 slots

#### 2. Riders / Wayreaders (Global, Research-Based)
- Global pool of riders who coordinate dragons in flight
- **Expanded via research** (Dragon Handler → Wayreaders track)
- Same track across all realms
- A dragon can only be assigned to a mission if there's an available rider

**Capacity Enforcement**:
- When total dragons > (stable capacity + available riders), missions become limited
- Players can expand by:
  1. Buying more stable slots (paid, per-realm)
  2. Unlocking higher rider tiers (research, see [[Technology Tree]])
- Quest progression gates capacity unlocks (see [[#Fantasy Quest Lines]])

### Standard Mission Types

#### 1. Map Commissions (Wayreaders)
- **Description**: Dragon rider draws a map of a specific region for a client
- **Required "Instruments"**: Wayreader Artisan (unlocks "Optical" map), Specialized Dragon types
- **Duration**: 10-30 min (scales by region size and degradation)
- **Base Difficulty**: Easy-Hard
- **Description for Player**: *"Fly a dragon and map this region for a merchant."*
- **Special Requirements**:
  - Must have trained Wayreader Artisan or map commission quest line completed
  - Specific dragon types for terrain (Earth dragon for forests, Fire dragon for volcanoes)
- **Power Source**: Dragon energy (fed at stables)

#### 2. Wayglass Beacon Placement
- **Description**: Dragon delivers a magical rune to create a navigation beacon in the sky
- **Required "Instruments"**: Rune-Smith Wizard, Wayglass Network access
- **Duration**: 5-15 min (rune crafting + delivery)
- **Base Difficulty**: Medium-Hard
- **Description for Player**: *"Craft and deliver this rune to create a navigation beacon."*
- **Special Requirements**:
  - Rune-Smith specialization
  - Must be delivered to correct coordinates (based on map data)
  - Part of the Skyward Chart quest line
- **Power Source**: Dragon energy (fed at stables) + Wayglass Network access

#### 3. Dragon Breeding
- **Description**: Breeding facility creates new dragons with desired traits
- **Required "Instruments"**: Dragon Trainer, Breeding Chamber, Nourishment Supply
- **Duration**: 30-120 min (incubation time varies by dragon type)
- **Base Difficulty**: Very Hard
- **Description for Player**: *"Breed dragons with these magical affinities."*
- **Special Requirements**:
  - Must own breeding facility (paid stable slots)
  - Need mature parent dragons
  - Specific magical affinity combinations (requires research to unlock)
- **Note**: This is in the **Breeding Stable** facility, not mission board

#### 4. Dragon Training
- **Description**: Training academy prepares dragons for specific tasks
- **Required "Instruments"**: Dragon Handler, Training Mounts, Magic Circuits
- **Duration**: 15-60 min (training sessions)
- **Base Difficulty**: Medium-Very Hard
- **Description for Player**: *"Train this dragon for the specified service."*
- **Special Requirements**:
  - Must own training academy (paid slot)
  - Dragon must be mature (not hatchling)
  - Training success rates vary by dragon personality
- **Note**: This is in the **Training Academy** facility, not mission board

#### 5. Cartography Expeditions
- **Description**: Experienced cartographer-dragon pair maps entire regions
- **Required "Instruments"**: Master Wayreader, High-Flying Dragon (Griffin, Dragon, etc.)
- **Duration**: 30-90 min (scales by region size and degradation)
- **Base Difficulty**: Very Hard
- **Description for Player**: *"Lead a cartography expedition across this region."*
- **Special Requirements**:
  - Master Wayreader companion (Level 20+)
  - Dragon with Navigation/Exploration affinity
  - Must have stable capacity available
- **Power Source**: Dragon energy (fed at stables)

#### 6. Astrology Observation
- **Description**: Dragon-wizard pair observes celestial events from high altitude
- **Required "Instruments"**: Wizard with Astronomy skill, Eagle/Sky Dragon
- **Duration**: 20-50 min (observation period)
- **Base Difficulty**: Hard
- **Description for Player**: *"Observe the star patterns from the sky realm."*
- **Special Requirements**:
  - Wizard must have Astronomy skill
  - Dragon must be able to fly to Sky Realm
  - Clear weather required (random check)
- **Power Source**: Dragon energy (fed at stables) + Sky Realm access

#### 7. Portal Maintenance
- **Description**: Wizard maintains magical portals for travelers
- **Required "Instruments"**: Runemaster, Portal Runes, Power Supply
- **Duration**: Continuous (until rune degrades or sabotage)
- **Base Difficulty**: Medium
- **Description for Player**: *"Maintain this portal for travelers."*
- **Special Requirements**: Must have beacon network (Wayglass) established
- **Note**: **Persistent mission** - high reward, dragons work faster than normal
- **Power Source**: Mage's magic reserves (restored at inns)

#### 8. Treasure Hunting
- **Description**: Adventurers search for lost magical artifacts in dungeons
- **Required "Instruments"**: Scout, Artifact Detector, Protection Runes
- **Duration**: 20-40 min
- **Base Difficulty**: Hard-Extreme
- **Description for Player**: *"Search for the lost artifact in this dungeon."*
- **Special Requirements**: Detection magic, protection from dungeon hazards
- **Power Source**: Adventurer stamina (restores between missions)

#### 9. Client Quests
- **Description**: One-off missions from random clients (merchant, adventurer, noble)
- **Required "Instruments"**: Varies by quest
- **Duration**: 5-30 min
- **Base Difficulty**: Easy-Hard (varies by quest)
- **Description for Player**: *"Complete this commission for the client."*
- **Special Requirements**: Varies wildly by quest (check quest description)
- **Unique Aspect**: Random quests, different every day (like event missions)

#### 10. Realm Defense
- **Description**: Protect the realm from invading creatures
- **Required "Instruments"**: Guardian Dragons, Runemasters, Defensive Towers
- **Duration**: 10-30 min (defense phase)
- **Base Difficulty**: Very Hard
- **Description for Player**: *"Defend this realm from the invading beast!"*
- **Special Requirements**:
  - Must have defensive structure built
  - Summon guardian dragons
  - Defeat waves of enemies
- **Power Source**: Realm's defensive magic (auto-renewable)

### Fantasy-Specific Quest Lines

See [[#Fantasy Quest Lines]] for detailed quest progression tied to mission completion.

### Fantasy Mission Rewards Structure

See [[#Fantasy Quest Lines]] for quest rewards. Standard mission rewards scale by realm difficulty:

| Mission Type | First Realm | Second Realm | Third Realm | Fourth Realm | Fifth Realm | Sky Realm |
|--------------|-------------|--------------|-------------|--------------|-------------|-----------|
| Map Commissions | 100 | 300 | 800 | 2,000 | 5,000 | 10,000 |
| Wayglass Beacon Placement | 150 | 400 | 1,000 | 3,000 | 7,000 | 15,000 |
| Cartography Expeditions | 300 | 800 | 2,000 | 5,000 | 10,000 | 20,000 |
| Astrology Observation | 200 | 500 | 1,200 | 3,000 | 6,000 | 12,000 |
| Portal Maintenance | 80/hour | 150/hour | 300/hour | 600/hour | 1,200/hour | 5,000/hour |
| Treasure Hunting | 200 | 500 | 1,500 | 4,000 | 10,000 | 25,000 |
| Realm Defense | 100 | 300 | 800 | 2,000 | 5,000 | 15,000 |
| Client Quests | 50-500 | 100-1,000 | 200-2,000 | 500-5,000 | 1,000-10,000 | 500-20,000 |

**Note**: Sky Realm missions pay significantly more due to difficulty and unique nature.

---

## Mission Flow: Assignment → Execution → Completion → Reward

When a player sends a satellite to a mission, here's what happens:

### 1. Assignment
- Player selects a planet/stable from the available destinations
- Mission board shows available missions for that location
- Player clicks a mission → satellite is **auto-assigned** to it
- Satellite enters **execution phase**

### 2. Execution
- Satellite flies to destination (transit time, varies by universe and distance)
- Arrives at destination planet/stable
- Begins mission execution
- Duration calculated by the formula above (base × degradation)
- During execution, satellite is **unavailable** for new missions

### 3. Completion
- Satellite finishes mission
- Satellite returns to the player's base
- Satellite is added to the "Available Satellites" queue
- **Rewards are distributed**:
  - Coins (per-universe currency, see [[Currency]])
  - Science points (global, contributes to research)
  - Occasional Bux drops (random missions, see [[Currency]])
  - Quest progress (if this mission is part of a quest chain)

### 4. Reward Collection
- Player can collect rewards from returned satellites (instant)
- Or wait and collect multiple at once (manual or time-skip, see [[Currency]])
- Completed mission count updates (for quest progress)

### 5. Cycle Repeats
- Satellite now available for new missions
- Player assigns next mission from the board
- Cycle continues indefinitely (until satellite needs patch/retirement)

---

## Mission Board UI

The mission board is displayed on each planet/destination in the [[Gameplay Loop]] when you click on it.

### Layout (Non-Fantasy / Orbital Universes)

```
┌─────────────────────────────────────────────────────────┐
│                  [Planet Name]                           │
│              Orbital Slots: 3 / 10                      │
├─────────────────────────────────────────────────────────┤
│               Available Missions:                       │
│                                                         │
│  [🗺️ Surface Mapping]           [📡 Comm Relay]         │
│     5 min          10 min         15 min              20 min │
│     🟢 Easy         🟡 Medium       🟠 Hard           🔴 Extreme │
│     +150 coins     +300 coins     +800 coins       +2,000 coins │
│                                                         │
│  [🔬 Atmos Monitoring]          [⚛️ Radiation]          │
│     8 min          12 min        18 min              25 min │
│     🟢 Easy         🟡 Medium      🟠 Hard          🔴 Extreme │
│     +200 coins     +500 coins    +1,200 coins      +3,000 coins │
│                                                         │
│  [🪨 Resource Collection]       [📻 Climate Monitor]    │
│     15 min         25 min        35 min             45 min │
│     🔴 Very Hard    🔴 Very Hard  🔴 Very Hard      🔴 Extreme │
│     +900 coins     +1,800 coins  +4,000 coins      +8,000 coins │
│                                                         │
├─────────────────────────────────────────────────────────┤
│          [Active Quests - Click to View Details]         │
│          [View All Missions]                             │
└─────────────────────────────────────────────────────────┘
```

### Layout (Fantasy / Stable Universes)

```
┌─────────────────────────────────────────────────────────┐
│               [Realm Name] Stables                       │
│             Dragon Slots: 5 / 25                        │
│             Available Riders: 8 / 50                   │
├─────────────────────────────────────────────────────────┤
│              Available Mission Slots:                   │
│                                                         │
│  [🗺️ Map Commissions] (6 slots)                         │
│     5 slots in use → 1 available                       │
│     Duration: 10-30 min (15 min avg)                    │
│                                                         │
│  [🔮 Beacon Placement] (4 slots)                        │
│     3 slots in use → 1 available                       │
│     Duration: 5-15 min (10 min avg)                     │
│                                                         │
│  [📖 Cartography] (3 slots)                             │
│     1 slot in use → 2 available                        │
│     Duration: 30-90 min (60 min avg)                    │
│                                                         │
│  [🦅 Astrology] (2 slots)                               │
│     2 slots in use → 0 available                       │
│     Duration: 20-50 min (35 min avg)                    │
│                                                         │
│  [⚛️ Portal Maintenance] (2 slots)                      │
│     1 slot in use → 1 available                        │
│     Duration: Continuous                               │
│     Rewards: 150 coins/hour (averaged)                  │
│                                                         │
│  [🗡️ Treasure Hunting] (1 slot)                         │
│     0 slots in use → 1 available                       │
│     Duration: 20-40 min (30 min avg)                    │
│                                                         │
├─────────────────────────────────────────────────────────┤
│          [Active Quests - Click to View Details]         │
│          [View All Missions]                             │
└─────────────────────────────────────────────────────────┘
```

### Mission Card Design

```
┌─────────────────────────────────┐
│  [🗺️]  Surface Mapping          │
│         Earth                   │
├─────────────────────────────────┤
│  🌞 Solar Power Required:       │
│     [☀️] [☀️] [☀️]             │
│     2/3 panels operational     │
│  ⏰ Duration: 8 min            │
│  ⚡ Power Cost: 500 units      │
├─────────────────────────────────┤
│  💰 +500 coins  🎖️ +10 Bux     │
│  🧪 +50 science points         │
├─────────────────────────────────┤
│  [🌍 Earth]    [🌙 Moon]       │
│  Available: 5 / 50 capacity   │
│  Completed: 15 / 100 required │
└─────────────────────────────────┘
```

### Capacity Display

- **Orbital Universes**: "Slots: X / Y" where Y is current capacity
- **Fantasy**: Separate display for "Dragon Slots" (stables) and "Riders" (Wayreaders)
- When capacity is full, "Add New Satellite" button becomes disabled

### Filter Options
- **Hide Degraded**: Hide satellites below 25% health (in patch queue)
- **Hide Parked**: Hide satellites not on active missions
- **Hide Completed**: Hide satellites that have finished all missions

### Quest Progress Display

```
## Quest: Earth Network Expansion
**Progress: 2 / 3 missions**

✅ 100 Surface Mapping missions (75% complete)
⏳ 50 Communication Relay missions (0% complete)
⏳ 30 Atmosphere Monitoring missions (0% complete)

**Reward**: 1,000 coins, Moon unlocks!
**Current Reward**: 250 coins (for completed missions only)
```

---

## Instrument Requirements Summary

Each universe's technology tree unlocks instruments progressively (see [[Technology Tree]]). Missions only become available when the required instruments are unlocked.

### Earth Instruments Progression

| Tier | Instruments | Unlock Condition |
|------|-------------|------------------|
| 1 | Optical Camera, Battery | Start |
| 2 | Spectrometer, Solar Efficiency | Reach Moon |
| 3 | Magnetometer, RTG Systems | Reach Mars |
| 4 | Radiation Detector, Hybrid Power | Reach Jupiter |
| 5 | Advanced Bus, Quantum Instruments | Reach Outer Space |

### Andromeda Instruments Progression

| Tier | Instruments | Unlock Condition |
|------|-------------|------------------|
| 1 | Spectrometer, Basic Atmos Sensor | Start |
| 2 | Advanced Optics, Heat Shielding | Reach First Colony |
| 3 | Quantum Sensor, Plasma Shielding | Reach Planet B |
| 4 | Dark Matter Detector, Life Biosensor | Complete Ancient Path |
| 5 | Universal Translator, Fusion Reconstructor | Unlock Sci-Fi |

### Sci-Fi Instruments Progression

| Tier | Instruments | Unlock Condition |
|------|-------------|------------------|
| 1 | Drone Controller, Basic Data Recorder | Start |
| 2 | Advanced Drone, Quantum Sensor | Reach Star System 2 |
| 3 | Construction Laser, Quantum Interface | Reach Star System 3 |
| 4 | Fusion Injector, Fusion Power | Build Dyson Sphere Core |
| 5 | Antimatter Generator, Quantum Teleporter | Dyson Sphere Complete |

### Fantasy Instruments Progression

| Tier | "Instruments" | Unlock Condition |
|------|--------------|------------------|
| 1 | Apprentice Wayreader | Hire first wayreader |
| 2 | Journeyman Wayreader | Level 5 wayreader |
| 3 | Artisan Wayreader | Level 10 wayreader |
| 4 | Rune-Smith | Complete Skyward Chart Phase 1 |
| 5 | Master Runemaster | Complete Skyward Chart |

### Mission Type → Instrument Mapping

| Mission Type | Required Instruments |
|--------------|---------------------|
| Surface Mapping | Optical Camera |
| Atmosphere Monitoring | Spectrometer, Atmospheric Sensor |
| Magnetic Field Studies | Magnetometer |
| Radiation Monitoring | Radiation Detector |
| Resource Collection | Spectrometer, Resource Scanner |
| Communication Relay | Antenna, Transmitter, Battery |
| Space Debris Tracking | Optical Camera, Radar |
| Climate Monitoring | Infrared Sensor, Radar Altimeter |
| Atmosphere Scanning | Spectrometer, Atmospheric Sensor |
| Surface Exploration | Optical Camera, LIDAR, Surface Scanner |
| Ancient Artifact Recovery | Quantum Sensor, Archaeological Scanner |
| Life Detection | Spectrometer, Biosensor, Mass Spectrometer |
| Dark Matter Mapping | Quantum Sensor, Dark Matter Detector |
| Resource Mining | Resource Scanner, Mining Drill |
| Relay Station Maintenance | Antenna, Transmitter, Battery |
| Colony Support | Cargo Bay, Communication Relay |
| Construction Contracts | Drone Controller, Construction Laser |
| Data Collection | Quantum Sensor, Data Recorder |
| Dyson Sphere Assembly | Solar Collector, Fusion Injector |
| Quantum Computer Assistance | Quantum Processor, Entanglement Sensor |
| Energy Harvesting | Energy Collector, Fusion Taps |
| Interdimensional Research | Quantum Portal Scanner, Dimension Detector |
| Starship Escort | Defense Array, Energy Shield |
| Time Dilation Study | Time Sensor, Chronometer |
| Map Commissions | Wayreader Artisan |
| Wayglass Beacon Placement | Rune-Smith Wizard |
| Dragon Breeding | Dragon Trainer, Breeding Chamber |
| Dragon Training | Dragon Handler |
| Cartography Expeditions | Master Wayreader |
| Astrology Observation | Wizard (Astronomy), Eagle Dragon |
| Portal Maintenance | Runemaster |
| Treasure Hunting | Scout, Artifact Detector |
| Client Quests | Varies (see individual quest) |
| Realm Defense | Guardian Dragons, Runemasters |

---

## Linking to Other Mechanics

This page links to:

- **[[Gameplay Loop]]**: How missions fit into the overall loop
- **[[Technology Tree]]**: Which instruments are available per universe
- **[[Power Systems]]**: Power requirements for each mission type
- **[[Orbital Capacity]]**: How capacity limits mission assignment (per-universe except Fantasy)
- **[[Currency]]**: What rewards players earn
- **[[Companions]]**: How companions assist with missions
- **[[Satellite Durability]]**: How mission wear affects satellites
- **[[Story Quests]]**: Main quest lines that tie missions together

---

## Future Expansions (TODO)

- [ ] Add event missions (limited-time bonuses)
- [ ] Add dynamic mission pool (missions change based on events)
- [ ] Add mission-specific companions (special abilities)
- [ ] Add mission difficulty modifiers (equipment bonuses)
- [ ] Add daily/weekly mission bonuses
- [ ] Add mission-based achievements
- [ ] Add prestige missions (reset capacity, bonus rewards)

---

## References

- Pocket Trains mission system inspiration
- Real satellite mission systems (Earth observation)
- Science fiction space opera mission concepts
- Fantasy cartography traditions (Wayglass, Wayreads)