# Gameplay Loop

This page describes the core gameplay loop of the Satellite Tycoon game. The game follows a streamlined tycoon loop adapted for space operations, with four distinct universes, each with unique mechanics.

> [[Production Facility]] | [[Launch System]] | [[Orbital Capacity]] | [[Missions]] | [[Technology Tree]] | [[Satellite Durability]] | [[Currency]] | [[Story]] | [[Companions]] | [[Laboratory]]

---
#TBD - everything here is hallucinated - to check if it's viable
## Core Loop Overview

The game begins empty, with no satellites deployed. Players must build and launch satellites to start earning income and progressing through the game. The loop follows a continuous cycle across all universes:

```
┌─────────────────────────────────────────────────────────────────┐
│                        START (Empty Universe)                   │
│     No satellites in orbit, no missions available               │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                       PRODUCTION                               │
│  [Build Satellites] → [Add to Launch Queue]                     │
│     Build from components (components: bus, power, instruments) │
│     Wait time: [Display current build time based on tech]      │
│     Skip with Bux: [Instant Build]                             │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                         LAUNCH                                │
│  [Select Destination Planet]                                   │
│  [Rocket/Portal Selection]                                     │
│  [Launch] → Transit begins                                     │
│  Pay: Launch cost (Coins, siloed per universe)                 │
│  Bux can be used for launch time skip                         │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                         TRANSIT                               │
│  [Loading... transit animation]                                 │
│  Distance: [XX,XXX km]                                         │
│  Duration: [X min]                                             │
│     - Solar System: Realistic transit times scaled down       │
│     - Andromeda: Instant wormhole (1-5 min)                   │
│     - Sci-Fi: Instant quantum transit (1-10 min)             │
│     - Fantasy: Instant portal (instant)                      │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                        ARRIVAL                               │
│  [Satellite Name] has arrived at [Planet]!                    │
│  [Animation: Landing/Deployment]                              │
│  [Check for arrival bonuses]                                  │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                     MISSION ASSIGNMENT                       │
│  New satellite appears on [[Mission Board]]                   │
│  [Filter by instruments]                                      │
│  [Auto-assign to fastest missions] ← Recommended               │
│  Or: [Manually assign missions]                               │
│  Or: [Add to queue for auto-assign]                           │
│  [Orbit slots used: X / Y]                                    │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                    MISSION EXECUTION                        │
│  [Satellites begin missions - runs automatically]            │
│     - Duration: [Base time × (1 + degradation penalty)]      │
│     - Power degrades/recharges based on [[Power Systems]]     │
│     - Health degrades slightly per mission (low-stress)       │
│     - Fantasy: Dragon enters sleep cycle when low energy     │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                     MISSION COMPLETION                    │
│  "Mission complete! Rewards received."                       │
│  Rewards:                                                     │
│     💰 Coins (siloed per universe)                           │
│     🎖️ Bux (premium, shared across universes)             │
│     🧪 Science Points (global, unlocks tech)              │
│     💎 Bux drops (random, cosmetic unlocks)               │
│     📖 Story progress (quest chains)                      │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                     SATELLITE RETURN                      │
│  Satellite returns to base                                     │
│  Health: [X%] (may have degraded)                            │
│  Power: [X%] (may need recharge)                             │
│  Status: [Ready / Needs Patch / Ready to Launch]           │
└─────────────────────────────────────────────────────────────────┘
                              │
                 ┌────────────┴────────────┐
                 ▼                        ▼
┌─────────────────────────────────┐  ┌─────────────────────────────────────┐
│     DEGRADATION HANDLING      │  │     REPEAT / EXPAND              │
│     [Earth: Manual patch]     │  │  [Build more satellites]        │
│     [Andromeda: Auto-fix]     │  │  [Launch to new planets]         │
│     [Sci-Fi: AI self-heal]    │  │  [Unlock new universes]          │
│     [Fantasy: Sleep recharge] │  │  [Expand stables capacity]       │
│                              │  │  [Research tech upgrades]         │
└─────────────────────────────────┐  └─────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                        REWARD COLLECTION                    │
│  [Universal timer: 24h rolling]                                │
│  [Claim completed missions]                                   │
│  [Collect currency, science, story rewards]                   │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                          CONTINUE                        │
│       Loop repeats with expanded universe                   │
│       More satellites in orbit, faster completion times     │
│       More planets to explore, more missions available       │
└─────────────────────────────────────────────────────────────────┘
```

---

## Phase 1: Production - Building Satellites

The first step in any new game session is to build satellites from components in your **[[Production Facility]]**. Since the game starts empty, this is your primary activity.

### Production Flow

