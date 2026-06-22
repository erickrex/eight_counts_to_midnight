# Meta Horizon Creator Competition: Game Design

## Production Plan

**Game Title:** Dancing with Dracula: Crimson Manor

---

## 1. MVP Definition

The MVP is a playable vertical slice of the core loop:

```text
Day preparation -> 3 short 8-beat dance phrases -> Dawn growth reward
```

It proves the central promise of the game: **the player manages preparation, turns that preparation into choreography, then sees the character and manor change because of the dance.**

### Included in MVP

| System | Minimum Scope |
|---|---|
| Characters | 1 player follower and 1 partner: Alistair. |
| Location | Grand Ballroom only, with one before/after restoration state. |
| Day actions | 2 choices: Train Technique and Rehearse Cards. |
| Wardrobe | 1 visible outfit/stat example to prove fashion affects performance. |
| Night performance | 3 playable 8-beat phrases in one short Bachata loop. |
| Cards | 10-card tutorial pool, 5 active hand cards, 4 card roles: Footwork, Transition, Styling, Support. |
| Stances | Open and Close fully playable; Shadow appears as one scripted teaser/payoff after Bond is introduced. |
| Lead patterns | Close Invitation as the main playable lead; Dark Embrace as a late-slice Shadow preview. |
| Resources | Beats, Flow, Frame, Poise, Bond, and Lumen Essence. |
| Progression | 1 card rehearsal upgrade, 1 Technique bonus, 1 Bond increase, 1 visible Ballroom improvement. |
| Cinematic payoff | 1 clean phrase replay, 1 Stumble variant, 1 Perfect Connection close-up. |

### Cut From MVP

| Cut Feature | Why It Waits |
|---|---|
| Full wardrobe economy | Needs more art and balancing; MVP only needs one visible outfit/stat example. |
| Multiple songs | One short loop is enough to test 8-beat phrase readability. |
| Full manor roster | The Ballroom proves restoration; Mirror Hall can appear as an unlock preview. |
| Large card catalog | Ten cards are enough to test deck-construction as choreography. |
| Multiple romance routes | Alistair must work first because he is the lead-pattern system. |
| Advanced syncopation | Adds complexity after players understand Beats, Flow, Frame, and stance. |
| Full monetization | Not needed to prove the design. |

The MVP is intentionally small. If this slice works, a player understands the fantasy, the management loop, the dance-card mechanic, and why they would return tomorrow.

---

## 2. Build Sequence

| Phase | What Gets Built | What's Testable After |
|---|---|---|
| 1 | Paper/card prototype: 10-card pool, 8-beat phrase rules, Open/Close stance legality, Flow generation/spend, Close Invitation lead. | A player can build a legal phrase on paper and explain why Step Into Close solves Alistair's lead. |
| 2 | Clickable portrait UI: Day action screen, card hand, Bar A/Bar B timeline, modifier slots, illegal-card feedback, phrase lock-in. | A player can complete the Day 2 loop without help: Train Technique, Rehearse Cards, build a phrase, lock it in. |
| 3 | Playable vertical slice: scoring, Frame/Poise checks, Stumble state, Perfect Connection, one short cinematic replay using placeholder animation. | A player can feel the cause/effect between preparation, card choices, and the dance result. |
| 4 | Presentation polish: Ballroom before/after, Alistair stone-crack moment, one outfit/stat example, Shadow teaser, final dawn reward screen. | Judges can see the complete promise: solo dance wakes the manor, partner dance proves connection, growth sets up tomorrow. |

Build order follows dependencies. The phrase rules come before UI polish. The UI comes before animation. The cinematic replay comes before full visual polish. Shadow is saved for the presentation layer because it depends on players already understanding stance, Bond, and Alistair's lead.

---

## 3. Testing & Validation

The first-playable milestone is the Day 2 partner dance. A player starts after the Day 1 awakening, sees Alistair awake but guarded, chooses two preparation actions, then enters the Ballroom. Alistair presents **Close Invitation**. The player uses a rehearsed card and **Step Into Close** to enter Close before Beat 5, attaches **Eye Contact**, locks the phrase, and sees a Perfect Connection replay.

### What "This Is Fun" Looks Like

- [ ] Players describe the game as "I am building a dance," not "I am playing random cards."
- [ ] Players understand that Day choices changed the Night result.
- [ ] Players voluntarily replay the phrase to get a cleaner Perfect Connection.
- [ ] Players notice the Ballroom restoration and understand that the dance changed the manor.
- [ ] Players ask what Shadow stance does or when they can unlock more vampire choreography.

### What Would Make Us Change Direction

- [ ] If players cannot understand the 8-beat phrase, simplify the UI to two larger bars and reduce hand size.
- [ ] If players ignore Day actions, make the Technique bonus and Rehearsal upgrade visible directly inside the Night phase.
- [ ] If the card play feels abstract, rename/reframe cards around clearer dance verbs and show stronger replay feedback.
- [ ] If Shadow feels confusing, keep it as a visual teaser only and delay playable Shadow until after Open/Close mastery.

## Before You Submit

This plan matches the GDD scope: Simulation & Management first, with deck-construction expressed as choreography. It also matches the Player Journey Map: Day 1 solo dance cracks the stone, Day 2 preparation leads into the first partner dance, and the first growth reward points toward tomorrow.

The MVP does not try to build the whole game. It builds the smallest version that can prove the hook:

```text
Prepare by day. Dance by night. Grow at dawn.
```
