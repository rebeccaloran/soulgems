# Soul Gems — Notation (v0.2)
Human-first logging for Core v0.5 + Relics + Field/Terrain + NPCs. This version adds **Adjournment & Resumption** so long games can pause and resume perfectly.

> General format: **one event per line**. Use short, fixed tokens; prefer clarity over brevity. Coordinates are algebraic (a1–h8; expand if using larger maps). All numbers are integers unless noted.

---

## 0) Session Header (required at game start)
```
GAME: <match_id> | DATE: <YYYY-MM-DD> | SESSION: <n>
PLAYERS: White=<handle1> Black=<handle2>
FORMAT: <Core | Core+Relics | +Field | +NPC | Campaign:Name>
MAP: <8x8 | 10x10 | 12x12 | 16x16 | customNxM>
SEED: <rng-seed-or-NA>   ; optional, for simulator parity
RULES: MoveCap=<NA|N> ; SessionLimit=4h ; Adjournment=ON
```
**Example**
```
GAME: SG-2025-0812-Alpha | DATE: 2025-08-12 | SESSION: 1
PLAYERS: White=Raven Black=Echo
FORMAT: Core+Relics+Field+NPC
MAP: 10x10
SEED: NA
RULES: MoveCap=NA ; SessionLimit=4h ; Adjournment=ON
```

---

## 1) State Blocks (snapshots)
State blocks are **machine-readable** snapshots. Log one **at the start of the game**, one **at adjournment**, and one **at resumption** (to confirm).

### 1.1 Board/Pools/Phase
```
STATE:
 TURN: <full-move-number> ; SIDE: <W|B> ; PHASE: <Start|Upkeep|M1|Battle|M2|End|NPC>
 LP: W=<int> B=<int> ; SP: W=<int> B=<int>
 KINGDMG: W=<int> B=<int>
 GEM: W=<int:0=ok,1=broken> B=<int>
 BAZAAR_USED_THIS_TURN: <0|1>
 WEATHER: <Clear|Fog|Rain|Snow|Storm> ; ROUNDS_LEFT=<int>
 CAPS_USED_THIS_TURN: tohit=<0-25> dmg=<0-2> rerolls=<0-1> acts_used=<0-2>
```

### 1.2 Pieces in Play & Gems
```
PIECES_ON_BOARD:
 W: P=<n> N=<n> B=<n> R=<n> Q=<n>
 B: P=<n> N=<n> B=<n> R=<n> Q=<n>

SOUL_GEMS:
 W: P=<n> N=<n> B=<n> R=<n> Q=<n>
 B: P=<n> N=<n> B=<n> R=<n> Q=<n>

CAPTURED_BY:
 W: P=<n> N=<n> B=<n> R=<n> Q=<n>
 B: P=<n> N=<n> B=<n> R=<n> Q=<n>
```

### 1.3 Terrain & Structures (public)
Assign **IDs** so you can reference them later.
```
TERRAIN:
 ROAD: id=R1..Rk ; SEGMENTS=<count> ; COORDS=[c5,c6,...]
 BRIDGE: id=BR1.. ; COORD=<e4>
 PORTAL: id=PA ; A=<b6> B=<h6>
 OUTPOST: id=O1.. ; COORD=<d5> ; SV=3
 SHRINE: id=S1.. ; COORD=<f3> ; MODE=<ACC|DMG> ; SV=3
 BAZAAR: id=BZ1.. ; COORD=<e4> ; SV=5
 MINT: id=MI1.. ; COORD=<b2> ; SV=4
 WEATHER_NODE: id=W1.. ; COORD=<g7> ; SV=4
 WALL: id=WL1.. ; PATH=[d4,d5,d6]
 NOTE: All terrain is PUBLIC. SV used for attacks/destruction. 
```

### 1.4 NPCs (public)
```
NPCS:
 GUARDIAN: id=G1.. ; AT=<e5> ; SV=4 ; STATUS=<OK|DMG:n|Removed>
 TRADER: id=T1.. ; AT=<f7> ; SV=3 ; STATUS=<OK|Removed>
 BEAST: id=BE1.. ; AT=<c3> ; SV=2 ; STATUS=<OK|Removed>
```

### 1.5 Relics & One-Shots
```
RELICS:
 W: PERMS=[<RelicA>,<RelicB>,...] ; INSTANTS_USED=[<CardX>@turn, ...]
 B: PERMS=[...] ; INSTANTS_USED=[...]

TURN_FLAGS:
 W: shrine_acc_used=<0|1> shrine_dmg_used=<0|1> outpost_used=<0|1>
 B: shrine_acc_used=<0|1> shrine_dmg_used=<0|1> outpost_used=<0|1>
```

---

## 2) Action Lines (per event)
Use these during play. One action per line.

### 2.1 Phases & Pass
```
PHASE: <Start|Upkeep|M1|Battle|M2|End|NPC>
PASS
```

### 2.2 Summon / Teleport / Move
```
SUMMON: <W|B> <piece> @<target> pay(<LP,SP>)
TELEPORT: <W|B> <piece> <from>→<to> pay(<LP,SP>) src=<PortalID>
MOVE: <W|B> <piece> <from>→<to> cost=<n>  notes=[Road|Outpost|Shrine|Portal]
```

