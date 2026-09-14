# Laboratory

This page describes the research and development laboratory where players can research new technologies, improve existing systems, and repair degraded satellites.

> [[Technology Tree]] | [[Currency]] | [[Satellite Durability]] | [[Gameplay Loop]] | [[Companions]]

---

## Core Principle

The Laboratory is the research and development (R&D) department where you can:
- **Research new technologies** from the technology tree
- **Patch degraded satellites** (restore health/performance)
- **Hire scientists and researchers** to speed up research
- **Manage R&D resources** (scientists, lab assistants, research materials)

The laboratory's capabilities and mechanics vary dramatically between universes, reflecting the different technological and magical systems of each universe.

---
#TBD - everything here is hallucinated - to check if it's viable
## 🌍 Earth / Solar System Laboratory

### Laboratory Appearance

```
┌─────────────────────────────────────────────────────────────┐
│              PLANETARY TECHNOLOGY RESEARCH CENTER            │
│               "Advancing Humanity Among the Stars"          │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  [RESEARCH SECTION]                                         │
│                                                             │
│  ┌───────────────────────────────────────────────────┐     │
│  │     TECHNOLOGY TREE INTERFACE                    │     │
│  │                                                   │     │
│  │          Production Improvements                 │     │
│  │         /                                      \     │
│  │        Standard Bus                →           \     │
│  │        /            \                 →         Advanced Bus → |
│  │       /              Heat Shielding             /              |
│  │      /              |                         |              |
│  │     Modular Bus     |                         |         Heat Resistant Bus → Modular Bus
│  │                      |                         |                ↓
│  │                      |                        Advanced Heat →     Advanced Bus
│  │                      |                               ↓            ↓
│  │                      |                              Cryo Storage → Cryo Storage
│  │                      ↓                                      ↓
│  │                     Heat Shielding                         Heat Shielding
│  │                                                               ↓
│  │                        Advanced Heat                   →       Advanced Bus
│  │                                                              ↓
│  │                        Quantum Computing        →            Quantum Chassis
│  │                                                               ↓
│  │                        Deep Space Net        →          Deep Space Network
│  │                                                             ↓
│  │                        Dyson Initiative              →           Andromeda Gate
│  └───────────────────────────────────────────────────┘     │
│                                                             │
│  [RESEARCH QUEUE]                                           │
│     ┌────────────┐  ┌────────────┐  ┌────────────┐         │
│     │ 100 Coins  │  │ 500 Coins  │  │ 1,000 Coins│ [Add]|  │
│     │ [Research] │  │ [Research] │  │ [Research] │    5   │         │
│     └────────────┘  └────────────┘  └────────────┘         │
│     ┌────────────┐  ┌────────────┐                         │
│     │ 1,200 Coins│  │ 1,500 Coins│ [Add]                  │
│     │ [Research] │  │ [Research] │                         │         │
│     └────────────┘  └────────────┘                         │
│     ┌────────────┐  ┌────────────┐                         │
│     │ 1,500 Coins│  │ 5,000 Coins│ [Add]                  │
│     │ [Research] │  │ [Research] │                         │         │
│     └────────────┘  └────────────┘                         │
│     ┌────────────┐  ┌────────────┐                         │
│     │ 2,000 Coins│  │ 8,000 Coins│ [Add]                  │
│     │ [Research] │  │ [Research] │                         │         │
│     └────────────┘  └────────────┘                         │
│                                                             │
│     [Clear Queue] [Priority: 5 slots]                     │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│  [PATCH SECTION]                                            │
│                                                             │
│  [DEGRADED SATELLITES]                                       │
│     Satellite Alpha:  65% health    [PATCH] 50 Coins         │
│     Satellite Beta:   45% health    [PATCH] 80 Coins         │
│     Satellite Gamma:  20% health    [PATCH] 150 Coins        │
│     Satellite Delta:  10% health    [PATCH] 200 Coins        │
│                                                             │
│  [PENDING PATCHES]                                          │
│     Satellite Epsilon:  [Processing...] 45%                    │
│     Satellite Zeta:     [Processing...] 23%                    │
│                                                             │
│  [STAFF SECTION]                                             │
│     ┌─────────────────────────────────────┐                 │
│     │ [HIRE SCIENTIST]                   │                 │
│     │ Level | Cost | Specialization |        │                 │
│     │ 1 | 500 coins | General Tech  | [Hire]│                 │
│     │ 5 | 2,500 coins | Production   | [Hire]│                 │
│     │ 10| 5,000 coins | Research     | [Hire]│                 │
│     │ 20| 15,000 coins| Laboratory   | [Hire]│                 │
│     └─────────────────────────────────────┘                 │
│                                                             │
│  [R&D MATERIALS]                                            │
│     Scientific Data:   45 units / 100 required           │
│     Research Samples:  23 units / 50 required            │
│     Rare Elements:     8 units  / 20 required            │
│     Energy Cores:     12 units  / 25 required            │
│                                                             │
│  [FACILITY UPGRADES]                                         │
│     Lab Assistants: 3/10                                    │
│     Equipment:      Basic / Standard / Advanced           │
│     Computing:      Mainframe (Unlocked)                  │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Research Categories

#### Production Improvements

Research that reduces satellite production time and improves component quality:

| Technology | Cost | Duration | Description | Effect | Unlock Condition |
|------------|------|----------|-------------|--------|------------------|
| Standard Bus | 100 coins | 2 min | Basic satellite platform | Base technology | Start game |
| Advanced Bus | 500 coins | 5 min | Reinforced hull, better power | -20% production time | Complete Earth Network (100 satellites in Earth orbit) |
| Modular Bus | 1,000 coins | 8 min | Customizable satellite configurations | -40% production time | Reach Moon |
| Heat Shielding | 800 coins | 6 min | Protection from radiation and heat | +10% heat resistance | Reach Mars |
| Advanced Heat Shielding | 1,500 coins | 10 min | Multi-layer radiation protection | +25% heat resistance | Reach Mars (after Heat Shielding) |
| Cryo Storage | 1,200 coins | 8 min | Preserve instruments in extreme cold | -30% cold degradation | Reach Jupiter |
| Quantum Chassis | 5,000 coins | 15 min | Stabilizes quantum instruments | -50% quantum decoherence | Unlock Quantum Instruments |
| Standard Launch | 200 coins | 3 min | Basic rocket launches | Base launch time | Start game |
| Faster Engines | 800 coins | 5 min | Shorter launch wait time | -30% launch time | Reach Moon |
| Cryogenic Fuel | 1,500 coins | 8 min | Extended range propellant | +40% range, +20% capacity | Reach Mars |
| Multi-Stage Separation | 1,200 coins | 10 min | More efficient staging | -35% launch time | Reach Mars |
| Gravity Assist Planning | 2,000 coins | 15 min | Optimal trajectory using planetary gravity | -50% launch time | Reach Jupiter |
| Hybrid Power | 2,000 coins | 12 min | Solar + RTG combination | +30% power efficiency | Reach Jupiter |
| Advanced Power | 3,000 coins | 15 min | Optimized power systems | +50% power efficiency | Reach Jupiter (after Hybrid Power) |

---

#### Power Upgrades

Research that improves satellite power systems:

| Technology | Cost | Duration | Description | Effect | Unlock Condition |
|------------|------|----------|-------------|--------|------------------|
| Battery Technology | 300 coins | 3 min | Extend recharge time, increase capacity | +15% battery capacity | Start game |
| Solar Efficiency | 600 coins | 5 min | Better solar panels, faster recharge | +25% solar output | Reach Moon |
| RTG Systems | 1,500 coins | 10 min | Radioisotope thermoelectric generators | Works on Mars (solar unreliable) | Reach Mars (requires Solar Efficiency) |
| RTG Efficiency | 1,000 coins | 8 min | Better fuel efficiency, less degradation | +20% RTG output, -15% degradation | Reach Mars (after RTG Systems) |
| Fission Reactor | 5,000 coins | 15 min | Compact nuclear fission power | Works anywhere in solar system | Reach Jupiter (requires RTG Efficiency) |
| Fusion Core | 15,000 coins | 30 min | Fusion power for deep space | Works anywhere, minimal degradation | Reach Jupiter (after Fission) |
| Hybrid Power | 2,000 coins | 12 min | Solar + RTG/Solar + Fission | Balanced power systems | Reach Jupiter |
| Adaptive Power | 3,000 coins | 18 min | Auto-switch power sources | Optimized for conditions | Reach Jupiter (after Hybrid) |
| Battery Technology | 300 coins | 3 min | Extend recharge time, increase capacity | +15% battery capacity | Start game |
| Solar Efficiency | 600 coins | 5 min | Better solar panels, faster recharge | +25% solar output | Reach Moon |

---

#### Propulsion Improvements

Research that improves launch and transit capabilities:

| Technology | Cost | Duration | Description | Effect | Unlock Condition |
|------------|------|----------|-------------|--------|------------------|
| Standard Launch | 200 coins | 3 min | Basic rocket launches | Base launch time | Start game |
| Faster Engines | 800 coins | 5 min | Shorter launch wait time | -30% launch time | Reach Moon |
| Cryogenic Fuel | 1,500 coins | 8 min | Extended range propellant | +40% range, +20% capacity | Reach Mars |
| Multi-Stage Separation | 1,200 coins | 10 min | More efficient staging | -35% launch time | Reach Mars |
| Gravity Assist Planning | 2,000 coins | 15 min | Optimal trajectory using planetary gravity | -50% launch time | Reach Jupiter |
| Ion Drive | 3,000 coins | 12 min | Ion thruster propulsion | -40% time, +30% cost | Reach Jupiter |
| Fusion Propulsion | 8,000 coins | 25 min | Fusion-powered spacecraft | -60% time, works anywhere | Reach Outer Space |
| Quantum Propulsion | 25,000 coins | 40 min | Quantum entanglement transit | Instant | Reach Andromeda |

---

#### Mission Instruments

Research that unlocks new satellite instruments:

| Technology | Cost | Duration | Description | Unlock | Effect |
|------------|------|----------|-------------|--------|--------|
| Optical Camera | 500 coins | 3 min | High-resolution imaging | Start | Enables Surface Mapping |
| Advanced Optics | 1,200 coins | 6 min | Better cameras, clearer images | Reach Moon | +20% imaging quality |
| Spectrometer | 800 coins | 5 min | Analyzes atmospheric composition | Reach Moon | Enables Atmosphere Monitoring |
| Magnetometer | 600 coins | 4 min | Measures magnetic fields | Start | Enables Magnetic Field Studies |
| Radiation Detector | 900 coins | 6 min | Monitors radiation levels | Reach Mars | Enables Radiation Monitoring |
| Geiger Counter | 400 coins | 3 min | Detects radiation exposure | Reach Mars | Enables Radiation Monitoring |
| Life Biosensor | 2,000 coins | 10 min | Detects biosignatures | Reach Mars | Enables Life Detection |
| Resource Scanner | 1,500 coins | 8 min | Identifies valuable resources | Reach Mars | Enables Resource Collection |
| Climate Monitor | 3,000 coins | 12 min | Tracks climate patterns | Reach Mars | Enables Climate Monitoring |
| Quantum Instruments | 10,000 coins | 20 min | Quantum sensor suite | Reach Jupiter | Enables Quantum Research |
| Deep Space Network | 15,000 coins | 25 min | Deep space communications | Reach Outer Space | Enables Outer Space missions |

---

### Patch Queue

When satellites degrade, they need to be patched to restore their performance.

#### Earth Patch System

- **Manual patching required**: You must actively send degraded satellites to the patch queue
- **Patch costs**: Based on health percentage
- **Patch duration**: Depends on degradation level and scientist level

```
┌─────────────────────────────────────────────────────────────┐
│                   PATCH QUEUE                                │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  [DEGRADED SATELLITES]                                       │
│                                                             │
│  Satellite Alpha:                                            │
│     Current Health: 65%                                     │
│     Required: 100%                                          │
│     Health to Restore: 35 points                            │
│     Estimated Cost: 50 coins                                │
│     Estimated Time: 15 min (with 1 scientist)               │
│                                                             │
│     [Add to Patch Queue]                                    │
│                                                             │
│  Satellite Beta:                                             │
│     Current Health: 45%                                     │
│     Required: 100%                                          │
│     Health to Restore: 55 points                            │
│     Estimated Cost: 80 coins                                │
│     Estimated Time: 25 min (with 1 scientist)               │
│                                                             │
│     [Add to Patch Queue]                                    │
│                                                             │
│  Satellite Gamma:                                            │
│     Current Health: 20%                                     │
│     Required: 100%                                          │
│     Health to Restore: 80 points                            │
│     Estimated Cost: 150 coins                               │
│     Estimated Time: 45 min (with 1 scientist)               │
│                                                             │
│     [Add to Patch Queue]                                    │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│  [PATCHING STATUS]                                           │
│                                                             │
│  Queue Slot 1: [Processing...] 30% - Satellite Alpha      │
│  Queue Slot 2: [Processing...] 15% - Satellite Beta        │
│                                                             │
│  [Add more degraded satellites...]                          │
│  [Clear Completed Patches]                                  │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

