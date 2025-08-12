SOUL GEMS — v0.5
A Tactical Chess Wargame • Full Game Guide for New Players
Comprehensive Rulebook • August 12, 2025
Created by Rebecca Loran • twitch.tv/rebeccaloran

# Welcome to Soul Gems
Imagine chess stepped into a heavier suit of armor. The board is still 8×8, the pieces still move as you remember—but the battle has grown teeth. Pieces hit, miss, bleed, and return from the void. You manage Life Points (LP) and Soul Points (SP) like a commander allocating fuel and munitions. Victory isn’t a checkmate; it’s the moment your enemy’s King finally shatters into a brand-new Gem.
This book teaches you Soul Gems from zero. It’s written like someone is sitting next to you at the table, pointing at the board, and explaining why this move matters. We’ll start simple, then zoom into the math, the momentum, and the sneaky plays that make campaigns sing.
# What is Soul Gems?
Soul Gems is a campaign-ready wargame built on chess movement. You’ll:
Spend LP/SP to move, attack, and summon pieces back from your Soul Gem.
Roll dice to resolve accuracy and special sequences.
Weigh tempo (making plays now) against economy (setting up bigger turns later).
Win by converting the enemy King (20 total damage) or—if you insist—by reaching 1000 LP.
# What You Need
Standard chess board and pieces.
Dice: two d10 (tens and ones), and three d6.
Pencil/paper for LP/SP, damage, and notes (or use the provided tracking sheet).
Two areas near the board to act as each player’s Soul Gem.
# A Quick Glossary
LP (Life Points):
Your general resource and life total. If you run out, you’re in trouble. You pay most costs from LP and/or SP.
SP (Soul Points):
Earned from captures and Soul Gem income. Fuels summons and big attacks. Can convert to LP at 2:1 (up to 20 SP per turn).
Soul Gem:
Your vault for captured pieces. It also generates SP during Upkeep.
Camp:
Your first four ranks. Summoned pieces must land here.
Distance:
The number of squares traveled along a legal move path. Knights count jumps.
# Setup (First Game)
Start with an empty board.
Each player secretly chooses a starting square for their King anywhere in their own camp (ranks 1–4 for White, 5–8 for Black). Reveal and place.
Both players begin with 20 LP and 0 SP.
Place all of your pieces in your Soul Gem area (off-board).
Grab scrap paper (or the sheet in the back) for tracking LP/SP, damage, and notes.
That’s it. Your army is off-board, your King is exposed, and your economy is a spark waiting to catch.
# Turn Structure (The Pulse of a Round)
Each of your turns follows the same rhythm:
Upkeep — gain SP from your Soul Gem, handle Gem break/repair, optionally Summon a piece.
Main Phase 1 — move and/or activate abilities (max 2 activations per turn; passive stuff doesn’t count).
Battle Phase — declare attacks, pay costs, roll to hit, resolve damage/captures.
Main Phase 2 — optional second round of movement; convert SP→LP (2 SP → 1 LP, up to 20 SP/turn).
End — clear any partial damage you dealt this turn. If you took no actions at all, gain +6 LP (Pass).
# Movement (Paying for Position)
To move a piece, pay:
Move Cost = piece value + distance
Examples:
A Rook (5) moves 3 squares → 5 + 3 = 8
A Queen (9) shifts 2 squares → 9 + 2 = 11
A Knight uses jumps: up to 2 jumps per Move action at 3 LP per jump (so 3–6 LP).
Why it matters: position fuels threats. Spending now to set up a line next turn is often worth more than a small pass bonus.
# Summoning & Teleport (Reinforcements Matter)
Summon (Upkeep only):
Take a piece from your Soul Gem and place it on one of its starting squares if free. Cost: piece value + 5.
Extended placement:
Pay extra (|Δx| + |Δy|) to place farther—still within your camp. Example: White summons a Queen to d1 for 14 (9+5). To place on h3 instead, add |h−d|=4 + |3−1|=2 = 6 → total 20.
Teleport (End only):
Same cost/limits as Summon, but it targets a piece already on the board. Use it to wrench a piece out of danger or spring a surprise line.
# Combat (How Hits Happen)
Attack Cost = 2 × (attacker’s piece value) + distance
This is the **original** cost from early versions and it stays. It makes big pieces hit hard but expensive, and keeps volleys deliberate.
Accuracy (d100):
Roll two d10 (first is tens, second is ones). A result of 00 counts as 100. You **hit** if:
d100 ≤ clamp(5, 20 + 10 × (AttackerValue − DefenderValue), 95)
Damage:
Each hit deals 1 damage. When the total damage you dealt this turn to a target ≥ its piece value, you capture it and put it in your Soul Gem (damage clears at the end of **your** turn).
Capture Reward:
Gain SP = 5 × captured piece value. That SP is your fuel for future turns.
# The King (Boss Fight Rules)
The King has 20 HP and is not captured via piece-value thresholds.
To hit the King:
d100 ≤ 10 × (attacker’s piece value) (still clamped to 5%–95%)
When the King has taken 20 total damage, it’s converted. That’s game.
# Limits That Keep Things Fair
Max +25% total to-hit bonus on any attack.
Max +2 damage per hit after all effects.
Max **one** reroll/advantage effect per attack.
Max **2** ability activations per turn (passive effects don’t count).
# Soul Gems & Economy (Why Captures Matter)
Your Soul Gem stores captured pieces and powers your economy.
SP income: At each Upkeep, sum the values of pieces in your Gem and multiply by 2. Gain that much SP. (No SP on your first turn.)
Break (your Upkeep): Pay 20, roll 3d6; success on 12+. If broken, your opponent can’t gain SP or Summon until repaired. Any of *your* pieces they had captured return to **your** Gem.
Repair (your Upkeep): Pay 10, roll 3d6; success on 10+.
No repair lock: You can’t deny repairs two turns in a row with denial effects.
Pass bonus: If you truly do nothing in your turn, gain +6 LP at End.
# Accuracy Intuition (Reading the Odds)
You don’t need to memorize tables, but this helps your gut:
If your attacker’s value equals the defender’s, your base hit threshold is about **20%**.
Every point of piece-value advantage adds about **+10%** to-hit (before caps).
Queen (9) shooting a Pawn (1) is effectively capped—you’ll be near the 95% ceiling.
Against the King: a Queen hits at **90%** base; a Rook hits at **50%** base; a Knight at **30%**.
# Worked Examples (Step by Step)
Example A — Capturing a Pawn with a Rook
You have a Rook (5) two squares away from an enemy Pawn (1). Attack cost is 2×5 + 2 = 12. Accuracy threshold: 20 + 10×(5−1) = 60%. Roll the d100; on 60 or less, you hit for 1 damage—enough to capture the Pawn (1 HP). Gain 5 SP.
Example B — Softening a Rook
Your Queen (9) is three squares from an enemy Rook (5). Attack cost: 2×9 + 3 = 21. Accuracy threshold: 20 + 10×(9−5) = 60%. A hit deals 1 damage. You’ll need multiple hits **this turn** (or a damage-boosting ability) to capture since the Rook is 5 HP.
Example C — Hitting the King
Your Rook (5) is within 2 squares. Attack cost: 2×5 + 2 = 12. Versus King, threshold is 10×5 = 50% (clamped). Each hit deals 1 damage toward the 20 total you need.
# Your First Match — A Guided Walkthrough
We’ll play a short, illustrative intro. Don’t worry about perfect moves; focus on flow and costs.
Turn 1 — White
Upkeep: No SP yet. Summon a Rook (5+5=10). LP 20→10. Move: Rook 2 squares (5+2=7). LP 10→3. End: no damage to clear.
Turn 1 — Black
Upkeep: No SP. Summon a Queen (9+5=14). LP 20→6. Holds position to bank resources. End: —
Turn 2 — White
Upkeep: Still no SP. Not enough LP to attack meaningfully. **Pass** → +6 LP (LP 3→9).
Turn 2 — Black
Upkeep: —  Main 1: Queen advances 2 squares (9+2=11). LP 6→(can’t pay) → chooses **Pass** → +6 LP (LP 6→12).
Turn 3 — White
Upkeep: —  Battle: Rook fires at a Pawn two squares away. Cost 12; threshold 60%. Roll 41 → **hit**, capture Pawn → gain 5 SP. End: damage clears (none lingering).
Turn 3 — Black
Upkeep: Gem has 1 captured Pawn value = 1, SP income = 2×1 = 2 SP. With 2 SP in hand and 12 LP, Black can fund a Queen shot next turn—or Summon a Knight for board presence.
Notice how the economy snowballs: small captures create SP which fund the next threat. Gem Breaks are powerful but expensive—save for a moment the opponent just spent big.
# Training Scenarios & Drills
Play these before your first campaign. They each teach a muscle you’ll use later.
Drill 1 — Last-Hit Practice
Set an enemy Pawn, Knight, and Rook at safe distances. Practice calculating costs and thresholds, then try to last-hit (capture) in one turn with minimal spend.
Drill 2 — Summon Timing
Start with 20 LP, 0 SP. Try three openings: (a) immediate Queen Summon; (b) double minor pieces; (c) Pass into Summon. Note how your next turn options change.
Scenario — Gem Siege Mini-Game
Each player starts with 10 SP and one Rook in Gem. First player to **successfully Break** the enemy Gem **and** capture any piece wins. Teaches resource denial tempo.
# Strategy — How to Think in Soul Gems
Target Selection:
Early on, farm low-value pieces for SP unless a clean hit on a major piece presents itself.
Tempo vs Economy:
A strong **Pass** (+6 LP) is often better than a weak attack. Bank for turns that matter.
King Pressure:
Queens hit Kings at ~90%. A single Queen volley won’t end it, but steady pressure forces bad trades.
Distance Discipline:
Every square of distance costs real LP. Teleport and Summon placement can save entire attacks’ worth of budget.
Gem Warfare:
Breaking the Gem is a fast lane to victory—time it after the opponent spends big and can’t immediately repair.
# Common Pitfalls (And How to Dodge Them)
Attacking without a plan to finish: damage clears at end of your turn. If you can’t cross the capture threshold, consider passing.
Ignoring Pawns: 5 SP per pawn capture is serious money early.
Over-summoning Queens: a turn-1 Queen Summon is flashy, but it might leave you broke and predictable.
Forgetting conversion caps: 2 SP → 1 LP, up to 20 SP per turn. Plan two turns ahead.
# Optional Module (Preview) — Relics & Spells
In the next version, we’ll introduce a Dominion-style layer with **Relics** (unique permanent abilities you draft) and **Spells** (single-use tactics you can buy mid-game). The core math stays the same—but the draft becomes high-stakes. See `relic_spells.md` if your group wants to experiment.
# Quick Reference
Move = piece value + distance
Attack = 2×piece value + distance
Hit if d100 ≤ clamp(5, 20 + 10×(Atk − Def), 95)
Capture reward = 5 × piece value (SP)
Summon (Upkeep) = piece value + 5 (within your camp; can pay extra (|Δx|+|Δy|) for farther)
Teleport (End) = as Summon, but for a piece already on the board
Break = Pay 20; 3d6 ≥ 12 • Repair = Pay 10; 3d6 ≥ 10
Pass = +6 LP (only if you took no actions that turn)
Win = enemy King takes 20 damage (or reach 1000 LP)
# Turn Tracker (Photocopy This Page)

