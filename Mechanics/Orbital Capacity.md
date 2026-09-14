# Orbital Capacity

This page describes how many satellites can orbit each planet/celestial body. Each universe has its own rules.

## Core Principle

Each universe has **orbital capacity per celestial body**. When a planet reaches its capacity:
- New satellites cannot be launched to that planet
- Can only do missions with satellites assigned to this planet
- To add new satellites, you must either:
	- Buy new orbital slots
	- Research obital capacity (global research)
	- Retire old satellites (Free up slots)

Orbit capacity is inspired by real orbital mechanics:
- Real satellites compete for limited orbital slots
- Too many satellites in the same orbit increases collision risk (Kessler Syndrome)
- Radio frequency interference becomes unmanageable

---

## Earth / Solar System

### Base Orbital Capacity
Each planet starts with a small base number of orbital slots:

| Planet      | Base Capacity | Base Power Source |
| ----------- | ------------- | ----------------- |
| Earth Orbit | 20 slots      | Solar + Battery   |
| Moon        | 5 slots       | Solar + Battery   |
| Mars        | 30 slots      | Solar + RTG       |
| Jupiter     | 50 slots      | Solar + RTG       |

### How It Works
- When you launch a satellite to a planet, it's assigned to an orbital slot
- Each slot can host one satellite at a time
- Slots on one planet are **independent** of slots on another planet

### Orbital Capacity Research (Global)
The Laboratory (Research) tree has a branch that **increases capacity across all planets**:

> #TBD - research probably takes time only, without coins (or maybe no time, but coins only)

| Research               | Effect               | Cost (approx.) |
| ---------------------- | -------------------- | -------------- |
| Mission Control Tier 1 | +1 slot per planet   | 100 Coins      |
| Mission Control Tier 2 | +3 slots per planet  | 500 Coins      |
| Mission Control Tier 3 | +5 slots per planet  | 1,200 Coins    |
| Relay Network          | +10 slots per planet | 3,000 Coins    |
| Enhanced Tracking      | +15 slots per planet | 5,000 Coins    |
| Deep Space Network     | +25 slots per planet | 8,000 Coins    |

**Mechanic**: This research unlocks additional ground stations and relay satellites, improving the Mission Control team's ability to track more objects simultaneously.

### Direct Slot Purchase (Per-Planet)
Players can also buy capacity for specific planets using Coins:

| Planet | First Purchase (1 slot) | Subsequent Slots |
|-------|------------------------|------------------|
| Earth Orbit | 50 Coins | 500 Coins each |
| Moon | 100 Coins | 1,000 Coins each |
| Mars | 150 Coins | 1,500 Coins each |
| Jupiter | 300 Coins | 3,000 Coins each |

**Why bigger planets start cheaper**: They physically have more orbital real estate, so the first slot is "cheaper" but costs rise quickly to balance the total capacity.

### Orbital Slots Are Planet-Specific
- Earth's slots are independent of Mars' slots
- You can max out Mars without affecting Earth capacity
- This allows players to focus on their favorite planets first

---

## Andromeda Galaxy

### Base Orbital Capacity
Planets in Andromeda have different starting capacities:

| Planet | Base Capacity | Base Power Source |
|-------|---------------|-------------------|
| Planet A | 10 slots | Solar + Fission |
| Planet B | 15 slots | Solar + Fission |
| Andromeda Core | 50 slots | Ancient Energy Network |

### How It Works
- Same slot mechanics as Earth (one satellite per slot)
- Capacity grows as you reactivate ancient artifacts (this is quest-progression tied)

### Orbital Capacity Research (Global)
Andromeda has its own research track for capacity:

| Research | Effect | Cost (approx.) |
|---------|--------|----------------|
| Dispatch Computer Mk1 | +1 slot per planet | 200 Coins (Andromeda currency) |
| Dispatch Computer Mk2 | +3 slots per planet | 800 Coins |
| Dispatch Computer Mk3 | +5 slots per planet | 2,000 Coins |
| Network Decryption | +10 slots per planet | 5,000 Coins |

### Direct Slot Purchase (Per-Planet)
Same pattern as Earth, but with Andromeda-specific costs.

---

## Sci-Fi Future World

### Base Orbital Capacity
Sci-Fi universe has more distant, exotic locations:

| Location | Base Capacity | Base Power Source |
|----------|---------------|-------------------|
| Inner Galaxy | 20 slots | Solar + Fusion |
| Outer Galaxy | 10 slots | Fusion only |
| Event Horizon | 5 slots | Quantum Entanglement |
| Dyson Sphere | 100 slots | Zero-Point Energy |

### How It Works
- Slots are tied to **interference-free communication channels**
- Each slot represents one entanglement pair
- Without enough entanglement pairs, satellites can't communicate, can't be coordinated

### Orbital Capacity Research (Global)
Sci-Fi capacity is quantum-technology based:

| Research | Effect | Cost (approx.) |
|---------|--------|----------------|
| Entanglement Pair Generation | +1 slot per location | 500 Sci-Fi Coins |
| Quantum Repeater Tier 1 | +3 slots per location | 2,000 Coins |
| Quantum Repeater Tier 2 | +5 slots per location | 5,000 Coins |
| Full Repeater Network | +15 slots per location | 15,000 Coins |

---

## Magic Fantasy World

### Base Capacity - Stables (Not Orbits)
Magic Fantasy uses **stables** instead of orbital slots. Each **realm** has its own capacity:

| Realm        | Base Stable Capacity |
| ------------ | -------------------- |
| First Realm  | 5 slots              |
| Second Realm | 10 slots             |
| Third Realm  | 15 slots             |
| Fourth Realm | 20 slots             |
| Fifth Realm  | 25 slots             |

### How It Works
- Dragons live in stables between missions
- Each stable slot can house one dragon
- **Riders (Handlers/Wayreaders)** are a separate global pool #TBD - not sure if riders are needed to add more friction, maybe dragons with stable slots are enough
- A dragon can only be assigned to a mission if there's an available rider to guide it #TBD - look higher
- **Stables are per-realm**, Riders are **global** (one track for all realms) #TBD

### The Network Questline Effect
When you complete the main story questline (creating the Skyward Chart/rune network):
- Capacity unlocks jump from Dragon Handlers → Wayreaders
- This is a one-time flavor upgrade in the tree, not a mechanical change

### Stables vs. Riders Split
#TBD - probably no riders needed, just dragons, or dragon with rider pair
- **Stable Capacity Research**: Each realm has its own research line to expand stables
  - "Stable Construction Tier 1" = +1 slot to this realm only
  - Flavored as "expanding the stables in this realm"
- **Rider Capacity**: Single global research track (same as orbital research elsewhere)
  - "Dragon Handler Tier 1" → "Wayreader Tier 1"
  - Affects all realms simultaneously

---

## Degradation Impact on Capacity

As satellites age, they become less efficient:
- Health drops → slower mission completion

**This creates the retirement incentive**:
- Old satellites slow down, consume resources for patches
- You can:
  1. **Retire** them → free up orbital/stable slot immediately
  2. Build a brand new satellite (takes time + resources)
  3. Use them at lower speed / power level

> [[Technology Tree]] | [[Satellite Durability]] | [[Production Facility]] | [[Power Systems]]