#### Patch Pricing Formula

```
Patch Cost = (100 - CurrentHealth) × BaseCostModifier

Base Cost Modifier = (ScientistLevel / 10)
```

Example:
- Health: 65% → 35 points to restore
- Scientist Level 5 → Modifier = 0.5
- Cost = 35 × 0.5 = 17.5 coins (rounded to 20)

Example:
- Health: 20% → 80 points to restore
- Scientist Level 5 → Modifier = 0.5
- Cost = 80 × 0.5 = 40 coins

Example:
- Health: 20% → 80 points to restore
- Scientist Level 0 → Modifier = 1.0
- Cost = 80 × 1.0 = 80 coins

#### Patch Duration Formula

```
Base Patch Duration (100% health) = 60 minutes
Duration Multiplier = (100 - CurrentHealth) / 100
Scientist Speed Multiplier = (ScientistLevel + 1) / 10

Final Duration = 60 × Duration Multiplier × Scientist Speed Multiplier
```

Example:
- Satellite at 65% health (35 points to restore)
- Scientist Level 5
- Duration = 60 × 0.35 × 1.5 = 31.5 minutes

---

### R&D Scientists

Hire scientists to speed up research and patch operations:

| Scientist | Level Cost | Cost | Specialization | Research Speed | Patch Speed |
|-----------|------------|------|----------------|----------------|-------------|
| Apprentice | 500 coins | 1 min | General | +10% | +10% |
| Junior | 1,000 coins | 5 min | Research | +25% | +20% |
| Associate | 2,500 coins | 10 min | Lab Operations | +40% | +30% |
| Senior | 5,000 coins | 20 min | Technology | +60% | +40% |
| Principal | 10,000 coins | 40 min | Advanced Research | +80% | +50% |
| Lead Researcher | 25,000 coins | 1 hour | Deep Space | +100% | +60% |
| Director | 50,000 coins | 1.5 hours | Strategic Research | +150% | +80% |