```
┌─────────────────────────────────────────────────────────────┐
│         PRODUCTION FACILITY                                    │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  Step 1: Choose Satellite Template                            │
│     Select pre-built template or create custom                 │
│                                                              │
│  Step 2: Select Components                                    │
│     Bus/Platform: Core structure                              │
│     Power Source: Solar / RTG / Fusion / Dragon Energy        │
│     Instruments: Choose from unlocked instruments            │
│                                                              │
│  Step 3: Review Configuration                                 │
│     Estimated build time: [X min]                            │
│     Cost: [X] coins                                          │
│     Destination capacity: [X / Y slots]                     │
│                                                              │
│  Step 4: Add to Queue                                         │
│     [Add to Build Queue]                                      │
│     Skip with Bux: [Instant Build] 10 Bux/satellite          │
│                                                              │
│  Step 5: Monitoring                                           │
│     [Progress Bar: [████░░░░]]                               │
│     [Cancel Build] (if queue space available)                 │
│                                                              │
│  Step 6: Completed! Ready to Launch                           │
│     [Move to Launch Queue]                                    │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

### Component System

Satellites are built from modular components:

| Component | Purpose | Production Cost | Notes |
|-----------|---------|-----------------|-------|
| Bus/Platform | Main structure, holds instruments | Increases with tier | Tier 1: Basic |
| Solar Panel | Power generation (Solar System only) | Increases with tier | Less efficient farther from sun |
| RTG | Nuclear power (deep space) | Higher cost, no sun dependency | Required for outer planets |
| Fusion Drive | Power generation (Sci-Fi) | Very high cost | Self-sufficient power source |
| Dragon Energy | Magical power (Fantasy) | Low cost, requires stables | Recharges through feeding |
| Instruments | Mission capabilities | Per-instrument unlock | See [[Technology Tree]] |
| Thrusters | Propulsion, station keeping | Affects transit duration | Upgrades reduce transit time |

### Production Times by Universe

Production time varies based on technology level and universe:

| Universe | Base Build Time (Tier 1) | With Max Tech (Tier 5+) | Speed Multiplier |
|----------|-------------------------|------------------------|------------------|
| Solar System | 2-5 min | 30 seconds - 1 min | 2× faster |
| Andromeda | 3-8 min | 45 seconds - 1.5 min | 2.5× faster |
| Sci-Fi | 5-15 min | 1 - 4 min | 4× faster |
| Fantasy | 10-60 min | 2-15 min | 6× faster |

### Production Queue

Limited queue slots for building satellites:

```
┌─────────────────────────────────────────────────────────────┐
│            PRODUCTION QUEUE ([Max 5 slots])                 │
├─────────────────────────────────────────────────────────────┤
│  Slot 1: [Basic Earth Sentinel] → Building [███░░░] 40%    │
│  Slot 2: [Advanced Earth Sentinel] → Building [█████░░] 60% │
│  Slot 3: [Explorer Drone] → Building [███████] 90%          │
│  Slot 4: [Ready - Waiting for launch]                       │
│  Slot 5: [Ready - Waiting for launch]                       │
└─────────────────────────────────────────────────────────────┘
```

Queue management:
- **Build in order**: Earlier queue positions start first
- **Cancel & rebuild**: Free up queue slots by canceling (no refund)
- **Priority**: Use Bux to reorder queue priority

### Time-Skip Options

Premium currency (Bux) can be used to skip production:
- **Instant Build**: 10 Bux per completed satellite
- **Queue Reorder**: 5 Bux to move a satellite to front of queue

---

## Phase 2: Launch - Sending Satellites to Orbit

Once satellites are built and ready, you can launch them to their destination planets.

### Launch Process

```
┌─────────────────────────────────────────────────────────────┐
│                   LAUNCH PAD                                 │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  Step 1: Select Satellites from Queue                         │
│     [Drag satellites to launch]                              │
│     Max launches per session: [5]                            │
│                                                              │
│  Step 2: Select Transport Method                             │
│     - Chemical Rocket: Standard, moderate cost               │
│     - Ion Drive: Slower but cheaper                           │
│     - Fusion Thruster: Fast and expensive (Sci-Fi+)          │
│     - Wormhole: Instant (Andromeda)                           │
│     - Quantum Teleporter: Fast (Sci-Fi)                      │
│     - Portal: Instant (Fantasy)                              │
│                                                              │
│  Step 3: Set Destination                                     │
│     Select planet/system from unlock tree                    │
│     Check orbital capacity: [X / Y slots]                    │
│     [Destination not available] ← If at capacity            │
│                                                              │
│  Step 4: Pay Launch Cost                                     │
│     Coins: [Amount] (siloed per universe)                    │
│     Bux: [Optional time skip - 5 Bux per satellite]          │
│                                                              │
│  Step 5: [LAUNCH!]                                           │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

### Launch Costs by Destination

| Universe | Destination | Launch Cost (Coins) | Transport Type | Unlock Requirement |
|----------|-------------|---------------------|----------------|-------------------|
| Solar System | Earth Orbit | Free | N/A (base) | Starting point |
| Solar System | Moon | 100 | Chemical rocket | Unlock Earth |
| Solar System | Mars | 500 | Chemical rocket | Unlock Moon |
| Solar System | Jupiter | 1,500 | Multi-stage rocket | Unlock Mars |
| Solar System | Outer Belt | 3,000 | Ion drive | Unlock Jupiter |
| Andromeda | First Colony | 10,000 | Wormhole | Reach 1,000 Earth satellites |
| Andromeda | Other Planets | 1,000 | Wormhole | Unlock First Colony |
| Sci-Fi | First Star System | 20,000 | Quantum Teleporter | Unlock Andromeda |
| Sci-Fi | Other Systems | 5,000 | Quantum Teleporter | Unlock First Star |
| Fantasy | First Realm | 5,000 | Quantum Portal | Complete Skyward Chart |
| Fantasy | Other Realms | 1,000 | Portal | Unlock First Realm |

### Launch Restrictions

- **Orbital Capacity**: Must have available slots at destination (see [[Orbital Capacity]])
- **Universe Progression**: Must complete previous universe's main goal
  - Solar System → Andromeda: Reach 1,000 operational satellites
  - Andromeda → Sci-Fi: Reach 5,000 operational drones
  - Sci-Fi → Fantasy: Complete Dyson Sphere construction
  - Fantasy: Complete Skyward Chart for all realms
- **Technology Requirements**: Some planets/systems require R&D tiers to reach
- **Capacity Limit**: Maximum [100] launch satellites per session

### Launch Flow

```
┌─────────────────────────────────────────────────────────────┐
│  SELECTED SATELLITES:                                       │
│  [Earth Sentinel Level 3] - Solar + Camera + Spectrometer   │
│  [Explorer Drone Level 1] - Solar + Magnetometer            │
├─────────────────────────────────────────────────────────────┤
│  TRANSPORT: [Wormhole]                                     │
│  DESTINATION: [Andromeda Colony]                           │
│  CAPACITY: [42 / 100 slots used, 58 available]              │
│  COST: [2,000 Coins]                                       │
│  TRANSIT TIME: [3 minutes]                                 │
├─────────────────────────────────────────────────────────────┤
│  [LAUNCH!]                                                 │
│     - Coins deducted: -2,000                               │
│     - Satellites sent to transit                           │
│     - Launch confirmed!                                   │
└─────────────────────────────────────────────────────────────┘
```

### Time-Skip Options

- **Instant Launch**: 5 Bux per satellite
  - Skips launch processing and transit time
  - Satellite arrives immediately at destination
- **Skip Queue**: 10 Bux to move satellite to front of queue

---

## Phase 3: Transit - Satellites Journey Through Space

Satellites travel from launch origin to destination planet.

### Transit Visualization

