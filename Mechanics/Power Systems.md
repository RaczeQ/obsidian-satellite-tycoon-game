# Power Systems

This page describes the power systems available across all universes. Each universe has unique power sources that scale in efficiency and versatility.

## Core Principle

All satellites need a power source to operate their instruments and communicate. The choice of power source depends on:
- **Distance from the star** (for solar-powered systems)
- **Mission duration** (longer missions drain more power)
- **Environmental conditions** (eclipse, radiation, etc.)

Across universes, power systems represent technological progression:
1. **Solar + Battery** (baseline, works close to stars)
2. **Radioactive/Nuclear** (RTG, fission, fusion - works anywhere)
3. **Advanced systems** (antimatter, AI self-sustaining, magic)

**Important Notes**:
- Solar efficiency decreases with distance from the star (**inverse-square law**)
- Nuclear-powered satellites (RTG/Fusion) don't rely on the star and work anywhere
- **No permanent power loss** - when power runs low, satellites degrade (work slower) but don't die
- Satellites can be **retired** when they become inefficient

> [[Technology Tree]] | [[Satellite Durability]] | [[Currency]] | [[Gameplay Loop]]

---

## Earth / Solar System

### Power Sources

#### 1. Solar Panels + Battery
- **Primary power source** for inner planets (Mercury through Mars)
- Solar panels generate electricity when exposed to sunlight
- Battery stores excess energy for eclipse periods (when satellite enters planet's shadow)

**How it works**:
1. Solar panels generate power proportional to distance from the Sun
2. Excess power charges the on-board battery
3. During eclipse or night time, battery discharges to keep instruments running
4. When battery is depleted, instruments continue to run on residual power but degrade

**Degradation**: Solar battery satellites have **manual R&D patching** (see [[Satellite Durability]]).

**Power Recharge Time**: Depends on solar intensity and battery size.

| Planet | Solar Intensity | Recharge Time | Notes |
|-------|----------------|---------------|-------|
| Mercury | Very High (6-7x Earth) | ~5-10 min | Barely uses fuel, almost infinite power |
| Venus | High (~2x Earth) | ~8-12 min | Excellent solar reception |
| Earth | Baseline | ~15-20 min | Standard conditions |
| Moon | Same as Earth location | Same as Earth | Shared orbit with Earth |
| Mars | Moderate (~43% Earth) | ~25-35 min | Noticeably longer recharge |
| Jupiter | Low (<4% Earth) | ~60-90+ min | Solar becomes impractical |
| Outer Planets | Negligible | Hours to days | Solar **doesn't work** past Mars |

#### 2. RTG (Radioisotope Thermoelectric Generator)
- **Nuclear power source** that works **anywhere** in the solar system
- Uses radioactive decay (typically Plutonium-238) to generate heat
- Heat is converted to electricity via thermoelectric effect

**How it works**:
1. RTG produces constant power output regardless of distance from star
2. Power output is lower than optimal solar panels on inner planets
3. Power output slowly **degrades over time** due to radioactive decay (half-life: ~87.7 years for Pu-238)

**Degradation**: **Manual R&D patching** (see [[Satellite Durability]]). Players must use Lab time to queue a "RTG efficiency" research project that extends fuel life.

**Power Output Comparison**:

| System | Initial Output | After 10 Missions | After 50 Missions | After 100 Missions |
|--------|---------------|------------------|------------------|-------------------|
| Solar (Mercury) | 100% | ~100% | ~100% | ~100% |
| Solar (Jupiter) | 4% | ~4% | ~3% | ~2% |
| RTG (All Planets) | 50% | ~48% | ~40% | ~32% |

**Recharge Time**: RTG doesn't "recharge" - it's continuous power generation. Instead, it has a **fuel depletion** effect:
- As RTG fuel degrades, satellite missions **slow down** by 5-15% (depending on system age)
- No battery needed, instruments run continuously until fuel is very low

### Visual Indicators

**Solar Satellite Card**:
- Sun icon - Shows current solar panel efficiency (1-3 filled suns)
- Battery icon - Shows battery charge level (0-100%)
- When solar doesn't work (Jupiter+): Icon is greyed out with lock symbol

**RTG Satellite Card**:
- RTG icon - Shows nuclear power level (0-100%)
- Slow animation - Indicates continuous but diminishing power

---

## Andromeda Galaxy

### Power Sources

#### 1. Solar Panels + Battery
- Works for planets **within the Andromeda's central bright region**
- Same inverse-square law principle as Earth's solar system
- **BUT** the Andromeda galaxy's core is billions of times brighter than the Sun

**Important Note**: For planets too far from Andromeda's core, solar power becomes impractical (same issue as Jupiter in Solar System).

#### 2. Fission Reactor (Kilopower)
- **Compact nuclear fission reactor**
- Works **anywhere** in the galaxy (doesn't rely on star)
- **Real technology**: NASA's Kilopower demonstration (2018) proved feasibility
- Produces 1-10 kilowatts (compared to RTG's few hundred watts)

**How it works**:
1. Fission reactor splits uranium/fissile material
2. Heat from fission is converted to electricity
3. Can continuously power instruments indefinitely

**Degradation**: **Automatic patching** (see [[Satellite Durability]]). Once Fission research is unlocked, satellite failures are detected and fixed automatically without player input.

**Power Output Comparison**:

| System | Initial Output | Degradation Style |
|--------|---------------|------------------|
| Solar (Near Core) | 100% | Standard solar eclipse cycle |
| Solar (Outer Regions) | 10-40% | Fails in outer galaxy |
| Fission | 80% | Very slow degradation (2-5% per 100 missions) |

**Recharge Time**:
- Solar: Standard eclipse cycle
- Fission: **No recharge** - continuous output

**Why Fission over RTG?**: Fission produces significantly more power than RTG for the same mass, making it the preferred choice for deep-space missions in Andromeda.

### Visual Indicators

**Solar Satellite Card**:
- Sun icon - Brighter sun icon due to Andromeda's core
- Battery icon - Same as Solar System

**Fission Satellite Card**:
- Fission icon - Shows reactor power level
- Auto-fix icon (if researched) - Indicates automatic repairs

---

## Sci-Fi Future World

### Power Sources

#### 1. Solar Panels + Battery
- Same as other universes, but **scaled for a super-giant star**
- The star in the Sci-Fi universe is much larger and brighter than the Sun
- Solar power works effectively even at distances where other stars would make it impossible

**Note**: Solar is still a **cheap, baseline option** - used for inner-system missions where possible.

#### 2. Compact Fusion Reactor
- **Controlled nuclear fusion** reactor (deuterium-tritium or D-He3)
- **Works anywhere** - independent of star
- **Most powerful conventional power source** - orders of magnitude better than fission

**How it works**:
1. Drone carries fusion fuel (deuterium and helium-3)
2. Fusion reaction generates massive amounts of energy
3. Energy stored in high-capacity onboard batteries

**Degradation**: **AI self-healing** (see [[Satellite Durability]]). All failures are fixed automatically by on-device AI without player input.

**Power Output Comparison**:

| System | Initial Output | Degradation Style |
|--------|---------------|------------------|
| Solar | High (super-star) | Standard eclipse cycle |
| Fusion | **500-1000%** of Solar | Very slow degradation (~1% per 100 missions) |
| Fusion (Antimatter Upgrade) | **2000-5000%** of Solar | **No degradation** - truly sustainable |

**Recharge Time**:
- Solar: Standard eclipse cycle
- Fusion: **Very fast** (10-30 min due to high capacity)

#### 3. Antimatter (Unlock via Dyson Sphere)
- **Matter-antimatter annihilation** for power
- **Only available AFTER Dyson Sphere is complete**
- Dyson Sphere produces massive energy surplus which is used to create antimatter fuel
- Once unlocked, antimatter drones can operate anywhere with infinite fuel

**How it works**:
1. Dyson Sphere collects star's entire energy output
2. Energy is converted to matter-antimatter pairs
3. Drones consume pre-fabricated antimatter fuel

**Degradation**: **AI self-healing** with **no fuel degradation** - truly permanent once Dyson Sphere is online

**Recharge Time**: **Instant** (antimatter doesn't decay, drones draw from Dyson Sphere network)

**Why this sequence?**:
- **Compact Fusion** is believable near-term tech
- **Antimatter** requires Dyson Sphere as a prerequisite (realistic - antimatter is expensive to create)
- **Zero-point energy** is kept out of reach for drones (it's the realm of the Concord Array quantum computer)

### Visual Indicators

**Solar Satellite Card**:
- Super sun icon - Glowing multi-color super-giant star
- Battery icon - Large battery capacity

**Fusion Satellite Card**:
- Fusion icon - Animated flame/plasma effect
- AI icon - Self-healing active
- Fast recharge indicator

**Antimatter Satellite Card**:
- Antimatter icon - Glowing purple/orange
- "Infinite" badge - No degradation
- Dyson Sphere linked - Shows energy source

---

## Magic Fantasy World

### Power Sources

Dragons don't use conventional power sources. They are living creatures that sustain themselves through biological processes.

#### Dragon Power Cycle

| State | Action | Energy Source | Duration |
|-------|--------|---------------|----------|
| Awake | Flying missions | Consumes stored energy | Limited time |
| Sleep | Resting in stable | Recharges slowly | Variable |
| Eat | Consuming food | Rapid recharge + healing | Variable |

**How it works**:
1. Dragon starts with 100% energy (fed by player/hatched)
2. As dragon flies missions, energy depletes
3. Dragon must enter **sleep state** or **eat** to recharge
4. After recharging, dragon can continue missions

**Degradation**: **No degradation** - dragons don't break, they age. When a dragon becomes very old, the player can choose to retire them for a **feel-good bonus moment**.

**Recharge Methods**:

| Method | Recharge Time | Bonus |
|--------|--------------|-------|
| Sleep | 5-15 min (varies by dragon age) | Basic recharge |
| Eat | 2-5 min | Fast recharge + health bonus |
| Rare Foods (Herbs, Magic Fruits) | 1-2 min | Fast recharge + experience |

**Dragon Age Factors**:
- Older dragons recharge **slower** when sleeping
- Young dragons hatch directly into stables (skip initial training)
- Certain rare bloodlines have faster metabolism

### Visual Indicators

**Dragon Card**:
- Dragon sprite (changes color based on mood/state)
- Energy bar (0-100%) - Visual indicator of power level
- Sleeping dragon icon - When recharging
- Food icon - When eating to recharge
- Age badge - Current dragon age

**Sleep State**:
- Dragon shown curled up in stable
- Small animated "zzz" or breathing effect
- Timer counts down to next wake time

**Eat State**:
- Dragon shown with food
- Fast recharge animation
- Health and energy both replenish

---

## Power System Progression Summary

| Universe | Primary Power Sources | Degradation Handling | Special Notes |
|----------|----------------------|---------------------|---------------|
| Earth | Solar + Battery, RTG | Manual R&D patching | Classic sci-fi progression |
| Andromeda | Solar + Battery, Fission | Auto-fix (if unlocked) | Kilopower = real tech |
| Sci-Fi | Solar + Battery, Fusion (to Antimatter) | AI self-healing | Fusion first, antimatter via Dyson Sphere |
| Fantasy | Dragon Sleep/Eat Cycle | Retire old dragons | No repair, but no permanent loss |

---

## Implementation Details

### Universal Mechanics

**1. Power Recharge Cycle**:
- All power systems have a recharge cycle when battery/power is depleted
- Recharge time is displayed on satellite card
- During recharge: satellite is **paused** (cannot accept new missions)
- Once recharged: satellite resumes normal operations

**2. Power Degradation (Non-Power Sources)**:
- When battery/power reaches critical level (e.g., <25%), satellite still functions but slower
- Degradation causes: **slower mission completion time**, **lower currency yield**
- **Never kills satellite** - they become inefficient but keep working

**3. Patch Queue (for Non-Perpetual Power)**:
- Solar and RTG satellites can be queued for R&D power upgrades
- While patched, satellite is temporarily unavailable
- Patch restores a portion of power/fuel efficiency

**4. Retirement (for Perpetual Sources)**:
- Fantasy dragons can be "retired" when too old
- Retirement gives **feel-good bonus** currency
- Slot in that planet's stable becomes available

### Visual Design

All power states should be **visually clear** at a glance:

| Power Source | Icon | Color | State Visual |
|--------------|------|-------|--------------|
| Solar + Battery | Sun + Battery | Yellow/Green | Sun icon brightness + battery fill |
| RTG | RTG | Orange/Red | Glowing icon with fuel meter |
| Fission | Fission | Blue/White | Cool reactor glow |
| Fusion | Fusion | Purple/Blue | Animated plasma |
| Antimatter | Antimatter | Silver/Purple | Sparkle/energy field |
| Dragon (Awake) | Dragon | Color varies | Flying animation |
| Dragon (Sleep) | Sleeping Dragon | Muted color | Curled up in stable |
| Dragon (Eat) | Dragon + Food | Bright | Eating animation |

---

## Universe-Specific Tips for Players

### Earth / Solar System
- **Inner planets** (Mercury, Venus, Earth, Moon): Use **Solar + Battery** satellites - cheaper
- **Outer planets** (Jupiter+): Must use **RTG** - solar too weak
- **Keep an eye on battery levels** during eclipse season
- **Patch solar panels** before they degrade too much

### Andromeda Galaxy
- **Near the core**: **Solar + Battery** works great (Andromeda's core is bright!)
- **Outer regions**: Use **Fission** - solar becomes unreliable
- **Fission unlocks automatic fixes** once researched - highly recommended

### Sci-Fi Future
- **Early chapter**: **Solar + Battery** for inner systems
- **Mid-game**: **Fusion** - much more reliable, faster recharge
- **Late-game**: **Antimatter** (after Dyson Sphere complete) - unlimited power
- **AI repairs everything** - no maintenance needed!

### Magic Fantasy
- **Just accept it** - dragons run on food and sleep
- **Feed your veterans** - older dragons benefit most from food
- **Retire the ancient ones** - emotional payoff, frees up space

---

## Power Sources in Technology Tree

The power system technologies are integrated into the [[Technology Tree]] as follows:

| Universe | Tech Tree Branch | Description |
|----------|-----------------|-------------|
| Earth | Power Upgrades | Solar Efficiency to RTG Systems |
| Andromeda | Power Systems | Solar Optimization to Fission Reactors |
| Sci-Fi | Power Systems | Fusion Reactors to Dyson Sphere Project to Antimatter Synthesis |
| Fantasy | Dragon Care | Stable Upgrades to Feeding System to Breed Selection |

---

> [[Satellite Durability]] - How degradation varies by power source
> [[Currency]] - How to afford better power systems
> [[Companions]] - Companions that help with power management
> [[Gameplay Loop]] - How power affects mission execution

---

*Last updated: [Date]*