Scientists can be:
- Hired at the Laboratory
- Unlocked through research
- Recruited from story events
- Gained through quest completion

---

### Research Mechanics

#### How Research Works

1. **Select technology** from the technology tree
2. **Check requirements**: Cost, prerequisites, scientist availability
3. **Pay the cost** in coins
4. **Research starts** immediately (or goes to queue)
5. **Wait for completion** (or use time skip with Bux)
6. **Receive rewards**: New instruments, unlocked content, etc.

#### Research Queue

The lab can only handle limited research simultaneously:

```
┌─────────────────────────────────────────────────────────────┐
│                   RESEARCH QUEUE                             │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  Slot 1: [Researching...] 25% - Advanced Optics           │
│  Slot 2: [Researching...] 60% - Better Batteries          │
│  Slot 3: [Ready]                                            │
│  Slot 4: [Ready]                                            │
│  Slot 5: [Ready]                                            │
│                                                             │
│  [Add to Queue] (must have requirements met)              │
│  [Clear Queue]                                            │
│  [Auto-fill with priority items]                          │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

Queue limits:
- Max 5 active research projects
- Queue can hold 10 pending projects
- Only certain technologies can be researched (tech tree progression)

#### Time Skip Research

Use Bux (premium currency) to skip research time:

| Research Tier | Skip Cost | Skip Cost |
|---------------|-----------|-----------|
| Basic (1 min) | 1 Bux | - |
| Medium (5 min) | 5 Bux | - |
| Long (15+ min) | 10 Bux | - |

Note: Research cannot be skipped if you don't have enough Bux.

---

## 🌌 Andromeda Galaxy Laboratory

### Laboratory Appearance

```
┌─────────────────────────────────────────────────────────────┐
│             ANDROMEDA SCIENTIFIC RESEARCH FACILITY          │
│       "Exploring the Unknown Corners of the Galaxy"        │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  [AUTOMATED RESEARCH]                                       │
│                                                             │
│  [ACTIVE RESEARCH PROGRAMS]                                  │
│     ✓ Colonial Habitat Optimization              45%         │
│     ✓ Atmospheric Composition Analysis          78%         │
│     ✓ Exoplanet Classification                   32%         │
│     ✓ Ancient Artifact Study                    12%         │
│     ✓ Quantum Resonance Theory                   5%          │
│                                                             │
│  [RESEARCH ACCOMPLISHMENTS]                                  │
│     Colonial Habitat Design: Unlocked                     │
│     Atmospheric Scanner: Unlocked                        │
│     Quantum Field Theory: Research in progress           │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│  [PATCH SECTION - AUTOMATIC]                                  │
│                                                             │
│  "Degraded satellites are automatically repaired."         │
│     Satellite Alpha: Repairing... 45%                     │
│     Satellite Beta:  Repairing... 80%                     │
│     Satellite Gamma: Repairing... 92%                     │
│                                                             │
│  "Your advanced Xeno-Ops technicians ensure rapid repair."│
│                                                             │
├─────────────────────────────────────────────────────────────┤
│  [STAFF SECTION - XENO-OPS TECHNICIANS]                      │
│                                                             │
│     [HIRE TECHNICIAN]                                       │
│     Level | Cost | Specialization | Effect          │
│     1 | 1,000 coins | General Repair | Base repair    │
│     5 | 5,000 coins | Advanced Xeno | +25% repair   │
│     10| 15,000 coins| Quantum Tech  | +50% repair    │
│     20| 50,000 coins| Fusion Expert | +100% repair  │
│                                                             │
│  [FACILITY UPGRADES]                                        │
│     Repair Bays: 5/20                                        │
│     Equipment: Standard / Advanced / Quantum               │
│     Automation: Manual / Partial / Full                   │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Unique Features