```
┌─────────────────────────────────────────────────────────────┐
│              TRANSIT ANIMATION                               │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  Satellite: [Your Earth Sentinel]                            │
│  From: Earth | To: Andromeda Colony                         │
│  Distance: 2,500,000,000 km                                  │
│  Transit Time: [██████████░░░░░░░] 67%                      │
│  ETA: [2 minutes 15 seconds]                                 │
│                                                              │
│  [Companion Dialogue]                                        │
│     "The wormhole ripples around us! Hold tight!"          │
│     - [Tap for more]                                         │
│                                                              │
│  [Visual Effects]: [████████████████████████████████████]  │
│     - Stars streaking by                                    │
│     - Wormhole tunnel effect                                │
│     - Destination planet approaching                       │
│                                                              │
│  [Skip Remaining Transit]: 2 Bux                          │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

### Transit Duration by Universe

Realistic transit times compressed for gameplay:

| Universe | Real Distance | Game Transit Time | Notes |
|----------|---------------|-------------------|-------|
| Solar System | Varies by km | 5 min (Moon) - 15 min (Mars) - 30 min (Jupiter) - 60 min (Outer Belt) | Distance-based |
| Andromeda | ~2.5 million ly | 1-5 min (wormhole) | Instant travel via wormhole tech |
| Sci-Fi | Variable light-years | 1-10 min (quantum transit) | Instant travel via quantum tech |
| Fantasy | Within realm | Instant (portal) | Instant travel via magic |

Transit time scales with:
- **Distance**: Outer planets/systems take longer
- **Thruster Tier**: Better thrusters = faster transit
- **Satellite Quality**: Better-built satellites move faster

---

## Phase 4: Arrival - Satellite Deploys to Planet

When transit completes, the satellite is deployed on the destination planet.

### Arrival Process

```
┌─────────────────────────────────────────────────────────────┐
│                     ARRIVAL NOTIFICATION                   │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  🎉 [Your Earth Sentinel] has arrived at [Andromeda Colony]! │
│     Transit complete!                                       │
│                                                              │
│  [Transit Statistics]                                       │
│     Duration: [3 minutes]                                    │
│     Fuel Consumed: [12%]                                     │
│     Health Loss: [1-2%]                                     │
│     Charge: Solar recharged: [80%]                         │
│                                                              │
│  [Transit Achievement]                                      │
│     "First Contact!" (if first satellite to this planet)   │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

### Deployment to [[Mission Board]]

The arriving satellite appears on the mission board for its destination planet:

```
┌─────────────────────────────────────────────────────────────┐
│               MISSION BOARD - Andromeda Colony              │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  [Satellite Slot 1]                                         │
│     [Your Earth Sentinel]                                   │
│     Health: [100%] | Power: [80%] | Status: [Ready]        │
│     Instruments: ☀️ Camera, ☀️ Spectrometer                │
│                                                              │
│  [Available Missions - Filtered by instruments]             │
│     [ ] Surface Mapping (8 min, 200 Coins, 10 Science)     │
│     [ ] Atmosphere Analysis (5 min, 150 Coins, 15 Science) │
│     [ ] [Requires more instruments]                        │
│                                                              │
│  [Orbit Capacity: 43 / 100 slots]                          │
│                                                              │
│  [Quick Actions]                                           │
│     [Auto-assign all missions] ← Recommended                │
│     [Assign manually]                                      │
│     [Add to queue]                                         │
│     [Retire]                                               │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

### Mission Assignment Options

When a satellite arrives, you have assignment choices:

1. **Auto-Assign (Recommended for new players)**
   - Automatically assigns to missions with shortest estimated completion time
   - Prioritizes missions matching all available instruments
   - Respects power requirements
   - Avoids degraded satellites (can filter option)

2. **Manual Assignment**
   - Click individual missions to assign
   - Drag-and-drop satellite to mission
   - See estimated completion time before assigning

3. **Queue for Later**
   - Add satellite to mission queue
   - Will auto-assign when current mission completes
   - Useful for planning ahead

### Assignment Rules

- **Instrument Match**: Satellite can only accept missions requiring instruments it carries
- **Power Requirement**: Satellite must have sufficient power level for mission type
- **Orbit Slot Usage**: Each active mission occupies one orbital slot
- **Minimum Requirements**: Some missions require minimum satellite level
- **Universe Specific**:
  - Solar System: Standard orbital mechanics
  - Andromeda: Artifact-focused missions
  - Sci-Fi: High-tech instrument missions
  - Fantasy: Only dragons (in stables), can perform all mission types

### Degradation & Power on Arrival

```
┌─────────────────────────────────────────────────────────────┐
│        SATELLITE STATUS ON ARRIVAL                          │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  Health: [98%] ← Degraded by [2%] during transit            │
│  Power: [80%] ← Recharged by solar / battery                │
│  Status: [Ready] (no degradation issues)                   │
│                                                              │
│  [Actions]                                                  │
│     [Accept Mission]                                        │
│     [Patch Health] (1 R&D slot, 5 science points)          │
│     [Add to Launch Queue] (send to new destination)        │
│     [Retire] (remove from service, +50 coins refund)       │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

---

## Phase 5: Mission Execution - Satellites Work

Assigned satellites begin their missions and work automatically. This is where the tycoon loop runs itself.

### Mission Progression

```
┌─────────────────────────────────────────────────────────────┐
│              SATELLITES ON ORBIT - [Planet Name]            │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  Satellite 1: [Earth Sentinel]                               │
│     Status: 🟢 Working                                       │
│     Mission: [Surface Mapping]                               │
│     Progress: [██████████░░░░░░░] 75%                      │
│     Estimated ETA: [2 min 30 sec]                            │
│     Health: [96%] | Power: [72%]                           │
│     [View Orbit - Zoom in]                                  │
│                                                              │
│  Satellite 2: [Explorer Drone]                               │
│     Status: 🔴 Degrading (Power 30%)                         │
│     Mission: [Atmosphere Analysis]                           │
│     Progress: [████░░░░░░░░░░] 30%                         │
│     Estimated ETA: [5 min 45 sec] (slowed by degradation)  │
│     Health: [85%] | Power: [30%]                           │
│     [Patch Power] (1 R&D slot)                             │
│                                                              │
│  Satellite 3: [Advanced Probe]                               │
│     Status: ⚫ Inactive (Health 18%)                         │
│     Mission: [Resource Mining]                               │
│     Status: ⚠️ Needs patch (Health < 25%)                  │
│     Health: [18%] | Power: [45%]                           │
│     [Patch Queue] (Earth only)                             │
│     [Retire]                                               │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

### Mission Duration Formula

Mission duration scales with planet difficulty, satellite degradation, and power level:

**Base Duration = Base Time × (1 + Degradation Penalty) × Power Modifier**

#### Base Time by Mission Type (per planet)

| Mission Type | Mercury | Venus | Earth | Mars | Jupiter | Andromeda | Sci-Fi | Fantasy |
|--------------|---------|-------|-------|------|---------|----------|-------|---------|
| Mapping | 3 min | 5 min | 8 min | 12 min | 25 min | 15 min | 10 min | 5 min |
| Monitoring | 4 min | 6 min | 10 min | 15 min | 30 min | 20 min | 15 min | 8 min |
| Mining | 8 min | 12 min | 20 min | 35 min | 60 min | 40 min | 25 min | 12 min |
| Construction | 15 min | 20 min | 35 min | 60 min | 120 min | 80 min | 50 min | 20 min |

#### Degradation Penalty Formula

Degradation penalty increases with mission count, capped at +200%:

```
Penalty Tier (by mission count): 0%, 5%, 10%, 15%, 20%
Base Penalty per mission: 2-8% (varies by mission type)
Critical Damage Chance: 3-5% (extra damage event)