### 2.3 Attacks & Captures
```
ATTACK: <W|B> <piece> <from>⇒<targetPiece|SV> @<sq|objID> cost=<n> thr=<%> roll=<d%> hit=<Y|N> dmg=<n> mods=[ACC+10|DMG+1|Lucky|Reaper|IronBlock1]
CAPTURE: <W|B> <targetPiece|SV> @<sq|objID> gainSP=<n>
KINGDMG: <W|B> dmg=<n> total=<n>
```

### 2.4 Field Builds (M2 only)
```
BUILD: <feature> id=<ID> @<coord(s)> pay(<LP,SP>) SV=<n> details=<mode|path|pair>
```

### 2.5 Weather Toggles
```
WEATHER: <Clear|Fog|Rain|Snow|Storm> rounds=<n> src=<W1>
```

### 2.6 NPC Phase (opponent-operated)
```
NPC: <id> <from>→<to>
NPC_ATK: <id> ⇒ <piece> @<sq> roll=<d%> hit=<Y|N> dmg=<n>
```

### 2.7 Gem Operations
```
GEM_BREAK_ATTEMPT: <W|B> pay(<LP,SP>) roll=3d6(<a+b+c>) mod=<+/-n> result=<Success|Fail>
GEM_REPAIR_ATTEMPT: <W|B> pay(<LP,SP>) roll=3d6(<a+b+c>) mod=<+/-n> result=<Success|Fail>
GEM_STATUS: W=<OK|BROKEN> B=<OK|BROKEN>
```

### 2.8 Conversions
```
CONVERT: <W|B> SP→LP amount=<nSP> gain=<nLP> [via=Mint]
```

---

## 3) Adjournment & Resumption

### 3.1 Declaring Adjournment
At the **end of the current phase**, add:
```
ADJOURN: REASON=<SessionLimit|Mutual|Director> TIME=<HH:MM local>
```
Immediately follow with a **STATE snapshot** (Sections 1.1–1.5). Both players confirm:
```
SIGNOFF: W=<sig> B=<sig>  ; method=<digital|paper>
```

### 3.2 Resuming Play
Start the next session with:
```
RESUME: DATE=<YYYY-MM-DD> SESSION=<n+1> TIME=<HH:MM>
```
Then paste the **last agreed STATE** and **confirm**:
```
STATE_CONFIRMED: W=<Y> B=<Y>
```

If any corrections are needed (e.g., a misplaced token), log a delta:
```
STATE_PATCH: desc="Correct S1 mode to ACC" AUTH: Judge=<name> W=<OK> B=<OK>
```

### 3.3 Integrity & Disputes
- If signatures differ, mark:
```
DISPUTE: field=<section.key> desc="<short text>"  AUTH: Judge=<name>
```
- Continue only after a **STATE_PATCH** is recorded.

---

## 4) Examples

### 4.1 Midgame with Weather & NPC
```
PHASE: M2
BUILD: SHRINE id=S2 @f3 pay(6,4) SV=3 details=ACC
END
NPC: G1 e5→f5
NPC_ATK: G1 ⇒ N @f5 roll=41 hit=Y dmg=1
```

### 4.2 Gem Operations & Adjournment
```
PHASE: Upkeep
GEM_BREAK_ATTEMPT: W pay(12,8) roll=3d6(5+4+6) mod=+1 result=Success
GEM_STATUS: W=OK B=BROKEN
PHASE: End
ADJOURN: REASON=SessionLimit TIME=03:59
STATE:
 TURN: 24 ; SIDE: W ; PHASE: End
 LP: W=14 B=9 ; SP: W=6 B=2
 KINGDMG: W=3 B=7
 GEM: W=0 B=1
 BAZAAR_USED_THIS_TURN: 1
 WEATHER: Fog ; ROUNDS_LEFT=1
 CAPS_USED_THIS_TURN: tohit=10 dmg=1 rerolls=1 acts_used=2
PIECES_ON_BOARD:
 W: P=5 N=2 B=1 R=1 Q=0
 B: P=6 N=1 B=2 R=1 Q=1
SOUL_GEMS:
 W: P=3 N=0 B=1 R=1 Q=1
 B: P=2 N=1 B=0 R=1 Q=0
CAPTURED_BY:
 W: P=2 N=1 B=0 R=0 Q=0
 B: P=1 N=0 B=1 R=0 Q=1
TERRAIN:
 ROAD: id=R1 ; SEGMENTS=6 ; COORDS=[c4,c5,c6,d6,e6,f6]
 PORTAL: id=PA ; A=b6 B=h6
 SHRINE: id=S1 ; COORD=e4 ; MODE=DMG ; SV=3
 OUTPOST: id=O1 ; COORD=d5 ; SV=3
NPCS:
 GUARDIAN: id=G1 ; AT=f5 ; SV=4 ; STATUS=OK
RELICS:
 W: PERMS=[CoordinatedDoctrine,StatisticalAim] ; INSTANTS_USED=[LuckyShot@21]
 B: PERMS=[GemMasonry,IronCitadel] ; INSTANTS_USED=[]
TURN_FLAGS:
 W: shrine_acc_used=1 shrine_dmg_used=0 outpost_used=1
 B: shrine_acc_used=0 shrine_dmg_used=1 outpost_used=0
SIGNOFF: W=/s Raven B=/s Echo  ; method=digital
```

---

## 5) Tips
- Keep **STATE** blocks aligned; they’re your save-files.
- Use **IDs** for any object you might change or destroy later.
- For big maps, keep a **legend** at the top: tile symbols, portal labels, wall paths.

---

**File version:** notation v0.2 (Adjournment).  Authors: Rebecca Loran & collaborators.
