# Satellite Durability

This page describes how satellites degrade over time and how they can be repaired across different universes.

## Core Principle

Satellites **never die** in a permanent sense (they don't disappear from your inventory or count). Instead:
- Their **performance degrades** over time (slower missions, lower efficiency)
- They can enter a **"patch queue"** when they malfunction
- You can **retire** them for a small bonus if you want (one-way exit)

This design is intentional:
- Matches the "tycoon" genre philosophy (progress never reverses)
- Avoids frustrating player "loss" mechanics
- Reflects real spacecraft (they slow down, rarely crash unexpectedly)

> [[Technology Tree]] | [[Currency]] | [[Companions]] | [[Gameplay loop]]

---

## Health System

Every satellite has a **health percentage** (0-100%), shown as a small badge on the satellite card.

### Health Loss: Mission Wear
Each mission causes some wear and tear:

| Risk Level | Health Loss Range | Example Zones |
|------------|-------------------|---------------|
| Low | 2–6% | Earth orbit, Moon, Venus |
| Medium | 7–12% | Mars, Mercury |
| High | 10–18% | Jupiter, outer planets, magnetosphere zones |
| Extreme | 15–25% | Van Allen belts, high radiation areas |

The exact loss is **random** within the range when the mission completes.

### Critical Events (Rare)
Occasionally (~3-5% chance per mission), a **critical event** strikes:
- Solar flares / Coronal Mass Ejections (CME)
- Micrometeorite strikes
- Geomagnetic storms

These cause **extra damage beyond the normal wear** (e.g., a "High risk" mission might hit for 25% instead of 10-18%).

### When Health Gets Low

The satellites with low health will take longer to recharge and longer to run the missions.
Players will be incentivised to replace them with new ones.
### Permanent Retirement
You **can** retire a satellite (one-way removal):
- Click "Retire" on the satellite card
- Receive a small **salvage bonus** (coins) based on how complete the satellite is
- The slot in your production queue opens up
- The satellite disappears from the orbital capacity count

> [[Production Facility]] | [[Laboratory]]

---

## Repair by Universe

> Probably repairs will be disabled to simplify the gameplay loop. Just degradation with replacement.

Different universes handle degradation differently, creating a **progression ladder** as you unlock new universes:

### Earth / Solar System

**Manual Repair Required** (Player-Controlled)

When a satellite malfunctions (enters patch queue):
1. **Check** the satellite - you'll see a malfunction message
2. **Research a patch** in the Laboratory (queue in Mission Control area)
3. **Wait** for the patch to complete
4. Satellite returns to the patch queue, ready for more work

**Available Patch Types**:
- Minor glitches (quick, cheap)
- Serious anomalies (requires prerequisite tech)
- Radiation damage (R&D unlocks help)

**Player must manually order** all patches. This fits the "scrappy new company" tone - you're hands-on fixing your own satellites.

### Andromeda Galaxy

**Auto-Detection, Auto-Fix** (Research-Based)

When a drone malfunctions:
1. System **automatically detects** the anomaly
2. If the corresponding patch is **unlocked in R&D**, it auto-applies
3. If not unlocked, drone sits in patch queue waiting

**Player does NOT need to manually order** patches once the system is set up.

**Tech Tree Integration**:
- Unlock "Xeno-Ops Technicians" (personnel capacity)
- Unlock specific patch technologies in R&D
- Toggle "Auto-Fix Mode" in settings (defaults to OFF initially)

**Flavor**: The salvage computer from the ancient alien ruins diagnoses the problem and patches it automatically, using reclaimed alien hardware.

### Sci-Fi Future World

**Self-Healing AI** (Fully Automated)

When a satellite encounters an anomaly:
1. On-device AI **autonomously repairs** the malfunction
2. Player never needs to intervene
3. Only needs to **build/launch** more satellites to replace degraded ones

**No research or player input required** for repairs in this universe.

**Flavor**: Each satellite has an advanced repair system, powered by the Dyson Sphere's infinite energy.

### Magic Fantasy World

**No Failures** (Immune to Degradation)

**Dragons don't malfunction**:
- They're living creatures, not machines
- Their "degradation" is natural aging (they fly slower over time)
- They don't enter patch queues
- They don't have "malfunctions" - that's a mechanical problem

**Riders/Handlers** don't "fix" dragons either:
- If a dragon is tired, you just send it to **retire** and get paid a bonus
- This is the **only universe** where retirement is a "feel-good" moment

**Flavor**: Dragons are honored for a lifetime of service, then gracefully return to sleep.

---

## Power & Degradation Relationship

The power source affects how long a satellite can operate:

### Solar Panels
- Recharge from sunlight
- **Weaker with distance from the Sun** (inverse-square law)
- Planets are tiered by "Sun Rating":
  - **3 Suns** (Mercury, Venus): Barely uses fuel
  - **2 Suns** (Earth, Moon): Minimal fuel use
  - **1 Sun** (Mars): Some help, still burns fuel
  - **No Sun** (Jupiter, outer): Solar doesn't work → needs RTG/Fission/Fusion

### RTG (Earth)
- Decays over time (radioactive material)
- Slower recharge = faster degradation
- Past Jupiter becomes impractical

### Fission (Andromeda)
- Longer-lasting than RTG (fission fuel is concentrated)
- Better degradation resistance

### Fusion (Sci-Fi)
- Very long-lasting fuel
- Faster recharge than RTG
- Better fuel efficiency

### Dragon Energy (Fantasy)
- Requires feeding/sleeping cycle
- No mechanical degradation
- Slows gradually over decades

---

## Retirement vs. Replacement

When satellites get old, player can either keep using them since they are scarce, or retire them and replace with a new one (you can launch a new satellite and it will automatically replace old one - player will select it during the build dispatch)

---

## Implementation Tips

### UI Display
- Show health as a **small percentage badge** (not a big bar)
- Only shows when you hover/click on satellite
- Below 25%: Shows "Needs Patch" icon, no new missions

### Performance
- Each mission roll adds small random value
- Do NOT track "time since last patch" - it causes confusion
- Health is the single stat that matters

### Psychology
- **Never urgent**: Below 25%, they just sit in queue
- **Rare critical hits**: Feel like story events, not threats
- **Always recoverable**: Satellites come back when patched
- **Retirement is optional**: Players have a "safe exit" if they want

---

## Summary Table

| Universe | Health Behavior | Fix Method | Player Input |
|----------|----------------|------------|--------------|
| Earth | 0-100%, slow when low | Manual patches | Required |
| Andromeda | 0-100%, slow when low | Auto-fix if unlocked | Optional toggle |
| Sci-Fi | 0-100%, slow when low | AI self-heal | None |
| Fantasy | Slows with age, no malfunction | Retire for bonus | Only choice |

---

> [[Story Quests]] | [[Companions]] | [[Currency]] | [[Laboratory]]