Effective Penalty = Base Penalty × Mission Count (capped at 200%)
Effective Duration = Base Duration × (1 + Effective Penalty)
```

**Example**: A satellite on its 5th mission:
- Base penalty: 5% per mission
- 5 missions × 5% = 25% degradation
- Critical damage: +5-10% chance of extra damage
- Final multiplier: 1.3x (125% duration)

**Maximum**: At 10+ missions, penalty caps at 200% (3x duration)

**Special Note**: Below 25% health, satellite stops taking new missions and enters patch queue

#### Power Modifier

Higher power = faster mission execution:

| Power Level | Speed Modifier |
|-------------|----------------|
| ⭐⭐⭐⭐⭐ (5 stars) | 1.2× faster |
| ⭐⭐⭐⭐ (4 stars) | 1.1× faster |
| ⭐⭐⭐ (3 stars) | 1.0× (base speed) |
| ⭐⭐ (2 stars) | 0.9× slower |
| ⭐ (1 star) | 0.8× slower |

### Power System Integration

See [[Power Systems]] for detailed power mechanics:

**Solar System**: Solar + battery recharge
- Recharge rate depends on distance from sun
- Eclipse events cause temporary drain
- RTG (nuclear) bypasses solar limitation

**Andromeda**: Battery + auto-repair
- Background recharge (no sun dependency)
- Auto-fix degradation (no player input)
- No power issues in gameplay loop

**Sci-Fi**: Fusion + AI healing
- Fusion power (independent of sun)
- AI self-repairs (no player input)
- No degradation impact

**Fantasy**: Dragon energy cycle
- Dragons sleep when energy low
- Wake on feeding (1 Bux, 15 min) OR stable expansion (paid slots)
- Energy regens naturally over time
- No degradation, no failures

### Visual: Active Orbit View

Click on any satellite for live orbit view:

```
┌─────────────────────────────────────────────────────────────┐
│               ORBIT VIEW - [Earth Sentinel]                 │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  [Orbit Path Animation]                                     │
│     [Orbit around planet]                                   │
│     [Current position indicator]                            │
│                                                              │
│  Current Mission: [Surface Mapping]                         │
│     Progress: [███████████░░] 80%                          │
│     Estimated Completion: [45 sec]                          │
│                                                              │
│  Health: [94%] → [92%] → [90%] (degrading)                 │
│  Power: [68%] → [70%] (recharging)                         │
│                                                              │
│  [Skip Mission] [Patch Health] [Skip Power]               │
│  [Return to Mission Board]                                 │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

---

## Phase 6: Completion - Rewards and Return

When a mission completes, rewards are distributed and the satellite returns to base.

### Completion Event

```
┌─────────────────────────────────────────────────────────────┐
│                   MISSION COMPLETE!                          │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  🎉 "Congratulations! [Your Earth Sentinel]                 │
│   completed the [Surface Mapping] mission on                │
│   [Earth]!"                                                 │
│                                                              │
│  💰 Coins: +[200] (added to Earth Coins)                   │
│  🎖️ Bux: +[5] (50% chance, from this mission)             │
│  🧪 Science: +[30] (added to global Science Pool)          │
│  💎 Bux: +[2] (possible return journey bonus)             │
│                                                              │
│  📖 Quest Progress: [Mapping Mars: 4/5]                  │
│     [New beat unlocked: "The Martian Dawn"]               │
│                                                              │
│  [Collect All Completed Missions]                          │
│     [Universal Timer: 24h rolling]                       │
│     [Queue next mission]                                   │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

### Reward Distribution

| Reward Type | Source | Usage |
|-------------|--------|-------|
| **Coins (Planet-specific)** | Mission completion | Production, launch costs |
| **Science Points** | All mission completions | Technology Tree research |
| **Bux (Premium)** | 50% chance on random missions | Time skips, cosmetics only |
| **Bux (Return Journey)** | Random (2-5 Bux) | Time skips, cosmetics only |
| **Story/Quest Rewards** | Quest chain completion | Narrative progression, unlocks |
| **Quest Chain Bonuses** | Complete all missions in chain | Large currency + unlock next phase |

**Important Notes**:
- Coins are **siloed per universe** (Earth Coins ≠ Andromeda Coins)
- Bux is **shared globally** across all universes
- Science Points are **global** and apply to all universes' tech tree
- **Bux cannot be exchanged** to coins (prevents pay-to-win)
- **Progression is unlocked, not purchased** (premium can't buy content)

### Satellite Return to Base

```
┌─────────────────────────────────────────────────────────────┐
│              SATELLITES RETURNED TO BASE                   │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  [Your Earth Sentinel]                                      │
│     Health: [89%] (degraded by [11%] on 6 missions)        │
│     Power: [55%] (needs [20 min] recharge)                 │
│     Status: [Needs Patch] (Health < 25% = ⚠️)           │
│     Instruments: ☀️ Camera, ☀️ Spectrometer             │
│     Level: 5                                                 │
│     [Reassign Mission] [Retire] [Add to Queue]            │
│                                                              │
│  [Explorer Drone]                                           │
│     Health: [95%] (healthy)                                │
│     Power: [70%] (recharging)                              │
│     Status: [Ready for Mission]                           │
│     Instruments: ☀️ Camera, ☀️ Magnetometer            │
│     [Reassign Mission]                                      │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