- **Automated repair**: Degraded satellites are automatically repaired (no manual patching)
- **Specialized Xeno-Ops technicians**: Instead of scientists, you hire alien-trained technicians
- **Research acceleration**: Automated systems speed up repair significantly
- **Discovery research**: Research focused on alien technology and knowledge

### Research Categories

#### Exploration Technology

Research focused on alien planet exploration:

| Technology | Cost | Duration | Description | Effect | Unlock Condition |
|------------|------|----------|-------------|--------|------------------|
| Basic Scanner | 2,000 coins | 5 min | Simple planet scanning | Basic exploration | Reach Colony |
| Advanced Scanner | 5,000 coins | 10 min | Detailed planet analysis | -20% scan time | Reach 3 planets |
| Quantum Scanner | 15,000 coins | 15 min | Deep dimensional scanning | -50% scan time | Reach Planet 5 |
| Life Detection System | 8,000 coins | 12 min | Advanced biosignature detection | Enable life detection | Reach 3 habitable planets |
| Artifact Resonator | 20,000 coins | 20 min | Ancient artifact activation | Enable artifact missions | Reach Planet 5 |

---

#### Alien Technology Research

Research into alien technology and knowledge:

| Technology | Cost | Duration | Description | Effect | Unlock Condition |
|------------|------|----------|-------------|--------|------------------|
| Ancient Script Analysis | 5,000 coins | 15 min | Decipher alien writing | Unlock artifact data | Reactivate 3 artifacts |
| Quantum Linguistics | 15,000 coins | 25 min | Translate alien language | Universal translation | Decipher 5 artifacts |
| Xenotech Integration | 30,000 coins | 40 min | Adapt alien tech | Unlock alien components | Unlock 10 artifacts |
| Dark Energy Theory | 50,000 coins | 60 min | Study dark matter/energy | Unlock dark matter tools | Complete artifact path |
| Quantum Wormhole Theory | 100,000 coins | 90 min | Theory of intergalactic travel | Unlock Sci-Fi access | Reactivate final artifact |

---

#### Specialized Equipment

Research for unique alien tools:

| Technology | Cost | Duration | Description | Effect |
|------------|------|----------|-------------|--------|
| Artifact Analyzer | 10,000 coins | 20 min | Study ancient alien tech | Unlock artifact missions |
| Xenobio Scanner | 15,000 coins | 25 min | Analyze alien biology | Enable life detection |
| Plasma Containment | 25,000 coins | 35 min | Handle alien plasma tech | Enable plasma research |
| Dimensional Stabilizer | 40,000 coins | 50 min | Study alternate dimensions | Enable Sci-Fi access |

---

### Repair Mechanics

#### Automatic Repair

Unlike Earth, Andromeda has **automated repair**:

```
┌─────────────────────────────────────────────────────────────┐
│                   REPAIR STATUS                              │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  Satellite Alpha: [Repairing...] 67%                       │
│     Health: 33% → 100%                                     │
│     Time Remaining: 12 min                                 │
│                                                             │
│  Satellite Beta: [Repairing...] 23%                        │
│     Health: 77% → 100%                                     │
│     Time Remaining: 25 min                                 │
│                                                             │
│  Satellite Gamma: [Health: 100%]                           │
│     Ready for missions                                     │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│  [REPAIR FACILITY STATUS]                                    │
│     Technicians: 5 / 20                                    │
│     Bays: 8 / 20                                          │
│     Automation Level: Advanced                            │
│                                                             │
│  "Xeno-Ops technicians are repairing satellites."         │
│  "All repairs are free. No coins spent."                  │
│     (Research has unlocked better technicians)           │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

#### Technician Levels

Xeno-Ops technicians speed up repairs:

| Technician Level | Research Cost | Repair Speed | Special Ability |
|-----------------|---------------|--------------|-----------------|
| Tech Level 1 | 1,000 coins | 1x (base) | Basic repairs |
| Tech Level 5 | 5,000 coins | 1.5x | Faster repairs |
| Tech Level 10 | 15,000 coins | 2x | Rapid repairs |
| Tech Level 20 | 50,000 coins | 3x | Emergency repairs |
| Tech Level 50 | 100,000 coins | 5x | Perfect repairs |

#### Automation Levels

As you progress, repair becomes more automated:

| Automation | Research Cost | Effect |
|------------|---------------|--------|
| Manual | - | You manually queue repairs |
| Partial | 5,000 coins | 50% auto-repair |
| Advanced | 15,000 coins | 75% auto-repair |
| Full | 30,000 coins | 100% auto-repair |

---

## 🚀 Sci-Fi Future World Laboratory

### Laboratory Appearance

```
┌─────────────────────────────────────────────────────────────┐
│               QUANTUM RESEARCH INSTITUTE                     │
│           "Exploring the Fabric of Reality"                │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  [QUANTUM RESEARCH SECTION]                                  │
│                                                             │
│  ┌───────────────────────────────────────────────────┐     │
│  │     QUANTUM TECHNOLOGY TREE                      │     │
│  │                                                   │     │
│  │          Propulsion Research                   │     │
│  │         /                                      \     │
│  │        Chemical          →                   \     │
│  │        /            \              →           Ion Drive → |
│  │       /             Fusion              /            |
│  │      /              |                 /             |
│  │     Quantum         |                Fusion         |
│  │      \             /                 \            /
│  │       \           Antimatter          \          /
│  │        \          /                    \        /
│  │         \        Quantum Computer        \      /
│  │          \      /                      Quantum Portal /
│  │           Dyson Sphere                          Next Universe
│  └───────────────────────────────────────────────────┘     │
│                                                             │
│  [RESEARCH QUEUE]                                           │
│     ┌────────────┐  ┌────────────┐  ┌────────────┐         │
│     │ 5,000 Coins│  │ 15,000 Coins│  │ 30,000 Coins│ [Add]│  │
│     │ [Research] │  │ [Research] │  │ [Research] │    7   │         │
│     └────────────┘  └────────────┘  └────────────┘         │
│     ┌────────────┐  ┌────────────┐                         │
│     │ 10,000 Coins│  │ 50,000 Coins│ [Add]                 │
│     │ [Research] │  │ [Research] │                         │         │
│     └────────────┘  └────────────┘                         │
│     ┌────────────┐  ┌────────────┐                         │
│     │ 25,000 Coins│  │ 100,000 Coins│ [Add]                │
│     │ [Research] │  │ [Research] │                         │         │
│     └────────────┘  └────────────┘                         │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│  [PATCH SECTION - AI SELF-REPAIR]                             │
│                                                             │
│  "Satellites repair themselves using AI."                    │
│     Satellite Alpha: Self-healing... 78%                    │
│     Satellite Beta:  Self-healing... 45%                    │
│     Satellite Gamma:  Self-healing... 92%                   │
│     Satellite Delta:  Self-healing... 33%                   │
│                                                             │
│  "Antimatter AI cores ensure perfect restoration."          │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│  [RESEARCH STAFF - QUANTUM PHYSICISTS]                        │
│                                                             │
│     [HIRE PHYSICIST]                                         │
│     Level | Cost | Specialization | Effect          │
│     1 | 2,000 coins | Quantum Basics | Base research   │
│     5 | 10,000 coins | Quantum Mech  | +30% research  │
│     10| 30,000 coins| Quantum Field | +60% research   │
│     20| 100,000 coins| Quantum Master| +100% research │
│                                                             │
│  [COMPUTING FACILITIES]                                      │
│     Mainframe: Level 5 / 10                                │
│     Quantum Core: Level 3 / 5                             │
│     AI Research Cluster: Level 2 / 10                     │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Unique Features

- **AI Self-Repair**: Satellites repair themselves automatically using AI (no manual patching)
- **Quantum Research**: All research uses quantum computing capabilities
- **Progressive AI Integration**: AI becomes more sophisticated, improving self-repair
- **Dyson Sphere Research**: Building blocks for the massive solar megastructure

### Research Categories

#### Quantum Computing Research

Research into quantum computing and quantum phenomena:

| Technology | Cost | Duration | Description | Effect | Unlock Condition |
|------------|------|----------|-------------|--------|------------------|
| Quantum Bits | 10,000 coins | 10 min | Basic quantum computing | Enable quantum research | Reach Star System 2 |
| Entanglement | 25,000 coins | 20 min | Quantum entanglement theory | Enable quantum teleporter | Reach Star System 3 |
| Quantum Processor | 50,000 coins | 30 min | Quantum computer chip | Faster quantum operations | Build initial quantum computer |
| Quantum Network | 100,000 coins | 45 min | Full quantum network | Instant quantum travel | Build full quantum computer |
| Quantum Consciousness | 200,000 coins | 60 min | Quantum mind interface | Unlock Fantasy access | Complete quantum research |

---

#### Dyson Sphere Research

Research focused on building the Dyson Sphere:

| Technology | Cost | Duration | Description | Effect |
|------------|------|----------|-------------|--------|
| Solar Panel Tech | 15,000 coins | 15 min | Advanced solar collection | Enable solar panel missions |
| Dyson Core Construction | 100,000 coins | 60 min | Build the Dyson Sphere core | Unlock Fusion technology |
| Dyson Shell Assembly | 200,000 coins | 90 min | Complete Dyson Sphere | Unlock unlimited power |
| Energy Distribution | 50,000 coins | 30 min | Power distribution network | Distribute Dyson energy |
| Fusion Reactors | 75,000 coins | 45 min | Fusion power generation | Enable fusion missions |
| Antimatter Creation | 150,000 coins | 75 min | Antimatter production | Enable antimatter missions |

---

#### Advanced Propulsion

Research into next-generation propulsion:

