# SOUL GEMS — Core Rulebook (v0.5 • LOCKED)

> **Design intent:** This document captures the **immutable physics** of Soul Gems. Expansion sets, campaign books, and card packs **must not** change any rule here. All meta-shaping will happen via **Relics & Spells** and scenario modules that operate **on top of** this core.

---

## 0) Key Terms

- **LP (Life Points):** Your general resource pool. Many costs can be paid from LP and/or SP.
- **SP (Soul Points):** Earned from captures and Soul Gem income; fuels Summons, abilities, and conversions.
- **Camp:** Your first four ranks.
- **Distance:** Number of squares traveled along a legal move path (knights count jumps).
- **Soul Gem:** Your vault for captured/stolen pieces; also your SP engine.
- **Activation:** A non-passive ability use. You may **activate at most 2** abilities each turn (any mix of Relics/Spells). Passive effects don’t count.

---

## 1) Setup

1. Start with an **empty board**.
2. Each player places their **King** anywhere in their own **camp** (ranks 1–4 for White, 5–8 for Black).
3. All other pieces start **in your Soul Gem** (off board).
4. Each player begins with **20 LP** and **0 SP**.
5. Roll 3d6; higher chooses to play White or Black. (Reroll ties.)

---

## 2) Turn Structure

Each of your turns has five phases:

1. **Upkeep**  
   - Gain **SP** from your Soul Gem income (see §6).  
   - Optionally attempt **Gem Break/Repair** (see §6).  
   - Optionally **Summon** **one** piece from your Soul Gem (see §5).

2. **Main Phase 1**  
   - Move pieces (see §3).  
   - Activate abilities (max **2** activations total per turn across all phases).

3. **Battle Phase**  
   - Declare attacks, pay costs, roll accuracy, apply damage, resolve captures (see §4).

4. **Main Phase 2**  
   - Optional movement.  
   - **Convert SP→LP** at a rate of **2 SP → 1 LP**, up to **20 SP converted per turn** total.

5. **End**  
   - **Clear all partial damage** you dealt this turn (damage persists only during your turn).  
   - If you took **no actions at all** this turn, gain **+6 LP** (Pass).

---

## 3) Movement

- **Move Cost** = **piece value** + **distance**.  
  - Values: Pawn 1, Knight 3, Bishop 3, Rook 5, Queen 9. King is special (see §4.4).
- **Distance** can never exceed the piece’s legal move distance.  
- **Knights**: up to **2 jumps** per Move action, at **3 LP per jump**.  
- Movement and capturing are **separate** (captures happen in Battle Phase).

---

## 4) Combat

### 4.1 Attack Cost
- **Attack Cost** = **2 × (attacker’s piece value)** + **distance**.

### 4.2 Accuracy (2d10 → d100)
- Roll two d10: first die is **tens**, second is **ones**. “00” counts as 100.  
- **Hit if:** `d100 ≤ clamp(5, 20 + 10 × (AttackerValue − DefenderValue), 95)`.

### 4.3 Damage & Capture
- Each hit deals **1 damage**.  
- When damage dealt to a target **this turn** ≥ its **piece value**, **capture** it and move it to your **Soul Gem**.  
- On capture, gain **SP = 5 × captured piece value**.

### 4.4 The King (20 HP, converted on defeat)
- The King is not captured via thresholds. Instead, it has **20 total HP**.  
- **Hit vs King:** `d100 ≤ clamp(10 × attacker’s piece value, 5, 95)`.  
- When the King has taken **20** total damage, it is **converted**. The game ends.

### 4.5 Per-Attack Safety Caps
- Max **+25%** total to-hit bonus on any attack.  
- Max **+2** damage **per hit** after all effects.  
- Max **one** advantage/reroll source on a single accuracy roll.

---

## 5) Summoning & Teleport

- **Summon (Upkeep only):** Place a piece from your Soul Gem on **one of its starting squares** if free.  
  **Cost:** piece value + 5.  
  You may pay extra **(|Δx| + |Δy|)** to place farther **within your camp**.

- **Teleport (End only):** Same cost and limits as Summon, but target a piece **already on board**.

---

## 6) Soul Gems & Economy

- **SP Income (Upkeep):** Sum the values of **all pieces in your Soul Gem**, multiply by **2**, gain that much **SP**.  
  *(No SP on your first turn.)*

- **Break (Upkeep):** Pay **20**; roll **3d6**. On **12+**, target enemy Gem is **broken**:  
  - They **gain no SP** and **cannot Summon** until repaired.  
  - All of **your pieces** previously captured by that opponent are **returned to your Gem**.

- **Repair (Upkeep):** Pay **10**; roll **3d6**. On **10+**, your Gem is **repaired**.

- **No Repair Lock:** Rules modules may not create “permanent repair denial”.

---

## 7) Victory & Tiebreaks

- **Primary:** Convert the enemy **King** (reach **20** damage).  
- **Alternative:** Reach **1000 LP** (comedic/optional; allowed).  
- **Tiebreak after max turns** (if a scenario sets one): highest **King damage**; then **score** = captured value×3 + board value×2 + LP + SP.

---

## 8) Immutable Contract (Expansion Compatibility)

**Cards, expansions, and campaigns must not:**  
- Change **piece values**, **attack/move costs**, or **accuracy formulas**.  
- Bypass the **+25% to-hit**, **+2 dmg/hit**, or **single-reroll** caps.  
- Alter the **SP→LP** conversion **rate** (2:1) or the **20 SP/turn** conversion cap.  
- Remove or rewrite **Gem Break/Repair thresholds** (12+/10+ on 3d6).  
- Add effects that create **infinite loops** or **unbounded SP/LP**.  
- Deny **repair** on **consecutive turns** with the same player’s effects.  
- Change **Turn Structure** ordering.

**Cards may:**  
- Add **cost modifiers** (e.g., −1 distance, −2 SP on Summon) **within** caps.  
- Add **conditional accuracy bonuses** respecting the **+25%** cap.  
- Add **conditional extra damage** respecting the **+2 per hit** cap.  
- Provide **timing** and **draft/market** variants.  
- Introduce **scenario** win conditions (campaign books) that **do not alter combat math**.

---

© Rebecca Loran — Core rules locked for long-term stability.