---

## Phase 7: Degradation Handling - Universe-Specific

When satellites degrade, they need maintenance. The method varies by universe.

### Solar System (Manual Maintenance)

```
┌─────────────────────────────────────────────────────────────┐
│           Solar System - Manual Patch Queue              │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  Degraded Satellites [X / Max 10]:                          │
│     [Your Earth Sentinel] - Health: 22%                  │
│     [Explorer Drone] - Health: 15%                         │
│                                                              │
│  [Request R&D Patch] ← Player must manually queue          │
│     [Patch Slot 1]: [Your Earth Sentinel]                │
│     [Patch Slot 2]: [Explorer Drone]                      │
│     [Empty] [Empty] [Empty] [Empty] [Empty] [Empty]      │
│                                                              │
│  [Patch Priority: Health > Power]                        │
│  [Skip Patch: 3 Bux per satellite]                      │
│  [Cancel Pending Patches]                               │
│                                                              │
│  Patch Duration: [5-20 min] (depends on R&D tier)       │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

**Patch System**:
- R&D slot required (5 slots, queue-based)
- Patch cost: 5 Science Points per satellite
- Patch duration: 5-20 min (decreases with R&D tier)
- Patch restores ~30% health per patch
- After 2-3 patches, satellite is "fully patched" to 100%
- Manual queue management (no auto-patch)

### Andromeda Galaxy (Auto-Repair)

```
┌─────────────────────────────────────────────────────────────┐
│            Andromeda - Auto-Repair System              │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  Degradation is DETECTED automatically and FIXED:          │
│     • Satellites automatically enter repair mode            │
│     • R&D automatically creates repair patches             │
│     • Satellites resume when repaired                      │
│     • Player: CHECK auto-patch status, approve if needed    │
│                                                              │
│  [Auto-Patch Settings]:                                    │
│     [✓] Auto-detect degradation                           │
│     [✓] Auto-request patches                              │
│     [✓] Auto-queue repairs                                │
│     [ ] Require player approval for serious issues       │
│                                                              │
│  [Manual Override]:                                        │
│     [Emergency Patch Request] - [X / 3] slots             │
│     [Patch Priority Queue]                                 │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

**Patch System**:
- No player input needed (toggleable)
- Degradation detected on mission completion
- R&D queue auto-fills with repairs
- Repair completes before satellite is reassigned
- Optional manual override for control

### Sci-Fi Future (AI Self-Healing)

```
┌─────────────────────────────────────────────────────────────┐
│               Sci-Fi - AI Self-Healing System          │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  Satellites SELF-REPAIR over time with AI assistance:      │
│     • Health regenerates naturally (0.5% per min)          │
│     • Full recovery: [X min] at current degradation       │
│     • AI technicians monitor fleet health                 │
│                                                              │
│  [AI Healer Status]:                                       │
│     [Active] - Healing [X] satellites                      │
│     [Healing Rate]: [20% per hour]                        │
│     [Research Unlocked]: AI Self-Healing v[Level]          │
│                                                              │
│  [Manual]: No action needed (true autopilot)            │
│     [Optional: Speed up healing - 10 Bux]               │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

**Healing System**:
- Continuous regeneration (0.5-1% health per minute)
- No R&D slots needed
- Can "buy time" with Bux (instant heal for 5 Bux)
- Full recovery at 100% health

### Fantasy World (Dragon Cycle)

```
┌─────────────────────────────────────────────────────────────┐
│             Fantasy - Dragon Energy Cycle              │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  Dragons don't have health - they have ENERGY:            │
│     • Dragons enter sleep cycle when energy depleted       │
│     • Sleeping dragons: Cannot work, cannot complete       │
│     • Wake triggers:                                         │
│       1. Feeding - 1 Bux (instant wake)                   │
│       2. Stable Expansion - 150 coins (adds slot)        │
│       3. Natural Regeneration - 60 min (free)           │
│                                                              │
│  [Stable Management]:                                     │
│     [Realms] [Available Stables: X / Paid Slots]         │
│     [Buy Stables]: [150 coins] per realm                │
│     [Free Stables]: Occasional events                 │
│                                                              │
│  [Energy Regeneration]:                                  │
│     • Sleeping dragons: Wake on feeding or time           │
│     • Active dragons: Natural energy regen (slow)        │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

**Dragon Energy System**:
- See [[Power Systems]] for detailed dragon mechanics
- No degradation = no failures = no permanent loss
- Stables are **paid per-realm slots**
- Riders (Wayreaders) are **global research progression**
- Two separate progression tracks

### Degradation Summary by Universe

| Universe | Degradation | Mitigation | Player Action |
|----------|-------------|------------|---------------|
| Solar System | 2-8% per mission, critical events | Manual R&D patches | Queue patches, wait for repair |
| Andromeda | 2-8% per mission, critical events | Auto-repair via R&D | Approve patches or let auto-fix |
| Sci-Fi | 2-8% per mission, critical events | AI self-healing | No action (or buy healing) |
| Fantasy | None (energy only) | Natural regeneration | Feed dragons or wait |

---

## Phase 8: Reward Collection - Universal Timer

Completed missions and rewards are collected on a rolling 24-hour timer.

### Mission Completion Queue

