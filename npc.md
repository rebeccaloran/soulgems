# NPC Phase — Quick Reference (Public Terrain Module)
*Use at the table. No third party required.*

**When:** After each player’s **End** phase (default 1v1).  
**Who controls:** the **non‑active player** (Opponent Operated NPC Phase — OONP).  
**Why:** Alternating control prevents self‑serving decisions and keeps flow fast.

---

## Script (Follow Exactly)

### Movement (each NPC)
1. **Target:** nearest enemy (Manhattan). Tie → enemy **highest piece value**; still tie → **d6**.  
2. **Step:** move 1 tile closer. Prefer orthogonal; if diagonal equally closer, controller chooses.  
3. **Blocked:** if no closer step exists, skip movement.

### Attack (each NPC)
1. If an enemy is in range (default 1), attack the **closest**. Tie → **highest piece value**; still tie → **d6**.  
2. **Accuracy:** standard d% rules. **Attacker value = SV** unless the NPC specifies a piece archetype (e.g., “as Bishop (3)”).  
3. **Damage:** 1 on hit unless specified. **Global caps apply** (+25% to‑hit, +2 dmg/hit).  
4. **Kings:** don’t target Kings unless **no other targets** exist in range.

**Order:** Controller chooses which NPC resolves first but must resolve **all** and follow this script.  
**Ambiguity:** Choose the option that closes distance to the nearest enemy; still unclear → **d6**.

---

## Variants
- **Two‑Window NPCs:** after **Upkeep** (move only) and after **End** (attack only).  
- **Tournament Team NPCs:** Two teams rotate an **NPC Captain** each round to run all NPC Phases by this card. Teams may **vote** on true ties; unresolved → **d6**.

---

## Public Terrain Reminder
- Features are **public**: roads, portals, shrines, bazaars, mints, bridges, outposts.  
- **Destruction:** structures/NPCs have **SV**; on destruction, attacker gains **SP = 5 × SV**; remove the feature and its aura immediately.

---

## Notation
`NPC: Guardian e5→f5; Atk f5→N d% 41/65 ✓ dmg1`
