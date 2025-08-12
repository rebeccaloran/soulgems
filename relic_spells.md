# Soul Gems — Relics & Spells (v0.6 Preview)

This document defines the **Dominion-style** card layer for Soul Gems:  
- **Relics** = **Permanent Enchantments** (unique engines you keep all game once drafted/claimed)  
- **Spells** = **Instants / Single-Use Tactics** (one-shot plays; then discard)

These are designed to sit on top of **v0.5** core rules and balance guardrails.

> **Core Guardrails (carry over from v0.5):**
> - Accuracy caps: **min 5% / max 95%**.  
> - Per-attack caps: **+25%** max to-hit, **+2 damage/hit** max, **max one** reroll/advantage effect.  
> - Ability activations: **max 2 activations/turn** (Relic activations + Spells). Passive Relics don’t consume activations.  
> - Convert: **2 SP → 1 LP**, up to **20 SP** converted **per turn** total (Relics that convert still count toward the cap).  
> - Gem: **Break 3d6 ≥ 12**, **Repair 3d6 ≥ 10**, no **back-to-back** repair denial.

---

## Draft & Market Flow

1) Reveal **8 Relics** (Permanent Enchantments, unique).  
2) **Snake draft**: each player chooses **2** Relics (they are now **exclusive** to that player).  
3) Reveal **8 Spell piles** (Instants), **3 copies** per pile. Spells can be bought mid-game.  
4) Any **undrafted Relic** may be **claimed once mid-game** by paying its **Buy Cost** (still unique).

**Costs notation:**
- **Relics** show **Unlock** (for draft) and **Buy** (mid-game claim) costs.  
- **Spells** list a single use cost.

You may pay costs from **LP**, **SP**, or any mix unless noted.

---

## Relics (Permanent Enchantments — Unique)

### LP (life/sustain)

**Iron Citadel** *(Passive)*  
- **Effect:** Once each **opponent turn**, prevent the **first 1 damage** to any one of your pieces.  
- **Unlock:** 6 LP • **Buy:** 15 LP • **Tags:** defense, sustain

**King’s Aegis** *(Passive)*  
- **Effect:** Attacks against your King suffer **−5%** to hit (counts against attacker’s +25% cap).  
- **Unlock:** 6 LP • **Buy:** 18 LP • **Tags:** king, defense

---

### SP (soul/summon)

**Soul Foundry** *(Passive)*  
- **Effect:** Gain **+3 SP** each **Upkeep**. *(During Upkeep, only your single highest SP engine produces.)*  
- **Unlock:** 6 SP • **Buy:** 18 SP • **Tags:** econ

**Phantom Gate** *(Passive)*  
- **Effect:** Your **Summons cost −2 SP** (min 0). **Teleports −1** (min 1).  
- **Unlock:** 5 SP • **Buy:** 15 SP • **Tags:** summon, mobility

---

### Hybrid (bridge/positioning)

**Coordinated Doctrine** *(Passive)*  
- **Effect:** If **2+** of your pieces can target the same defender, the **primary** and **one secondary** attacker each gain **+5%** to hit (counts toward +25% cap).  
- **Unlock:** 5 LP & 5 SP • **Buy:** 15 LP & 15 SP • **Tags:** offense

**Overclock Array** *(Activated, 1/turn)*  
- **Effect:** One piece gets **double movement range** this turn. *(Activation consumes 1 of your 2/turn ability uses.)*  
- **Unlock:** 6 LP & 6 SP • **Buy:** 18 LP & 18 SP • **Tags:** mobility

---

### Dice (odds control)

**Fate Engine** *(Activated, 1/turn)*  
- **Effect:** **Reroll one die** in any roll. *(Cannot stack beyond the “one advantage/reroll per attack” limit.)*  
- **Unlock:** 6 LP • **Buy:** 18 LP • **Tags:** dice, control

**Statistical Aim** *(Passive)*  
- **Effect:** **Once/turn**, if an accuracy roll misses by **≤5**, treat it as a **hit**.  
- **Unlock:** 5 LP • **Buy:** 15 LP • **Tags:** dice, offense

---

### Ritual (sacrifice/spike)

**Blood Economy** *(Passive)*  
- **Effect:** When you **sacrifice** one of your pieces, gain **+1 SP per piece value** (in addition to any other effects).  
- **Unlock:** 0 • **Buy:** 10 LP • **Tags:** sacrifice, econ

**Gem Masonry** *(Passive)*  
- **Effect:** You get **+1** to **Gem Repair** rolls; foes get **−1** on **Break** rolls against you. *(Still roll 3d6; modifies the total.)*  
- **Unlock:** 6 LP • **Buy:** 18 LP • **Tags:** gem, defense

---

### Wildcards (meta)

