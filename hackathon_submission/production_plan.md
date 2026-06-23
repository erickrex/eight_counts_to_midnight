# Meta Horizon Creator Competition: Game Design

## Production Plan

Author: Erick Alberto Rea

**Game Title:** Eight Counts to Midnight

---

## 1. MVP Definition

The MVP is a playable vertical slice of the core loop:

```text
Day preparation -> 3 short 8-beat dance phrases -> Dawn growth reward
```

It proves one promise: **the player prepares, turns that preparation into choreography, then sees the character and manor change.**

### MVP Acceptance Criteria

- Day choices change visible Night values.
- The player can build 3 legal 8-beat phrases.
- Illegal cards explain the problem in plain language.
- Close Invitation can be answered with Step Into Close.
- Clean, Stumble, and Perfect Connection outcomes are visible in replay.
- Dawn applies at least one lasting reward and one Ballroom change.

### Included in MVP

| System | Minimum Scope |
|---|---|
| Characters | 1 player follower and 1 partner: Alistair. |
| Location | Grand Ballroom with one before/after state. |
| Day actions | 2 choices: Train Technique and Rehearse Cards. |
| Wardrobe | 1 outfit/stat example showing fashion affects performance. |
| Night performance | 3 playable 8-beat phrases in one short Bachata loop. |
| Cards | 10-card tutorial pool, 5 active hand cards, 4 card roles. |
| Stances | Open and Close playable; Shadow appears as a scripted teaser. |
| Lead patterns | Close Invitation playable; Dark Embrace previewed for Shadow. |
| Resources | Beats, Flow, Frame, Poise, Bond, and Lumen Essence. |
| Progression | 1 card upgrade, 1 Technique bonus, 1 Bond increase, 1 Ballroom improvement. |
| Cinematic payoff | 1 clean replay, 1 Stumble variant, 1 Perfect Connection close-up. |

### Later Scope

| Feature | Why It Waits |
|---|---|
| Full wardrobe economy | The MVP only needs one outfit/stat proof. |
| Multiple songs | One loop is enough to test phrase readability. |
| Full manor roster | The Ballroom proves restoration; Mirror Hall can appear as a preview. |
| Large card catalog | Ten cards are enough to test choreography. |
| Multiple romance routes | Alistair must work first because he drives the lead system. |
| Advanced syncopation | Best after players understand Beats, Flow, Frame, and stance. |

---

## 2. Technical Dependencies

| Dependency | Why It Matters | MVP Approach |
|---|---|---|
| Phrase rules engine | Checks Beats, stance legality, Flow/Frame costs, and lead responses. | Use a small card data table and one validation function. |
| Card metadata schema (move taxonomy) | Every card needs prerequisite stance, ending stance, Beat cost, Flow, and tags so the rules engine, legality checks, and replays stay consistent. A shared schema is what lets content scale without re-engineering. | Define the schema once and fully label the 10 MVP cards. The same structure scales later to a large Bachata move library (target 500+ moves) as a content task, not a code change. |
| Card/timeline UI | Lets players read choreography on a phone. | Portrait layout with hand cards, Bar A/Bar B, modifier slots, and clear illegal-card feedback. |
| Lead-pattern validation | Makes Alistair feel like a dance partner. | Build Close Invitation first; preview Dark Embrace only as the Shadow teaser. |
| Replay layer | Turns card choices into a dance result. | Use short pose sequences for Clean, Stumble, and Perfect Connection outcomes. |
| Progression save state | Lets Day choices affect Night and Dawn. | Store Technique bonus, upgraded card, Bond, Lumen Essence, and Ballroom state. |
| Art and animation pipeline | The 3D partner dance is the highest-risk, highest-cost asset. Bachata is a connected lead/follow dance, so motion must read as real partnering, not two solo loops. | MVP uses still poses and simple movement beats for Clean, Stumble, and Perfect Connection. The production build captures real Bachata dancers with motion capture, retargets to the two characters, and polishes in Cascadeur for physics-based cleanup and secondary motion. Modular base moves plus additive Styling layers keep the combination count manageable: a focused set of mocapped Footwork, Transitions, and key dips per stance covers many card combinations without capturing every permutation. |

---

## 3. Build Sequence

| Phase | What Gets Built | What's Testable After |
|---|---|---|
| 1 | Paper/card prototype: 10 cards, 8-beat rules, Open/Close legality, Flow, Close Invitation. | A player can build a legal phrase and explain why Step Into Close solves the lead. |
| 2 | Clickable portrait UI: Day action screen, card hand, Bar A/Bar B timeline, modifier slots, illegal-card feedback, lock-in. | A player can complete the Day 2 loop: Train, Rehearse, build a phrase, lock it in. |
| 3 | Playable slice: scoring, Frame/Poise checks, Stumble, Perfect Connection, placeholder replay. | A player can feel how preparation and cards change the dance result. |
| 4 | Presentation polish: Ballroom before/after, stone-crack moment, outfit/stat example, Shadow teaser, dawn screen. | Judges can see the full promise: solo dance wakes the manor, partner dance proves connection, growth sets up tomorrow. |

Build order follows dependencies. Phrase rules come before UI polish. UI comes before animation. Replay comes before final visual polish. Shadow is saved for the presentation layer because it depends on stance, Bond, and lead readability.

---

## 4. Testing & Validation

The first-playable milestone is the Day 2 partner dance. The player starts after the Day 1 awakening, chooses two preparation actions, enters the Ballroom, sees **Close Invitation**, uses **Step Into Close**, attaches **Eye Contact**, locks the phrase, and watches a Perfect Connection replay.

### Fun Signals

- [ ] A new player builds the first legal phrase within 2 minutes.
- [ ] A new player can explain why **Step Into Close** answers **Close Invitation**.
- [ ] A new player notices the Technique or Rehearsal bonus during the Night phase.
- [ ] Players replay for a cleaner Perfect Connection.
- [ ] Players ask when they can unlock Shadow stance.

### Adjustment Signals

- [ ] For better 8-beat readability, use two larger bars and a smaller hand.
- [ ] For stronger Day action payoff, show the Technique bonus and Rehearsal upgrade inside the Night phase.
- [ ] For stronger dance feel, use clearer dance verbs and stronger replay feedback.
- [ ] For smoother Shadow onboarding, keep it as a teaser until Open/Close are clear.

## Before You Submit

This plan matches the GDD and Player Journey Map:

```text
Prepare by day. Dance by night. Grow at dawn.
```

The MVP builds the smallest version that proves the hook.