```
┌─────────────────────────────────────────────────────────────┐
│             REWARD COLLECTION QUEUE                   │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  Completed Missions [X / Y waiting]:                     │
│     1. [Surface Mapping - Earth] - 0 min remaining       │
│     2. [Atmosphere Analysis - Mars] - 15 min remaining    │
│     3. [Mapping - Moon] - 25 min remaining              │
│     4. [Coverage Mission - Andromeda] - 45 min remaining │
│     ...                                                   │
│                                                              │
│  Pending Rewards:                                        │
│     Coins: Earth +[500] Andromeda +[300]                │
│     Science: +[50] Global                             │
│     Bux: +[15] (50% chance, some pending)              │
│     Quest Progress: [Mapping Mars: 5/5]              │
│     [Quest Complete: "The Martian Dawn"]            │
│                                                              │
│  [Claim All Ready Rewards]                          │
│     Only collects rewards with 0 min remaining          │
│                                                              │
│  [Claim All Rewards]                             │
│     [Universal timer: 24h rolling]                    │
│     [Skip timer with Bux: 100 Bux]                   │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

### Reward Timing

- **Standard missions**: Rewards distributed when mission completes
- **Quest chain missions**: Rewards distributed when chain completes
- **Universal timer**: 24-hour rolling timer for claiming:
  - Rewards queue until claimed
  - If you're offline for days, rewards stack
  - Can claim all at once when you return
  - **No time pressure** - this is your convenience, not a hard limit

### Claim Process

```
┌─────────────────────────────────────────────────────────────┐
│                 CLAIM REWARDS                       │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  Ready to Claim (Timer Expired):                         │
│     🪙 +[500] Earth Coins                               │
│     🪙 +[300] Andromeda Coins                           │
│     🎖️ +[50] Bux (Premium)                             │
│     🧪 +[100] Science Points                           │
│     📖 Quest: "Mapping Mars" COMPLETE!                │
│        - Unlock: "Dawn of the Red Planet" story       │
│        - Reward: [Bonus 500 Earth Coins]              │
│     🎁 Cosmetic: [Limited Time Emblem]                  │
│                                                              │
│  Still Waiting (Timer Active):                          │
│     [Some missions still in queue]                     │
│     [Pending Bux drops]                               │
│                                                              │
│  [Claim Ready] [Skip Timer: 100 Bux]                 │
│                                                              │
│  [Collect & Continue]                                  │
│     - Rewards added to inventory                       │
│     - Quests logged as complete                         │
│     - Progression saved                                │
│     - Satellite becomes available again                │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

---

## Phase 9: Repeat - Expansion and Growth

The loop continues as you expand your universe presence.

### The Complete Loop Cycle

```
START GAME (Empty Universe)
    │
    ▼
[Build Satellites] → Production Phase
    │ [Wait: 1-60 min | Skip: 10 Bux]
    │
    ▼
[Launch to Planet] → Launch Phase
    │ [Pay Launch Cost | Skip: 5 Bux]
    │ [Check: Orbital Capacity]
    │
    ▼
[Satellite Travels] → Transit Phase
    │ [Wait: 5-60 min (distance based) | Skip: 2 Bux]
    │
    ▼
[Arrive at Planet] → Arrival Phase
    │ [Animation: Landing]
    │
    ▼
[Assign to Mission Board] → Assignment Phase
    │ [Auto-sort by: Estimated Completion Time] ← Recommended
    │ [Manually assign if preferred]
    │ [Filter: Hide degraded satellites (optional)]
    │ [Uses: X / Y orbital slots]
    │
    ▼
[Satellites Work] → Execution Phase
    │ [Wait: Base time × (1 + degradation) | Skip: 1 Bux/min]
    │ [Power degrades/recharges based on [[Power Systems]]]
    │ [Health degrades: 2-8% per mission | Critical: 3-5%]
    │ [Fantasy dragons sleep when low energy]
    │
    ▼
[Complete Mission] → Completion Phase
    │ [Wait: Completion event]
    │
    ▼
[Receive Rewards] → Collection Phase
    │ [Universal timer: 24h rolling]
    │ [Claim rewards]
    │ [Collect: Coins, Bux, Science, Quest Progress]
    │
    ▼
[Satellite Returns to Base]
    │ Health: [Degraded X%] | Power: [Needs Recharge]
    │
    ▼
[Cycle Repeats!]
    │ [Wait for satellites to be ready]
    │ [Build more satellites]
    │ [Launch to new planets]
    │ [Expand stables (Fantasy)]
    │ [Research new tech]
    │
    ▼
[Unlock Next Universe] → Next Phase
    │ [Complete main quest line]
    │ [Reach goal: 1000/5000/10000/10000 satellites]
    │
    ▼
[Repeat Loop with New Universe]
```

### Key Loop Principles

1. **No time pressure**: Missions unlimited, no hard timers
2. **Low-stress maintenance**: Degradation causes slowdown, not death
3. **Progression unlocked**: Research unlocks content, premium only buys cosmetics/time skips
4. **Flexible expansion**: Switch universes freely, progress carries over
5. **Cross-platform rewards**: Bux and achievements sync (Google Play/Steam/Apple)

### Recommended Play Style

| Phase | New Players | Returning Players |
|-------|-------------|-------------------|
| Production | Build 1-2 satellites per queue slot | Fill all queue slots, use Bux skips |
| Launch | Launch to nearest available planet | Fill capacity, prioritize fast planets |
| Assignment | Auto-assign by time | Manual assignment for optimization |
| Degradation | Let auto-fix (if available) | Queue patches proactively |
| Rewards | Claim daily, stay on track | Front-load claim, collect backlog |
| Progression | Follow main quest | Experiment with all universes |

---

## Universe-Specific Loop Variations

Each universe modifies the core loop with unique mechanics:

### Solar System (Earth, Moon, Mars, Jupiter, Outer Belt)

| Phase | Variation |
|-------|-----------|
| Production | Standard component building |
| Transit | Distance-based (5-60 min) |
| Power | Solar + battery (recharge), eclipse drain |
| Degradation | Manual R&D patches (5 R&D slots) |
| Rewards | Coins (siloed per planet), Science (global) |
| Special | 1,000 operational satellites = steady passive income |

### Andromeda Galaxy (Colony, Planets, Artifacts)

| Phase | Variation |
|-------|-----------|
| Production | Standard + drone components |
| Transit | Instant wormhole (1-5 min) |
| Power | Battery recharge (no sun dependency) |
| Degradation | Auto-repair via R&D (no player input) |
| Rewards | Coins (siloed per planet), Science (global) |
| Special | 5,000 operational drones = passive income |

### Sci-Fi Future World (Star Systems, Dyson Sphere)

| Phase | Variation |
|-------|-----------|
| Production | High-tech components |
| Transit | Instant quantum (1-10 min) |
| Power | Fusion (independent, superior) |
| Degradation | AI self-healing (fully automatic) |
| Rewards | Coins (siloed), Science (global), Bux (small drops) |
| Special | Quantum data processing, Dyson Sphere research |

### Fantasy World (Realms, Dragons, Wayreaders)

