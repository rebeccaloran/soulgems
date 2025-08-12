# Soul Gems

## Overview
Soul Gems is an advanced, Warhammer-style strategy game based on chess mechanics with layered combat, resource management, and a Dominion-style draft system. The twist: once you claim a **Permanent Enchantment** ability card, it’s yours alone for the rest of the game — no one else can have it.

Players manage **LP** (Life Points) and **SP** (Skill Points) while deploying attacks, capturing pieces, and unlocking powerful abilities to create custom "builds." Games are designed for high-stakes, multi-session campaigns.

---

## Core Rules

### 1. Piece Values
- Pawn = 1
- Knight / Bishop = 3
- Rook = 5
- Queen = 9
- King = Special (20 HP)

### 2. Damage & Capture
- Capturing a piece requires dealing damage equal to its value in HP.
- **Attack Cost Formula:** `2 × (Attacking Piece Value) + (Distance in squares)` LP.
- Attacks must be declared before rolling for accuracy.

**Example:**  
Attacking a Queen (9 HP) with:  
- Rook at d1 (distance 6) → cost = 2×5 + 6 = 16 LP  
- Knight at e5 (distance 3) → cost = 2×3 + 3 = 9 LP  
- Pawn at e6 (distance 1) → cost = 2×1 + 1 = 3 LP  
Total = **28 LP**.

### 3. Accuracy Rolls
- Roll **two 10-sided dice** (first = tens digit, second = ones digit) for a 1–100 result.
- A roll ≤ **Hit Threshold** counts as a hit.
- **Hit Threshold:** `20 + (10 × Attacker Value) - (10 × Target Value)` (min 5%, max 95%).

### 4. Capturing Rewards
- Capturing a piece grants: `5 × (Captured Piece Value)` SP.

### 5. LP and SP
- LP = Health + resource for attacks.
- SP = Currency for unlocking abilities, summoning, and special effects.
- You may convert SP → LP at 2:1, max 20 LP per turn.

---

## Dominion-Style Draft Phase
At game start, players **draft** from a shared pool of ability cards (face-up). The pool is composed of:

- **Permanent Enchantments (PE)** — Unique upgrades you keep the entire game. Once drafted, no other player can take it.
- **Single-Use Cards (SU)** — Spells, bursts, or one-time events. Discard after use.

### Draft Rules:
1. Each player begins with 10 Draft Points (DP), usable **only during setup** to acquire abilities.
2. Permanent Enchantments have higher DP cost (4–7 DP).  
3. Single-Use Cards cost 1–3 DP.
4. Unspent DP is lost after drafting.
5. Permanent Enchantments stay active all game; Single-Use Cards go to your “Arsenal” and can be played once per match.

---

## Ability Card Examples

### Permanent Enchantments
- **Soul Steal (6 DP)** — Whenever you capture a piece, heal LP equal to its value.
- **Reaper’s Strike (5 DP)** — All your attacks deal +2 damage on hit.
- **Coordinated Strike (4 DP)** — The second (and later) attacker in a multi-attacker volley gains +10% hit chance.
- **Gem Ward (7 DP)** — Enemy must roll 3d6 ≥ 14 to break your Gem instead of 12.

### Single-Use Cards
- **Ritual Sacrifice (3 DP)** — Sacrifice one of your pieces to gain SP equal to `5 × its value`.
- **Overdrive (2 DP)** — This turn, all attacks cost −4 LP (min cost = 2 LP).
- **Emergency Shield (1 DP)** — Prevent the next successful attack on any of your pieces this turn.

---

## Gem Mechanics
- Breaking a Gem (opponent’s) during your upkeep: roll 3d6 ≥ 12.
- Repairing your own Gem during upkeep: roll 3d6 ≥ 10.
- No player may break the same Gem two turns in a row.

---

## King Mechanics
- The King has 20 HP.
- If your King dies, you lose.
- Abilities affecting Kings stack normally.

---

## Win Conditions
- Eliminate the opponent’s King.
- Reduce the opponent’s LP to 0.

---

## Campaign Play
- Designed for **weeks/months-long sessions**.
- Players maintain LP/SP totals, ability inventory, and board state across sessions.
- Between matches, players may add new abilities to the shared pool for future drafts.

---

## Notes from Testing
- Mid-value captures (Rooks, Knights) are difficult without damage buffs — **ensure at least one damage buff PE is in the pool**.
- Gems create high-stakes tempo plays without soft-locking opponents.
- Permanent Enchantments add huge strategic depth; drafting phase is now *the* tension point.

---