Design & Rules © Rebecca Loran. This guide was written to make Soul Gems accessible without sacrificing its depth. Stream your campaigns, write your legends, and send feedback.

## Relic Spells Drafting Rules (v0.5)

Relic Spells add a powerful and strategic layer to Soul Gems. They are drafted before the game begins and can be used at specific times during play. Relic Spells fall into two main categories:

- **Permanent Relics** — These are placed in front of you after being played and remain active for the rest of the game, continuously affecting gameplay.
- **Instant Spells** — These are one-time effects, played instantly when conditions are met or during an allowed phase, then discarded.

### Drafting Procedure

1. **Setup the Relic Spell Deck**  
   Shuffle all Relic Spell cards together into a single deck.

2. **Initial Draft**  
   At the start of the game, before placing Kings, each player draws **5 Relic Spell cards** from the deck.

3. **Selection**  
   From these 5, each player chooses **3 cards** to keep. The other 2 are returned to the deck and reshuffled.

4. **Secrecy**  
   Players may keep their chosen Relic Spells hidden until they are played.

5. **Hand Limit**  
   Players may hold a maximum of **3 Relic Spells** in their hand at any given time. If a player would gain another, they must immediately discard one.

### Playing Relic Spells

- Instant Spells are played **during the phase specified** on the card (e.g., Upkeep, Main Phase, Battle Phase, End Phase).
- Permanent Relics are played during your Main Phase unless otherwise stated. Place them in your Relic Zone where both players can see them.
- Some cards may have SP (Soul Points) or LP (Life Points) costs; these must be paid before playing the card.
- Relic Spells **cannot** be used to directly capture the King, but they may indirectly affect conditions for capture.