| Phase | Variation |
|-------|-----------|
| Production | Dragon/ritual crafting |
| Transit | Instant portal (instant) |
| Power | Dragon energy cycle (sleep/wake) |
| Degradation | None - dragons sleep when low energy |
| Rewards | Coins (siloed per realm), Bux (small drops) |
| Special | **Stables** = paid per-realm slots | **Riders** = global Wayreader research |
| Unlocked | Only Wayglass/Wayreader track after Skyward Chart |

---

## UI Screens in the Loop

### Main Hub

```
┌─────────────────────────────────────────────────────────────┐
│              SATELLITE TYCOON - Main Hub                  │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  [Universal Currency]                                      │
│     🎖️ Bux: [1,250 / Free: 250]                             │
│     📊 Science: [15,500] / [Next Tech: 20,000]           │
│                                                              │
│  [Active Universes]                                        │
│     🌍 Solar System: [6 satellites]  [Goal: 1,000]       │
│     🌌 Andromeda: [120 drones]       [Goal: 5,000]        │
│     🚀 Sci-Fi: [45 satellites]      [Goal: 10,000]       │
│     🐉 Fantasy: [240 runes]         [Goal: 10,000]        │
│                                                              │
│  [Universal Timer] [14:32:00 / 24h cycle]                │
│  [Daily Rewards] [✓ Claimed] [Next: 08:00 AM]           │
│                                                              │
│  [Navigation]                                              │
│     [🌍 Solar System] [🌌 Andromeda]                    │
│     [🚀 Sci-Fi] [🐉 Fantasy]                             │
│     [🔬 Laboratory (R&D)] [🏭 Production]               │
│     [📡 Mission Board - All Universes]                 │
│                                                              │
│  [News & Events] [📢]                               │
│     - Limited time emblem available!                    │
│     - Weekend double coins event                        │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

### Planet View

```
┌─────────────────────────────────────────────────────────────┐
│                   PLANET: [Earth]                        │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  [Planet Art]                                              │
│     [Glowing Earth icon]                                  │
│                                                              │
│  Difficulty: [Easy] | Capacity: [200 / 200 slots]       │
│  Transit Time: [5-15 min] | Power: [Solar primary]      │
│                                                              │
│  [Mission Board] [Unlock Capacity: $500]               │
│  [View Orbit: Zoom In] [Manage Satellites]            │
│                                                              │
│  [Satellites Currently Here: 24]                         │
│  [Available Slots: 0 / 200]                             │
│  [Waiting for Transits: 8]                             │
│                                                              │
│  [Quick Stats]                                            │
│     Satellites Deployed: [182 / 1,000 goal]            │
│     Coins Collected: [450,000]                          │
│     Active Missions: [24]                              │
│     Completed Missions: [545]                         │
│     Avg Health: [82%]                                   │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

### Mission Board

```
┌─────────────────────────────────────────────────────────────┐
│              MISSION BOARD - [Earth]                    │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  [Filter Options]                                         │
│     [✓ Show All] [ ] Show New [ ] Show Degraded       │
│     [Sort: EST. TIME] ← Auto-sorted                     │
│     [ ] Sort: Reward Value [ ] Sort: Quest Progress   │
│     [Instrument Filter: ☀️☀️☀️☀️☀️]             │
│                                                              │
│  [Orbit Capacity]                                         │
│     Slots Used: [24 / 200] | Available: [176]          │
│     Capacity Upgrade: [250 / 500] [$500]               │
│                                                              │
│  [Available Missions - Sorted by EST. Time]              │
│     ┌─────────────────────────────────────────────────────┐│
│     │ [A] Surface Mapping                              ││
│     │     Time: 5 min | Reward: [200 Coins, 10 Science] ││
│     │     Requires: ☀️ Camera                         ││
│     │     Installs: [X / Y satellites]               ││
│     │     [ ] Assign to Satellite 1                   ││
│     │                                                  ││
│     │ ────────────────────────────────────────────────││
│     │                                                  ││
│     │ [B] Atmosphere Analysis                          ││
│     │     Time: 8 min | Reward: [350 Coins, 20 Science] ││
│     │     Requires: ☀️ Spectrometer                   ││
│     │     Installs: [X / Y satellites]               ││
│     │     [ ] Assign to Satellite 2                   ││
│     │                                                  ││
│     └─────────────────────────────────────────────────────┘│
│     ... [Scroll for more missions]                      ││
│                                                              │
│  [Queue Management]                                       │
│     [Clear Queue] [Prioritize Next 3]                   │
│     [Auto-Assign All] ← Recommended for new arrivals    │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

### Satellite Status Screen

```
┌─────────────────────────────────────────────────────────────┐
│          SATELLITE STATUS - [Your Earth Sentinel]         │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  [Satellite Icon] [Health: 89%] [Power: 55%]           │
│  [View Orbit - Zoom] [View Mission History]             │
│                                                              │
│  Current Status: [Needs Patch] (Health < 25% = ⚠️)     │
│                                                              │
│  [Next Mission Suggestions]                               │
│     1. [Surface Mapping] - 5 min est. time             │
│     2. [Atmosphere Analysis] - 8 min est. time         │
│     3. [Resource Mining] - 15 min est. time           │
│                                                              │
│  [Actions]                                                │
│     [Assign Mission] [Add to Queue] [Retire]           │
│     [Patch Health]: [5 science points]                │
│     [Recharge Power]: [500 coins]                    │
│     [Send to Launch Queue]: [300 coins]              │
│                                                              │
│  [Mission History]                                      │
│     1. [Surface Mapping] - Completed (100%)          │
│     2. [Atmosphere Analysis] - Completed (100%)      │
│     3. [Resource Mining] - In Progress (60%)        │
│     4. [Coverage Mission] - Degraded (40%)          │
│     5. [...Previous missions...]                       │
│     Total Missions: [8 / Unlimited]                   │
│     Total Health Loss: [11%]                       │
│     Total Reward: [2,500 Coins, 80 Science]          │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

### Production Facility

