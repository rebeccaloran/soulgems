# Soul Gems — Human‑First Notation (v0.5)

A compact note‑taking system you can **scribble mid‑match** and still reconstruct the game later. Phase‑aware, pen‑and‑paper friendly, judge‑auditable.

---

## Goals
- **Fast to write** with minimal symbols.
- **Readable later** (you can replay the game).
- **Phase‑aware**: mirrors the locked core turn order.
- **Math‑lite**: totals tracked at phase ends, not every line.

---

## Legend (Cheat Sheet)

**Pieces:** `K Q R B N P`  
**Squares:** `a1`–`h8` (standard chess coordinates)

**Phases:** `U` (Upkeep) · `M1` (Main 1) · `B` (Battle) · `M2` (Main 2) · `E` (End)

**Actions:**  
- `Sm` = **Summon** (Upkeep only)  
- `Tp` = **Teleport** (End only)  
- `Mv` = **Move**  
- `Atk` = **Attack**  
- `Conv` = **Convert** SP→LP (2:1, cap 20 SP/turn)  
- `Brk` / `Rep` = **Gem Break** / **Repair** (Upkeep only)  
- `Rel` / `Spl` = **Relic activation** / **Spell cast**  
- `Pass` = Did nothing this turn (**+6 LP**)

**Symbols & Snips:**  
- `→` move/target arrow  
- `x` capture (append to the attack that captured)  
- `✓` success · `✗` fail  
- `d% r/t` = d100 roll result `r` vs threshold `t` (e.g., `d% 48/65 ✓`)  
- `3d6=13` for Gem rolls  
- `ΔLP+6` / `ΔSP−5` for quick total changes  
- `KD+1` = add 1 damage to King; track cumulative as `KD=7`  
- Costs: `pay7` or split `pay7 (3LP,4SP)`

**Activations:** mark `A*1`, `A*2` per turn (max 2). Passive relics don’t use activations.

---

## Game Header (write once)

```
Date / Table / Set: Core v0.5
Players: White = ____________    Black = ____________
King starts: W K@____   B K@____

Relics (W): ________________________________
Relics (B): ________________________________

Spell market (circle when bought): ____________________________
```

---

## Turn Block Template (use one block per player turn)

```
W1 U:  SP+__ ⇒ __ | Brk/Rep? | Sm: <P@sq> pay__ | notes
   M1: Mv: <piece sq→sq> pay__ | Rel: <name> A*1 | Spl: <name> A*2 | notes
    B: Atk: <Att@from → Tgt@sq> cost__ thr__ d% r/t ✓/✗ dmg__ [x <piece>] [+SP__]
       (repeat each attack as its own line)
   M2: Mv: ... | Conv: SP__→LP__ | notes
    E: Tp: <piece sq→sq> pay__ | KD=__ | LP=__, SP=__ | Pass? (+6 LP)
```

**Notes**
- Only record **what you actually did**. Blank bits can be skipped.  
- Damage to non‑King pieces clears at End. **King damage persists**: track as `KD=`.

---

## Minimal Mode (super fast jotting)

```
U: Sm Q@d1 pay14
M1: Mv Nd2→f3 pay5 | Rel: Overclock A*1
B: Atk Qd1→Rd7 cost19 thr80 d% 72/80 ✓ dmg1
B: Atk Nd2→Rd7 cost9 d% 33/50 ✓ dmg1 xRd7 +SP25
M2: Conv SP10→LP5
E: LP=26 SP=0 KD=0
```

---

## Common Patterns (how to write them)

### Summon / Teleport
- `U: Sm R@a1 pay10` *(5 + 5)*  
- `E: Tp Bc4→g8 pay(3 + distance)`

### Moves
- `M1: Mv Nb1→d2 pay5` *(3 + 2 distance)*  
- Multi‑jump Knight (if used): `Mv N: b1→d3→f4 pay6` *(3 per jump)*

### Attacks (non‑King)
- `B: Atk Rd1→Qd7 cost16 thr65 d% 48/65 ✓ dmg1`  
- If capture: append `xQd7 +SP45`