### Example Relic Spell Uses

- **Soul Ward** *(Permanent Relic)*: Reduces all incoming damage to your King by 2.  
- **Temporal Rift** *(Instant Spell)*: Immediately take an extra Movement Phase after this one.  
- **Soul Drain** *(Instant Spell)*: Steal 5 SP from your opponent’s Soul Gem total.

### Optional Draft Variants

- **Open Draft** — Players draft with all cards visible, adding a layer of mind games.
- **Double Draft** — Players draw 8 cards and keep 4, returning the others to the deck.

---


## Example Game: Full Turn Walkthrough with Relic Spells Draft

### Pre-Game Setup
- Both players set up the board in standard chess layout.
- Players shuffle the Relic Spells deck (combining both Permanent Relics and Instant Spells).
- Each player draws **5 Relic Spell cards**.
- Player A chooses **Soul Ward** (Permanent Relic), **Temporal Rift** (Instant Spell), and **Soul Drain** (Instant Spell).
- Player B chooses **Mirror Barrier** (Permanent Relic), **Arcane Surge** (Instant Spell), and **Spirit Exchange** (Instant Spell).
- The remaining cards are shuffled back into the deck.
- Players keep their chosen cards hidden in hand unless they are Permanent Relics in play.

### Turn 1: Player A
- **Upkeep Phase**: No effects yet.
- **Main Phase**: Player A deploys Soul Ward (Permanent Relic), protecting their King with -2 damage reduction.
- **Movement Phase**: Moves a pawn forward two spaces.
- **Battle Phase**: No attacks possible this early.
- **End Phase**: Pass turn.

### Turn 1: Player B
- **Upkeep Phase**: No effects yet.
- **Main Phase**: Player B keeps all Relics in hand for later strategic use.
- **Movement Phase**: Moves a knight into a forward position.
- **Battle Phase**: No valid attacks yet.
- **End Phase**: Pass turn.

### Mid-Game Interaction
- On Turn 5, Player B moves a rook into range of Player A’s bishop and plays **Arcane Surge** to increase damage output for one attack.
- Player A responds by playing **Temporal Rift**, taking an extra Movement Phase to reposition their bishop out of range before the attack resolves.

### Late Game
- Player A uses **Soul Drain** to steal SP from Player B, then spends those SP on a high-cost coordinated attack to capture Player B’s queen.
- Permanent Relics remain in play to the end, shaping both offensive and defensive tactics.

---