| Technology | Cost | Duration | Description | Effect |
|------------|------|----------|-------------|--------|
| Ion Drive | 5,000 coins | 8 min | Ion thruster propulsion | Faster transit |
| Fusion Drive | 50,000 coins | 20 min | Fusion-powered drive | Near-light speed |
| Antimatter Engine | 100,000 coins | 30 min | Antimatter propulsion | Instant intergalactic |
| Quantum Propulsion | 200,000 coins | 40 min | Quantum entanglement travel | Instant universal travel |
| Time Dilation Drive | 300,000 coins | 60 min | Manipulate time for faster travel | Time dilation effect |

---

### AI Self-Repair

Unlike Earth or Fantasy, Sci-Fi uses **AI self-repair**:

```
┌─────────────────────────────────────────────────────────────┐
│                 AI SELF-REPAIR SYSTEM                         │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  [AI REPAIR STATUS]                                         │
│                                                             │
│  Satellite Alpha: [AI Repairing...] 62%                   │
│     Health: 38% → 100%                                     │
│     Time Remaining: 18 min                                 │
│                                                             │
│  Satellite Beta: [AI Repairing...] 85%                   │
│     Health: 15% → 100%                                     │
│     Time Remaining: 8 min                                  │
│                                                             │
│  Satellite Gamma: [AI Repairing...] 100%              │
│     Health: 100% (perfect)                               │
│     Status: Ready                                         │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│  [AI RESEARCH LEVELS]                                       │
│                                                             │
│  AI Level | Repair Speed | Cost | Effect       │
│  1 | 1x (slow) | 0 coins | Basic self-repair │
│  5 | 1.5x | 5,000 coins | Faster healing     │
│  10| 2x  | 15,000 coins | Rapid healing      │
│  20| 3x  | 50,000 coins | Emergency healing  │
│  50| 5x  | 150,000 coins | Perfect healing    │
│                                                             │
│  [Upgrade AI] [View Details]                               │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

#### AI Development

AI self-repair improves as you research:

| AI Level | Research Cost | Self-Repair Quality | Notes |
|----------|---------------|--------------------|-------|
| AI Level 1 | 5,000 coins | 50% repair | Basic healing, slow |
| AI Level 5 | 20,000 coins | 70% repair | Better healing, faster |
| AI Level 10 | 50,000 coins | 85% repair | Rapid healing, efficient |
| AI Level 20 | 100,000 coins | 95% repair | Near-perfect |
| AI Level 50 | 300,000 coins | 100% repair | Perfect healing |

At AI Level 50, satellites are effectively immortal (can be retired if needed).

---

## 🐉 Magic Fantasy World Laboratory

### Laboratory Appearance

```
┌─────────────────────────────────────────────────────────────┐
│                 THE ANCIENT MAGE ACADEMY                     │
│        "Learning the Arcane Arts of the Realms"            │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  [MAGIC RESEARCH SECTION]                                    │
│                                                             │
│  ┌───────────────────────────────────────────────────┐     │
│  │          MAGICAL RESEARCH TREE                   │     │
│  │                                                   │     │
│  │          Arcane Studies                          │     │
│  │         /                                       \     │
│  │        Basic   →                          \     │     │
│  │        /        \                          Advanced → |     │
│  │       /         Fire           →             Healing │     │
│  │      /          |                      /            │     │
│  │     Air          |                    Protection     │     │
│  │      \          /                   /               │     │
│  │       \        Spellcasting        /               │     │
│  │        \      /           /          \            │     │
│  │         \    Dragon      /            Magic Theory │     │
│  │          \  /          /             /          \  │     │
│  │           \ Beacon Training /      /            \ \ │     │
│  │            \             /      /               \/ │     │
│  │             Universal Access (Next Universe)        │     │
│  └───────────────────────────────────────────────────┘     │
│                                                             │
│  [RESEARCH QUEUE]                                           │
│     ┌────────────┐  ┌────────────┐  ┌────────────┐         │
│     │ 500 Coins  │  │ 2,000 Coins│  │ 5,000 Coins│ [Add]│  │         │
│     │ [Research] │  │ [Research] │  │ [Research] │    10  │         │
│     └────────────┘  └────────────┘  └────────────┘         │         │
│     ┌────────────┐  ┌────────────┐                         │         │
│     │ 10,000 Coins│  │ 50,000 Coins│ [Add]                 │         │
│     │ [Research] │  │ [Research] │                         │         │
│     └────────────┘  └────────────┘                         │         │
│     ┌────────────┐  ┌────────────┐                         │         │
│     │ 25,000 Coins│  │ 100,000 Coins│ [Add]                │         │
│     │ [Research] │  │ [Research] │                         │         │
│     └────────────┘  └────────────┘                         │         │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│  [DRAGON BREEDING LAB]                                       │
│                                                             │
│  [INCUBATION PODS]                                           │
│     [● Pod 1] 15% complete - Dragon (Earth)                 │
│     [● Pod 2] 78% complete - Dragon (Fire)                  │
│     [● Pod 3] 92% complete - Dragon (Air)                   │
│     [● Pod 4] 45% complete - Dragon (Water)                 │
│     [● Pod 5] 23% complete - Dragon (Earth)                 │
│     [● Pod 6] 67% complete - Dragon (Shadow)                │
│     [● Pod 7] 89% complete - Dragon (Sun)                   │
│     [● Pod 8] 56% complete - Dragon (Storm)                 │
│     [● Pod 9] 100% complete - [HATCHED!] 🐉                │
│     [○ Pod 10] Empty (incubating new egg)                  │
│                                                             │
│  [TREASURE CHEST] - Sale of hatched dragons              │
│     Earth Dragon: 3,000 coins (1 available)               │
│     Fire Dragon:   3,500 coins (0 available)              │
│     Water Dragon:  3,000 coins (1 available)              │
│     Air Dragon:    4,000 coins (1 available)              │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│  [WAYREADER ACADEMY]                                         │
│                                                             │
│  [WAYREADER TRAINING]                                        │
│     [Apprentice] [10/20 to Journeyman] [15 coins]           │
│     [Journeyman] [10/20 to Artisan] [30 coins]              │
│     [Artisan]    [10/20 to Master] [60 coins]               │
│     [Master]     [10/20 to Grandmaster] [150 coins]        │
│     [Grandmaster][0/50 to Legendary] [500 coins]           │
│                                                             │
│  [COMPLETION REWARDS]                                        │
│     Apprentice: 50 coins, 5 mana                         │
│     Journeyman: 150 coins, 15 mana                      │
│     Artisan: 300 coins, 30 mana                        │
│     Master: 800 coins, 80 mana                         │
│     Grandmaster: 2,000 coins, 200 mana                  │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│  [RUNE CRAFTING WORKSHOP]                                    │
│                                                             │
│  [SELECT RUNE]                                               │
│     ☑️ Navigation   ☑️ Portal   ☑️ Anchor   ☑️ Boundary   │
│     ☑️ Compass     ☑️ Landmark  ☑️ Beacon   ☐ Special   │
│                                                             │
│  [SELECT MATERIALS]                                          │
│     [Mana Orbs] 500 / Required ████████████░░░░░░ 60%   │
│     [Crystal Shards] 100 / Required ██████░░░░░░░░ 45%  │
│     [Dust of Stars] 25 / Required ████░░░░░░░░░░ 20%     │
│                                                             │
│  [RUNE BONUS MODIFIERS]                                      │
│     ☑️ Enhanced Range (50% extra range)                 │
│     ☑️ Enhanced Stability (lasts 2x longer)          │
│     ☐ Enhanced Speed (travel 2x faster)               │
│     ☐ Rare Rune (5% chance, +100% effect)              │
│                                                             │
│  [CRAFT] [View Runes Available]                            │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Unique Features