### Attacks vs King
- `B: Atk Qd1→K d% 44/90 ✓ KD+1  (KD=7)`  
  *(King threshold uses 10× attacker value, clamped to 5–95)*

### Gem Break / Repair
- `U: Brk pay20 3d6=13 ✓ (opp Gem Broken)`  
- `U: Rep pay10 3d6=9 ✗` or `3d6=10 ✓`

### Convert (SP→LP)
- `M2: Conv SP14→LP7` *(2:1, cap 20 SP/turn total)*

### Pass
- `E: Pass ΔLP+6` *(only if you took **no** actions that turn)*

### Relics / Spells
- `Rel: Fate Engine A*1`  
- `Rel: Iron Citadel (blocked 1 dmg this opp turn)` *(passive note)*  
- `Spl: Lucky Shot A*2`  

---

## Two Opening Turns — Worked Example

**White Turn 1**  
```
U: Sm Q@d1 pay14
M1: Mv Nd2→f3 pay5 | Rel: Overclock A*1
B: Atk Qd1→Rd7 cost19 thr80 d% 72/80 ✓ dmg1
B: Atk Nd2→Rd7 cost9 d% 33/50 ✓ dmg1 xRd7 +SP25
M2: Conv SP10→LP5
E: LP=26 SP=0 KD=0
```

**Black Turn 1**  
```
U: Brk pay20 3d6=11 ✗ | Sm R@a8 pay10
M1: Mv Bc8→g4 pay7
B: Atk Ra8→Qd8 cost13 thr65 d% 81/65 ✗
E: LP=__ SP=__ KD=0
```

---

## End‑of‑Turn Footer (optional, one‑liners)

```
Tn: LP=?, SP=?, KD=?, Caps: {P:_,N:_,B:_,R:_,Q:_}
```

Great for tournament sheets when judges need a quick audit.

---

## Printable Scoresheet (Markdown)

Copy this page and print. One **row** per player turn.

```
Game: ___________   Date: _______   Set: Core v0.5
White: __________________   Black: __________________
Relics (W): ________________________________
Relics (B): ________________________________

Turn  Side  U (SP+/Sm/Brk/Rep)           M1 (Mv/Rel/Spl)                 B (Atk lines)                                 M2 (Conv/Mv)            E (Tp/LP/SP/KD/Pass)
----  ----  -----------------------------  ------------------------------  --------------------------------------------  ----------------------  ---------------------
 1    W     _____________________________  ______________________________  ____________________________________________  ______________________  _____________________
 1    B     _____________________________  ______________________________  ____________________________________________  ______________________  _____________________
 2    W     _____________________________  ______________________________  ____________________________________________  ______________________  _____________________
 2    B     _____________________________  ______________________________  ____________________________________________  ______________________  _____________________
 3    W     _____________________________  ______________________________  ____________________________________________  ______________________  _____________________
 3    B     _____________________________  ______________________________  ____________________________________________  ______________________  _____________________
 4    W     _____________________________  ______________________________  ____________________________________________  ______________________  _____________________
 4    B     _____________________________  ______________________________  ____________________________________________  ______________________  _____________________
 5    W     _____________________________  ______________________________  ____________________________________________  ______________________  _____________________
 5    B     _____________________________  ______________________________  ____________________________________________  ______________________  _____________________
...
```

> Tip: Mark `A*` checkboxes in the margin to track activations. Circle captures. Box the **KD** total when it changes.

---

## Judge Notes (optional)

- If a dispute arises, the only numbers that must be present are **LP**, **SP**, **KD**, and **capture** annotations at the end of each turn.  
- Rolls (`d% r/t`, `3d6=__`) are **nice to have** but not mandatory unless a ruling depends on them.  
- For streamed matches, snap a photo of each completed turn row before proceeding to the next.

---

**That’s it.** This system keeps the table moving and gives you enough breadcrumbs to reconstruct pivotal turns later.