**Siege Workshop** *(Activated, 1/turn)*  
- **Effect:** Before **your** Gem Break attempt, add **+1** to that roll (stacks with nothing else).  
- **Unlock:** 6 SP • **Buy:** 18 SP • **Tags:** gem, offense

**Conversion Nexus** *(Activated, 1/turn)*  
- **Effect:** Convert **up to 6 SP → 3 LP** **without using Main 2**. *(Still counts toward the **20 SP**/turn conversion cap.)*  
- **Unlock:** 5 LP & 5 SP • **Buy:** 15 LP & 15 SP • **Tags:** econ, timing

> **Engine stacking rule:** During Upkeep, only your **single highest LP engine** and **single highest SP engine** produce. Prevents runaway stacking.

---

## Spells (Instants / Single-Use Tactics)

### LP school

**Iron Reserves** — *(12 LP)*  
- Prevent all damage to **one piece** **this turn**.

**Reserve Stockpile** — *(9 LP)*  
- Gain **+3 LP** at the start of each of your next **3 Upkeeps**.

**Guardian’s Oath** — *(18 LP; max 2 uses/game)*  
- **Cancel** a single opponent ability **this turn** (Relic activation or Spell).

**King’s Guard** — *(14 LP)*  
- Attacks against your King suffer **−10%** to hit **this turn**.

---

### SP school

**Reaper’s Strike** — *(14 SP)*  
- One attacker deals **+2 damage per hit** **this turn**. *(Respects +2 dmg/hit cap.)*

**Soul Torrent** — *(12 SP)*  
- You gain **+10%** to all accuracy rolls **this turn**. *(Counts toward +25% cap.)*

**Specter’s Veil** — *(12 SP)*  
- One of your pieces is **untargetable** until your next turn; it also **cannot attack** during that time. *(Not usable on Kings.)*

**Gem Shock** — *(14 SP; 1/game; respects no-back-to-back rule)*  
- Opponent **cannot attempt Gem Repair next turn**.

---

### Hybrid school

**Coordinated Strike** — *(3 LP & 3 SP)*  
- Each additional attacker beyond the first gets **+10%** (cap **+20%**, counts toward the +25% cap).

**Phase Shift** — *(2 LP & 2 SP)*  
- One piece **ignores intervening pieces** for movement **this turn**.

**Soul Forge** — *(5 LP & 5 SP)*  
- **Summon** one piece; it also gains **+10%** to hit **this turn**.

**Pulse Barrier** — *(12 LP & 12 SP)*  
- Prevent any attacks against your **King** **next turn**.

---

### Dice school

**Lucky Shot** — *(9 SP)*  
- Roll accuracy **twice**, take the better. *(Still respects the “one advantage/reroll per attack” limit.)*

**Loaded Fate** — *(15 LP)*  
- **Reroll one die** in any roll.

**Critical Edge** — *(12 LP)*  
- If your hit succeeds by **≤5**, deal **+1 damage** (after all other modifiers).

**Chaos Surge** — *(15 SP; 1/game)*  
- Roll **1d6**; on a **6**, gain an **extra Main Phase 1** immediately.

---

### Ritual school

**Blood for Souls** — *(Free; 1/game)*  
- **Sacrifice** one of your pieces: gain **SP = 2× its value**.

**Rebirth Pact** — *(—; 1/game; pay when used)*  
- **Lose 20 LP**: return a captured piece to your camp.

**Eternal Binding** — *(10 LP)*  
- Target enemy (not King) **can’t move for 2 turns**. They may pay **10 LP** at their turn start to end it early.

**Sealed Gem** — *(12 LP; 1/game)*  
- Opponent **gains no SP from captures** next turn.

---

### Classic (optional) — Soul Steal as a Spell

**Soul Steal** — *(1/game)*  
- If you have **≥1** piece adjacent (8-ring) to the target (not King), pay **(8 − #adjacent)** **LP** **and** **SP** to attempt a steal:  
  Roll **d100**; **success** if `d100 ≤ 20 × (#adjacent, max 4 → 80%)`.  
  On success, move the piece to your **Soul Gem**. On failure, that target can’t be attacked/targeted again **this turn**.

---

## Play Notes & Balance Guidance

- **Market seeding:** Every 8-Relic/8-Spell market should include **at least one** of: *Reaper’s Strike*, *Coordinated Doctrine*, *Fate Engine*, or a mobility piece (*Overclock Array*, *Phase Shift*). This ensures captures don’t stall.  
- **Tempo:** Keep **Pass = +6 LP**. It encourages recovery without making turtling optimal.  
- **Economy stacking:** Enforce the **single highest engine produces** rule to avoid runaway econ.  
- **Anti-lock:** Respect the **no consecutive repair denial** rule with *Gem Shock* and similar effects.

---

*Drop this file into your repo as `relic_spells.md`. When we move to v0.6, these become official and the draft will use Relics + Spells by default.*
