
# Soul Gems — Development Notes (v0.5)

**Created by Rebecca Loran**  
Original v0.2 Date: 2021-05-11  
Current v0.5 Revision: 2025-08-12  
twitch.tv/rebeccaloran

---

## Overview

Version 0.5 incorporates changes from the recent full playtest, rules refinements, and targeted adjustments aimed at balancing strategic depth with pacing. These notes are for internal development use and intended to guide further refinement.

---

## Major Changes from v0.2

1. **Draft Start Mechanic (Inspired by Dominion)**  
   - At the start of the game, instead of beginning with fixed armies, players **draft** their initial units from a shared pool.  
   - Draft order alternates, starting with the player who wins the opening roll.  
   - Each drafted piece goes into that player's Soul Gem (except the King, which is placed as per setup rules).  
   - Draft continues until both players have the agreed-upon number of pieces in their Soul Gem.

2. **Attack Cost Retained from v0.2**  
   - Original attack formula `[2(piece value) + (distance)]` remains intact.  
   - This decision was made to preserve the high cost of aggressive play while rewarding calculated strikes.

3. **Soul Gem Interaction Adjustments**  
   - Breaking a Soul Gem now has clearer cost calculation, ensuring the "[(captured piece value) - (your captures) + 20]" formula is explicit and consistently applied.  
   - Repair and SP → LP conversion remain unchanged but will be a focus in the next test for potential tuning.

4. **Pass Mechanic Clarification**  
   - Passing for LP is now explicitly tied to the *on-board* value of your army minus enemy captures, with a **minimum gain of 10 LP**.

5. **Summoning and Teleporting Clarifications**  
   - Summon placement cost calculations clarified with stepwise examples.  
   - Teleport is unchanged mechanically but now explicitly states it can only be done in End Phase.

---

## Playtest Observations (Full Game — v0.5)

### Strengths
- **Draft start** created immediate strategic engagement and replayability.
- Attack costs remain a strong balancing factor, preventing reckless trades.
- Soul Gem mechanics continue to feel unique compared to other chess variants.

### Weaknesses / Bottlenecks
- **Game length**: A full game ran longer than expected (2–3 hours).  
- **SP→LP Conversion**: Rarely used due to opportunity cost vs. other actions.
- **Breaking Soul Gems**: Players often avoided targeting Gems due to perceived high investment, even when strategically viable.

### Notable Player Strategies
- One player focused entirely on summoning mid-value pieces quickly to overwhelm early.  
- Another player turtled, passing for LP to build a massive economy before striking.

---

## Suggestions for Future Tests

### High Priority
1. **Test variable attack costs** for pawns/knights to speed up skirmishes.  
2. **Evaluate reduced break cost** for Soul Gems to encourage targeted aggression.  
3. **Introduce an optional mid-game event** (e.g., neutral piece or objective) to break stalemates.

### Medium Priority
1. **Ability card prototype** — Implement 3–5 one-use abilities obtainable by fulfilling board conditions.  
2. **Crypt mechanic prototype** — A second storage area for “banished” souls that require special actions to retrieve.

---

## Next Playtest Scenarios
1. **Fast Draft Variant**: Reduce initial Soul Gem piece count to 5 each.  
2. **Aggro Economy**: Reduce LP gain from passing to 5 minimum and see if aggression increases.  
3. **Gem Break Incentive**: Award LP when successfully breaking opponent's Gem.

---

**End of Notes**  
Future updates will include finalized ability card rules and the Crypt mechanic.
