# Soul Gems — Field & Terrain Module (Public Works Edition)
*Compatible with Core v0.5. All effects are symmetric. No changes to core math.*

> Everything added to the board (tiles, roads, portals, shrines, NPCs, weather nodes) becomes **public terrain**. Either player may benefit. Global caps always apply: **+25% to‑hit**, **+2 dmg/hit**, 2 activations/turn, SP→LP conversion 2:1 (≤20 SP/turn).

---

## 1) What This Module Adds
- **Field Draft** to expand the board before play.
- **In‑game builds** (roads/bridges/portals/shrines/bazaars/mints).
- **Neutral NPCs** as public hazards/objectives.
- **Weather** toggles as temporary global modifiers.
- All of the above are **public** and **destructible** (Structure Value = SV).

---

## 2) Board Size & Draft
- **Core Ranked:** 8×8 (default).  
- **Expanded Ranked:** up to **10×10** (recommended upper bound for vanilla relic set).  
- **Scenario/Campaign:** up to **32×32** with terrain helpers (roads/portals) or 5‑rank summon bands.
- **Connectivity:** Each added tile must touch the existing field **orthogonally** (no floating islands).
- **Choke Rule:** No 1‑file corridor longer than **3 tiles** unless there’s an alternate lane.
- **Draft Procedure (Pre‑game):** Players alternate placing one expansion tile at a time on the outer perimeter until the scenario quota is reached.

> DIY: draw the expanded grid on paper; see “Symbols” below.

---

## 3) Build Economy (In‑Game)
- **When:** **Main Phase 2** only.
- **Rate:** **1 Field purchase per M2** (does *not* use ability activations).
- **Slots per player:** `2 + floor(captured_value / 9)` (max **6**).  
  • **Roads:** **4 segments = 1 slot**.
- **Public Symmetry:** Once placed, features have **no owner**.
- **Destruction:** Target like a piece; defender value = **SV**. Upon destruction, attacker gains **SP = 5 × SV**. Remove the feature; any aura ends.

---

## 4) Features & Costs (Public Objects)

### 4.1 Infrastructure
| Feature | SV | Cost | Rules |
|---|---:|---:|---|
| **Road Segment** | 1 | **3 LP** | Entering a road tile grants **−1 distance** on that **move** (min 1). **4 segments = 1 slot**. |
| **Bridge** | 2 | **5 LP** | Creates a passable link across a gap; counts as Road. |
| **Waypoint / Portal (pair)** | 4 | **10 LP & 6 SP** | Move **onto A**, then **exit B** as the **next step** of the same move (**+1 distance** to exit). **Limit:** 1 pair per player placed; once placed, public. |
| **Fortified Outpost** | 3 | **8 LP & 4 SP** | **Aura r=2**: once/turn per acting player, **−1 distance** for an **attack** that starts inside the aura (min 1). |

### 4.2 Commerce & Civic
| Feature | SV | Cost | Rules |
|---|---:|---:|---|
| **Bazaar** | 5 | **10 LP & 10 SP** | **Once per turn total (global):** the **first** Relic/Spell purchase that turn costs **−3 LP** (min 0). Mark used. |
| **Mint** | 4 | **8 LP & 8 SP** | **End of current player’s turn:** convert up to **4 SP → 2 LP** **in addition** to core conversion, but still within the **20 SP/turn** cap. |
| **Shrine** *(choose one mode at placement)* | 3 | **6 LP & 4 SP** | **Aura r=2**: once/turn per acting player, one attack from inside the aura gains **+10% to‑hit** *or* **+1 dmg**. Contributes to global caps; self‑stacking on the same attack not allowed. |

### 4.3 Weather (Field Event)
| Feature | SV | Cost | Rules |
|---|---:|---:|---|
| **Weather Node** | 4 | **7 LP & 5 SP** | **Once/game:** set weather for **2 full rounds**. Options: **Fog** (LoS 3), **Rain** (ranged −1 dmg; Water +1 range), **Snow** (−1 move), **Storm** (+1 lightning dmg, −1 fire dmg). Public modifiers; caps apply. |

### 4.4 Neutral NPCs (Public Hazards)
| NPC | SV | Cost | Rules | Reward |
|---|---:|---:|---|---|
| **Trader** | 3 | **6 LP & 2 SP** | Stationary. **Visit** (end move adjacent): pay **3 LP** → gain a **Trader Token** (1/turn): **−2 LP** on your **next Field purchase** (min 0). | — |
| **Guardian** | 4 | **8 LP & 4 SP** | Hostile. On its phase, advances 1 toward nearest piece; attacks in range 1 (**to‑hit as Bishop (3)**). | **SP = 15** |
| **Wandering Beast** | 2 | **3 LP** | Random step to adjacent empty tile each NPC phase; blocks movement. | **SP = 10** |

> **Kings:** By default, NPCs do **not** target Kings unless no other targets are in range.

---

## 5) NPC Phase (No Third Party Needed)
**Default 1v1 — Opponent Operated NPC Phase (OONP)**  
- **When:** After each player’s **End** phase.  
- **Controller:** the **non‑active player**.  
- **Scripted Priority:** no discretion beyond listed tie‑breakers.

**Movement (each NPC):**  
1) Target nearest enemy (Manhattan). Tie → enemy **highest piece value**; still tie → **d6**.  
2) Step 1 tile closer (prefer orthogonal; if diagonal equally closer, controller chooses).  
3) If blocked, skip movement.

**Attack (each NPC):**  
1) If an enemy is in range (default 1), attack the **closest**. Tie → **highest piece value**; still tie → **d6**.  
2) **Accuracy:** standard d% rules; attacker value = **SV** unless the NPC specifies a piece type.  
3) **Damage:** 1 on hit unless specified. **Global caps apply.**  
4) **Kings:** only targeted if no other enemies are in range.

**Variants:**  
- **Two‑Window NPCs:** after **Upkeep** (move only) and after **End** (attack only).  
- **Tournament Team NPCs:** a rotating **NPC Captain** (by round) runs all tables using this script; teams may vote only on true ties; unresolved → **d6**.

---

## 6) Symbols (DIY Maps)
`▲` high ground · `~` water · `╬` bridge · `║/═` wall · `◎` NPC · `✦` weather node · `⛬` shrine · `⛨` outpost · `⟳A/B` portal pair labels

---

## 7) Guardrails (Large Maps)
1) **1 build per M2** and **slot caps** prevent runaway.  
2) **Distance floor = 1** even with roads/auras/portals.  
3) **No self‑stacking on the same attack** (take the single best aura).  
4) **Portals:** max **1 pair per player**; entering/exiting is movement; exit costs **+1 distance**.  
5) **Summon timing unchanged**; no feature grants extra Summon windows.  
6) **Connectivity & choke rules** prevent exploitative layouts.

---

## 8) Notation
- **Build:** `M2: Build Bazaar@e4 pay(10LP,10SP)`  
- **Use:** `Road used (−1 dist)` · `Portal A→B (+1 step)` · `Bazaar used (−3 LP)`  
- **NPC:** `NPC: Guardian e5→f5; Atk f5→N d% 41/65 ✓ dmg1`