```
┌─────────────────────────────────────────────────────────────┐
│               PRODUCTION FACILITY                        │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  [Component Inventory]                                    │
│     ☀️ Solar Panels: [15] | 🔋 Batteries: [20]       │
│     🔬 Cameras: [8] | 📡 Spectrometers: [5]        │
│     🎤 Magnetometers: [3]                              │
│     ☢️ RTG: [2] | ☄️ Fusion Cores: [0]             │
│     🐉 Dragon Eggs: [0] | ☂️ Wayreader Runes: [5]    │
│                                                              │
│  [Builder Interface]                                      │
│     Template: [Basic Earth Sentinel ▼]                │
│     Bus: [Custom] [Select from unlocked]            │
│     Power: [Solar] [RTG] [Fusion] [Dragon Energy]    │
│     Instruments: [Select: ☀️☀️]              │
│     Thrusters: [Standard] [Upgraded ▼]              │
│     Level: [Basic] [Advanced ▼]                    │
│     Preview: [Rendered satellite icon]             │
│     Build Time: [3 min] [Skip: 10 Bux]           │
│     Cost: [500 coins]                               │
│     [Add to Queue]                                  │
│                                                              │
│  [Launch Pad Queue]                                       │
│     Slot 1: [Advanced Earth Sentinel] → [Ready]      │
│     Slot 2: [Explorer Drone] → [Ready]              │
│     Slot 3: [Empty]                                  │
│     Slot 4: [Empty]                                  │
│     Slot 5: [Empty]                                  │
│     [Add Selected to Launch Queue]                  │
│                                                              │
│  [Statistics]                                            │
│     Satellites Built: [182] | Satellites Launched: [170] │
│     Launch Cost: [0] | Current Queue: [5]            │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

### Laboratory (R&D)

```
┌─────────────────────────────────────────────────────────────┐
│                   LABORATORY (Research & Development)    │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  [Research Tree]                                          │
│     [Unlocked Researches] [Research Queue]              │
│     [Progress Bar: [████████░░░░░]]                  │
│     [Speed Up: 1 science point per level]            │
│     [Research Slots: 3 / 5]                             │
│                                                              │
│  Active Research Tree:                                   │
│     [Production Speed] ← 🔨 Level 5                    │
│     [Instruments] ← 🔬 Camera (40), Spectrometer (5)     │
│     [Orbital Capacity] ← 🚀 Level 3                     │
│     [Power Systems] ← ☀️ Solar Efficiency Lvl 3        │
│     [Degradation Fix] ← ⚡ Auto-repair Lvl 2           │
│     [Companion Perks] ← 🎯 Explorer's Insight Lvl 1    │
│     [Fantasy Only: Dragon Energy] ← 🐉 Lvl 2            │
│                                                              │
│  [Satellite Patch Queue (Earth Only)]                   │
│     [Patch Slot 1] [Patch Slot 2] [Patch Slot 3]      │
│     [Patch Slot 4] [Patch Slot 5]                      │
│     [Pending: 2] [Completed: 8]                       │
│     [Clear Queue] [Add Degraded Satellites]          │
│     [Skip: 3 Bux per patch]                          │
│                                                              │
│  [Companion R&D Support]                                │
│     [Dr. Chen]: "Fusion research at 70%!"             │
│     [Prof. Okonkwo]: "AI healing v2 stable!"        │
│     [Luna]: "Dragon rituals need 5 more eggs!"      │
│                                                              │
│  [Unlock Next Universe]                               │
│     Progress: [985 / 1,000 satellites]              │
│     [✓ Goal Complete! Unlock Andromeda]             │
│     [✓ Unlock Next Research Tier]                │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

---

## References

- Pocket Trains gameplay loop
- Real satellite operations (NASA, SpaceX)
- Star Citizen/Elite Dangerous (for contrast)
- Planet Coaster/Planet Zoo (for tycoon mechanics)
- Story progression from [[Story]]
- Quest structures from [[Story Quests]]
- [[Missions]] - Mission types, durations, rewards per universe
- [[Technology Tree]] - Research and unlocks per universe
- [[Currency]] - Currency systems (Coins siloed, Bux shared)
- [[Satellite Durability]] - Health degradation and repair
- [[Power Systems]] - Power sources per universe
- [[Orbital Capacity]] - Per-planet slot limits, stables as paid slots
- [[Companions]] - Companion archetypes and universe-specific versions
- [[Achievements]] - Cross-platform achievement tracking

---

## See Also

- [[Production Facility]] - Component building and launch queue
- [[Launch System]] - Launch mechanics, transport types, costs
- [[Orbital Capacity]] - Per-planet capacity, stables vs. slots
- [[Missions]] - Mission board, types, requirements, rewards
- [[Technology Tree]] - Research system, tech unlocks
- [[Satellite Durability]] - Health system, degradation, retirement
- [[Currency]] - Coins (siloed), Bux (shared), Science (global)
- [[Story]] - Main narrative, quest lines per universe
- [[Companions]] - Companion system, perks, universe variations
- [[Laboratory]] - R&D, patch queue, research progression
- [[Achievements]] - Cross-platform synced achievements

---

## Future Enhancements (TODO)

- [ ] "Weekend event" missions with extended timers and bonus rewards
- [ ] "Flash sale" events for cosmetics (time-sensitive Bux offers)
- [ ] Leaderboards for friendly competition (same-world only)
- [ ] Cooperative elements (invite friends to boost each other's progress)
- [ ] Seasonal events (holiday themed missions, rewards)
- [ ] Prestige/reset system (reset universe for bonus Bux)
- [ ] Dynamic events (rare cosmic incidents affecting specific planets)
- [ ] More universe-specific loop variations
- [ ] Achievements with cross-platform sync (Google Play/Steam/Apple)
- [ ] Unlockable alternate skins for existing satellites (Bux purchases)

---

## Design Notes

### Decisions Documented

1. **No permanent destruction**: Degradation slows performance, doesn't kill satellites permanently
2. **Missions unlimited**: No timer or pool limit, only capacity constraints
3. **Currency separation**: Coins siloed per universe, Bux shared across all
4. **Progression unlocked**: Research unlocks content, premium only buys cosmetics/time skips
5. **Cross-platform achievements**: Synced across Google Play/Steam/Apple
6. **Fantasy capacity split**: Stables (paid, per-realm) + Riders (research, global)
7. **Universal timer**: 24h rolling for reward claims, no hard time pressure
8. **Auto-sort by time**: Mission board auto-sorts by estimated completion time

### Philosophy

The game is designed for **low-stress, low-pressure progression**:

- Satellites are permanent fixtures once they arrive
- Degradation causes slowdown, not permanent loss
- Players can switch universes freely
- No urgent timers or penalties for being offline
- Premium is for cosmetics and time, not content

This creates a **relaxed tycoon experience** where players can progress at their own pace, with meaningful but never punishing choices.