- **No traditional research tree**: Progression through magical abilities, dragon breeding, and companion training
- **Dragon breeding**: Instead of buying satellites, you hatch and train dragons
- **Rune crafting**: Instead of buying equipment, you craft magical runes
- **Companion-dependent progression**: Some unlocks require companion interactions

### Research Categories

#### Magic Studies

Research magical abilities and theories:

| Technology | Cost | Duration | Description | Effect | Unlock Condition |
|------------|------|----------|-------------|--------|------------------|
| Basic Casting | 500 coins | 2 min | Simple spellcasting | Enable basic magic | Hire first Wayreader |
| Elemental Theory | 2,000 coins | 5 min | Study of elements | Unlock Fire, Air, Water, Earth | Train 5 dragons |
| Healing Magic | 5,000 coins | 10 min | Life-restoring spells | Unlock healing for dragons | Own breeding stable |
| Protection Magic | 8,000 coins | 15 min | Shield and barrier spells | Dragon protection | Train 10 dragons |
| Spell Theory | 15,000 coins | 20 min | Advanced magic systems | Unlock advanced spells | Train 20 dragons |
| Runecraft Basics | 10,000 coins | 25 min | Rune creation and reading | Enable rune crafting | Train 30 dragons |

---

#### Dragon Breeding

Research focused on dragon hatching and genetics:

| Technology | Cost | Duration | Description | Effect |
|------------|------|----------|-------------|--------|
| Basic Genetics | 3,000 coins | 30 min | Understand dragon traits | Enable breeding |
| Trait Inheritance | 8,000 coins | 60 min | Predict offspring traits | Better breeding outcomes |
| Elemental Balance | 15,000 coins | 90 min | Balance magical elements | More stable hatching |
| Ancient Dragon Bloodline | 50,000 coins | 150 min | Unlock legendary dragons | Access ancient dragons |
| Mutation Studies | 100,000 coins | 200 min | Create new dragon types | Unlock experimental dragons |

---

#### Wayreader Training

Research for improving human magic users:

| Technology | Cost | Duration | Description | Effect |
|------------|------|----------|-------------|--------|
| Mana Sensitivity | 1,000 coins | 10 min | Better mana perception | +10% mana efficiency |
| Pathfinding | 2,500 coins | 20 min | Faster portal navigation | -20% travel time |
| Rune Theory | 5,000 coins | 30 min | Understand rune mechanics | Better rune creation |
| Arcane Knowledge | 10,000 coins | 60 min | Deep magical studies | Unlock advanced spells |
| Universal Magic | 50,000 coins | 120 min | Magic across all realities | Unlock next universe |

---

#### Beacon Crafting

Research for creating and placing wayglass beacons:

| Technology | Cost | Duration | Description | Effect |
|------------|------|----------|-------------|--------|
| Rune Smithing | 5,000 coins | 40 min | Craft navigation runes | Enable beacon placement |
| Portal Stabilization | 15,000 coins | 80 min | Create stable portals | Beacons last longer |
| Skyward Chart Theory | 30,000 coins | 120 min | Map all 5 realms | Complete navigation system |
| Beacon Optimization | 50,000 coins | 150 min | Maximize beacon efficiency | Beacons work better |
| Universal Beacon | 100,000 coins | 200 min | Beacons between universes | Unlock all universes |

---

### Dragon Breeding Mechanics

Instead of traditional R&D, Fantasy uses **dragon breeding**:

```
┌─────────────────────────────────────────────────────────────┐
│                DRAGON BREEDING INTERFACE                    │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  [SELECT PARENT DRAGONS]                                     │
│                                                             │
│  Mother Dragon:                                              │
│     Type: [Earth Dragon ▼] [Fire Dragon ▼] [Water Dragon ▼] │
│     Elements: [Earth] [Fire] [Water] [Air] [All]          │
│     Trait: Loyalty [____] (20-100%)                        │
│     Trait: Magic [____] (20-100%)                          │
│     Trait: Combat [____] (20-100%)                         │
│     Trait: Speed [____] (20-100%)                          │
│                                                             │
│  Father Dragon:                                              │
│     Type: [Earth Dragon ▼] [Fire Dragon ▼] [Water Dragon ▼] │
│     Elements: [Fire] [Earth] [Water] [Air] [All]          │
│     Trait: Loyalty [____] (20-100%)                        │
│     Trait: Magic [____] (20-100%)                          │
│     Trait: Combat [____] (20-100%)                         │
│     Trait: Speed [____] (20-100%)                          │
│                                                             │
│  [BREED] [Cancel]                                           │
│                                                             │
│  [ESTIMATED OFFSPRING]                                       │
│     Most Likely Type: [Fire Dragon] 60%                    │
│     Secondary Type: [Earth Dragon] 40%                    │
│     Traits: Average of parents ± 10%                     │
│     Incubation Time: 60-90 min (varies by type)          │
│     Mana Cost: 500-800 (varies by type)                 │
│                                                             │
│  [CONSUME MANA] or [Buy with Coins]                        │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│  [INCUBATION]                                                │
│     Egg: [████████████░░] 75%                              │
│     Status: [🥚 Incubating]                               │
│     Time Elapsed: 45 min                                  │
│     Estimated Completion: 20 min remaining               │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Trait Inheritance

Dragons inherit traits from parents:

| Trait | Inheritance Mechanism |
|-------|---------------------|
| Elemental Type | 50/50 chance from mother/father base types |
| Loyalty | (Mother Loyalty + Father Loyalty) / 2 ± 10% |
| Magic | (Mother Magic + Father Magic) / 2 ± 10% |
| Combat | (Mother Combat + Father Combat) / 2 ± 10% |
| Speed | (Mother Speed + Father Speed) / 2 ± 10% |

#### Mutations

Random mutations can occur (5% chance per egg):

| Mutation Type | Effect | Bonus |
|---------------|--------|-------|
| Enhanced Trait | One trait goes above average | +25% trait value |
| Reduced Trait | One trait goes below average | -15% trait value |
| Rare Element | Unusual element type | +50% value for that element |
| Balanced | All traits equal | Base 70% |

---

## Laboratory Upgrades

Upgrade your laboratory to improve capabilities:

### Earth Lab Upgrades

| Upgrade | Cost | Effect |
|---------|------|--------|
| Lab Assistant 1 | 1,000 coins | +1 patch slot, +10% research speed |
| Lab Assistant 2 | 2,500 coins | +1 patch slot, +20% research speed |
| Lab Assistant 3 | 5,000 coins | +1 patch slot, +30% research speed |
| Better Equipment | 5,000 coins | +20% research speed |
| Advanced Equipment | 15,000 coins | +40% research speed |
| Research Computer | 10,000 coins | Unlock advanced research |
| Computing Server | 25,000 coins | +50% research speed |
| Quantum Computer | 50,000 coins | Unlock quantum research |

### Andromeda Lab Upgrades

| Upgrade | Cost | Effect |
|---------|------|--------|
| Repair Bay 1 | 5,000 coins | +1 repair bay, auto-repair starts |
| Repair Bay 2 | 10,000 coins | +1 repair bay, +20% repair speed |
| Repair Bay 3 | 20,000 coins | +1 repair bay, +40% repair speed |
| Tech Lab | 15,000 coins | Unlock advanced research |
| Tech Lab 2 | 40,000 coins | Unlock quantum research |
| Quantum Lab | 100,000 coins | Unlock intergalactic research |

### Sci-Fi Lab Upgrades

| Upgrade | Cost | Effect |
|---------|------|--------|
| AI Core 1 | 10,000 coins | AI Level 1 (basic self-repair) |
| AI Core 2 | 25,000 coins | AI Level 5 (faster healing) |
| AI Core 3 | 50,000 coins | AI Level 10 (rapid healing) |
| Quantum Server | 30,000 coins | Better quantum research |
| Quantum Server 2 | 75,000 coins | Better quantum research |
| Quantum Server 3 | 150,000 coins | Better quantum research |
| Dyson Research Module | 200,000 coins | Unlock Dyson research |

### Fantasy Lab Upgrades

| Upgrade | Cost | Effect |
|---------|------|--------|
| Nursery Expansion 1 | 5,000 coins | +3 incubation slots |
| Nursery Expansion 2 | 10,000 coins | +5 incubation slots |
| Nursery Expansion 3 | 20,000 coins | +8 incubation slots |
| Training Hall | 15,000 coins | Unlock wayreader training |
| Training Hall 2 | 30,000 coins | More training slots |
| Rune Workshop | 25,000 coins | Unlock rune crafting |
| Rune Workshop 2 | 60,000 coins | More rune slots |

---

## Linking to Other Mechanics

This page links to:

- **[[Technology Tree]]**: Technology unlock progression per universe
- **[[Currency]]**: Research and patch costs
- **[[Satellite Durability]]**: Degradation and repair
- **[[Gameplay Loop]]**: How research fits into the loop
- **[[Companions]]**: Companions who assist with research
- **[[Production Facility]]**: How research improves production
- **[[Missions]]**: How new instruments unlock new missions
- **[[Orbital Capacity]]**: How research improves capacity

---

## Future Expansions (TODO)

- [ ] Add event-based research opportunities
- [ ] Add collaborative research (with friends)
- [ ] Add experiment system for testing new theories
- [ ] Add lab customization/cosmetics
- [ ] Add rare research outcomes (critical success)
- [ ] Add research shortcuts beyond time skips
- [ ] Add lab prestige (reset for bonuses)
- [ ] Add more Fantasy magical traditions
- [ ] Add more Alien technology types
- [ ] Add more Sci-Fi quantum branches

---

## See Also

- [[Companions]] - Companion roles in R&D
- [[Currency]] - Currency requirements
- [[Technology Tree]] - Technology unlocks
- [[Gameplay Loop]] - Research cycle
- [[Missions]] - Instruments for missions