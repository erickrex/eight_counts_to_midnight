# Extended Game Loop: Lead & Follow System

Alistair should not have a normal "enemy turn." He should have an **Intent / Lead system**.

Think of each turn as this:

> **Alistair leads. The player follows.**

Alistair's "move" is shown as a telegraphed dance invitation *before* the player commits their 8-beat phrase. The player is not guessing randomly. She is reading his body language, the music, and the relationship cues. Mechanically, that appears as a visible **Alistair's Lead** panel.

This document describes the complete loop using canon rules: persistent deck, 20-card active deck later, each night as a performance, each performance made of 8-beat phrases, no roguelike reset, and failure causing stumbles/Poise loss/reduced rewards rather than permadeath.

---

## Core Idea

A short session is:

```
Day prep
→ Night performance: 3 phrases
   → Phrase 1: 8 beats
   → Phrase 2: 8 beats
   → Phrase 3: 8 beats
→ Dawn rewards
```

A phrase is your "turn."

Each turn is **not**:

```
Player turn → Enemy turn → Player turn → Enemy turn
```

It **is**:

```
Alistair reveals his lead intention
→ Player builds an 8-beat response
→ Game checks rhythm, stance, Flow, Frame, and connection
→ Cinematic dance replay
```

So Alistair does act, but not by playing cards after you. He acts by setting the dance pressure for the phrase.

---

## What Alistair Does

Alistair is the **Lead Intent** system.

At the start of each 8-beat phrase, he reveals something like:

```
ALISTAIR'S LEAD: Close Invitation
Timing: Beats 5-8
Reward: Perfect Connection x2 if you enter Close by Beat 5
Miss: Lose multiplier, no Bond bonus
```

or:

```
ALISTAIR'S LEAD: Sudden Dip
Timing: Beat 7
Requirement: Close stance + 3 Frame by Beat 7
Success: Cinematic Dip, big score, Bond bonus
Failure: Stumble, lose Poise
```

He does not need a separate turn because partner dance already has a natural structure:

1. Leader gives intention.
2. Follower responds.
3. Connection is judged.

The gameplay is about whether the player reads him correctly and chooses cards that make her response safe, beautiful, and musically correct.

---

## How We Know Alistair's Intentions

This should be shown through three layers.

### 1. UI Telegraph

The player sees an "Alistair's Lead" card near the timeline.

```
┌─────────────────────────────────┐
│       ALISTAIR'S LEAD           │
│                                 │
│       Close Invitation          │
│         Beats 5-8               │
│                                 │
│ He draws you inward during      │
│ the second bar.                 │
│                                 │
│ Success: +2 Bond, x2 Multiplier │
│ Miss: No Connection bonus       │
└─────────────────────────────────┘
```

This makes the tactical objective clear.

### 2. Body-Language Animation

Alistair's model gives a visual cue:

| Lead | Animation Cue |
|------|---------------|
| Open Invitation | He keeps distance, offering one hand |
| Close Invitation | His hand moves toward her back |
| Sudden Dip | He lowers his center of gravity and opens space |
| Wrap Exit | His arm angle shifts as if preparing to unwind her |
| Sensual Phrase | He slows, closes distance, and waits for expressive movement |

So even without reading the text, the player starts to learn his cues.

### 3. Relationship Progression

**Early game (low Bond):**
> *"Alistair wants to draw closer soon."*

**Mid game (higher Bond):**
> *"Close Invitation — Enter Close before Beat 5."*

**Late game (high Bond):**
> *"Close Invitation, Beats 5-8. Close-stanced Styling cards gain +25%."*

That makes romance mechanically meaningful. The more she knows him, the better she reads his lead.

---

## Design Note: Rename Player Cards

Because Alistair is the leader, some card names could confuse the fantasy.

| Instead of... | Use... |
|---------------|--------|
| Cross Body Lead | Follow Cross-Body |
| Inside Turn | Follow Inside Turn |

The player is still making decisions, but fictionally she is choosing how to respond, not taking over the leader role.

---

## Resources During a Phrase

Each phrase has four important values:

| Resource | What It Means | Carries Between Phrases? |
|----------|---------------|--------------------------|
| **Beats** | The 8-count timing budget | No; each phrase is exactly 8 beats |
| **Flow** | Momentum/confidence for expressive cards | Usually no |
| **Frame** | Posture/support/trust for difficult moves | Usually no |
| **Poise** | Nightly mistake buffer | **Yes**, across the whole performance |

**The key distinction:**
- Beats = time
- Flow = momentum
- Frame = safety/support
- Poise = how many mistakes the night can survive

---

## Card Roles

The player builds each 8-beat phrase from cards.

| Card Type | Uses Beats? | Uses Flow? | Purpose |
|-----------|-------------|------------|---------|
| **Footwork** | Yes | Usually no | Main movement, creates rhythm, generates Flow |
| **Transition** | Yes | Usually no | Changes stance: Open, Close, Wrap |
| **Styling** | No | Yes | Adds beauty, score, hair/hip/arm/body expression |
| **Support** | No | Yes | Builds Frame, stabilizes difficult leads, gains Bond |

A clean phrase usually looks like this:
- Base movement cards fill 8 beats
- Styling and Support cards attach on top

So the player is not trying to cram 10 cards into the timeline. The timeline remains readable.

---

## Complete Session Example

Let's walk through a complete short session.

### Day Prep Before the Session

The player chooses **2 Day Actions**:

**Day Action 1: Mirror Hall Training**
- Effect: +1 Starting Frame on the first phrase

**Day Action 2: Wardrobe Atelier**
- Equip outfit: Crimson Waltz
- Effect: +1 Starting Flow each phrase

She enters the ballroom with:

| Stat | Value |
|------|-------|
| Poise | 10 |
| Starting stance | Open |
| Active deck | 20 cards |
| Hand size | 5 |
| Performance length | 3 phrases |

Tonight's song:

```
La Noche en el Manor
Difficulty: Beginner
Length: 3 phrases
```

Now the night begins.

---

## Phrase 1 — "Establish the Rhythm"

### Start of Phrase

| Stat | Value |
|------|-------|
| Phrase | 1 / 3 |
| Beats | 0 / 8 |
| Stance | Open |
| Flow | 1 |
| Frame | 1 |
| Poise | 10 |

**Player draws 5 cards:**
- Basic Step
- Side Together
- Head Accent
- Eye Contact
- Step Into Close

### Alistair's Lead

```
┌─────────────────────────────────┐
│       ALISTAIR'S LEAD           │
│                                 │
│       Open Invitation           │
│        Timing: Beats 1-8        │
│                                 │
│ He offers one hand and keeps    │
│ distance.                       │
│                                 │
│ Goal: Stay in Open stance and   │
│ maintain rhythm.                │
│                                 │
│ Success: +1 Bond, +25% score    │
│ Miss: No penalty, but no bonus  │
└─────────────────────────────────┘
```

This is a gentle opening. Alistair is basically saying:

> *"Stay with me. Keep rhythm. Do not rush into Close yet."*

### Player Builds the 8 Beats

The timeline has two bars:
- **Bar A:** Beats 1-4
- **Bar B:** Beats 5-8

The player chooses:

**Beats 1-4: Basic Step**
- Type: Footwork
- Stance: Open → Open
- Generates: +2 Flow

**Attach: Head Accent**
- Type: Styling
- Cost: 1 Flow
- Effect: +Style score

**Beats 5-8: Side Together**
- Type: Footwork
- Stance: Open → Open
- Generates: +2 Flow

**Timeline:**

```
  1   2   3   4  │  5   6   7   8
├───────────────┼───────────────┤
│  Basic Step   │ Side Together │
│ + Head Accent │               │
```

### Live Resource Preview

Before lock-in, the UI shows:

| Metric | Value |
|--------|-------|
| Beats | 8 / 8 |
| Final stance | Open |
| Flow generated | +4 |
| Flow spent | -1 |
| Flow remaining | 4 |
| Frame | 1 |
| Lead matched | Yes |
| Risk | Safe |

Flow remaining disappears after the phrase, unless a later upgrade lets the player carry some forward.

### Resolution

The game checks:
- Exactly 8 beats? ✓ Yes
- Correct stance chain? ✓ Yes
- Matched Open Invitation? ✓ Yes
- Frame check needed? No
- Poise lost? No

**Result:**

| Metric | Value |
|--------|-------|
| Phrase Score | 120 |
| Connection Bonus | +25% |
| **Final Phrase Score** | **150** |
| Bond | +1 |
| Poise | 10 / 10 |

### Cinematic Replay

The UI fades. The player sees:

1. Alistair offers his hand.
2. She steps cleanly into rhythm.
3. On Beat 4, she adds a sharp Head Accent.
4. They finish the phrase still in Open stance.

**This phrase teaches:**
- Footwork builds Flow
- Styling spends Flow
- Alistair's lead is an objective
- Matching him gives Bond and score

---

## Phrase 2 — "Enter Close"

### Start of Phrase

After Phrase 1:
- Used cards go to discard
- New hand is drawn
- Poise carries forward
- Score carries forward
- Flow resets
- Frame resets, except bonuses if any
- Stance carries forward between phrases

So the player starts Phrase 2 in Open stance because Phrase 1 ended Open.

| Stat | Value |
|------|-------|
| Phrase | 2 / 3 |
| Beats | 0 / 8 |
| Stance | Open |
| Flow | 1 |
| Frame | 0 |
| Poise | 10 |

**New hand:**
- Basic Step
- Step Into Close
- Close Sway
- Eye Contact
- Body Roll

### Alistair's Lead

```
┌─────────────────────────────────┐
│       ALISTAIR'S LEAD           │
│                                 │
│       Close Invitation          │
│        Timing: Beats 5-8        │
│                                 │
│ He draws his right hand toward  │
│ your back.                      │
│                                 │
│ Goal: Enter Close stance before │
│ Beat 5.                         │
│                                 │
│ Success: Perfect Connection x2  │
│          +2 Bond                │
│ Miss: Lose phrase multiplier    │
└─────────────────────────────────┘
```

Alistair is not taking a turn. He is setting the target:

> *"I am inviting you into Close for the second half of the phrase."*

### Player Builds the 8 Beats

The player needs to enter Close before Beat 5.

**Beats 1-4: Basic Step**
- Type: Footwork
- Stance: Open → Open
- Generates: +2 Flow

**Beats 5-6: Step Into Close**
- Type: Transition
- Stance: Open → Close
- Generates: +1 Frame

**Beats 7-8: Close Sway**
- Type: Footwork
- Stance: Close → Close
- Generates: +1 Flow

**Attach: Eye Contact**
- Type: Support
- Cost: 1 Flow
- Effect: +Bond, +Connection score

**Timeline:**

```
  1   2   3   4  │  5   6  │  7   8
├───────────────┼─────────┼─────────┤
│  Basic Step   │Step Into│Close    │
│               │Close    │Sway     │
│               │         │+Eye     │
│               │         │Contact  │
```

### Live Resource Preview

| Metric | Value |
|--------|-------|
| Beats | 8 / 8 |
| Final stance | Close |
| Flow start | 1 |
| Flow generated | +3 |
| Flow spent | -1 |
| Frame | 1 |
| Lead matched | Yes |
| Connection | Perfect |
| Risk | Safe |

### Resolution

The game checks:
- Exactly 8 beats? ✓ Yes
- Was player in Close by Beat 5? ✓ Yes
- Did player answer Alistair's Close Invitation? ✓ Yes
- Was Support used? ✓ Yes, Eye Contact

**Result:**

| Metric | Value |
|--------|-------|
| Base phrase score | 160 |
| Perfect Connection | x2 |
| Eye Contact bonus | +20 |
| **Final Phrase Score** | **340** |
| Bond | +2 |
| Poise | 10 / 10 |

### Cinematic Replay

The UI fades. The player sees:

1. **Beats 1-4:** They remain in Open, stepping cleanly.
2. **Beat 5:** Alistair draws her inward.
3. **Beats 5-6:** She accepts the Close transition.
4. **Beats 7-8:** They settle into Close Sway. Eye Contact triggers a slow camera close-up.

**This phrase teaches:**
- Alistair can ask for a stance change
- Transitions are how the player answers
- Support cards can turn a correct answer into an emotional moment

---

## Phrase 3 — "Survive the Dip"

### Start of Phrase

Phrase 2 ended in Close stance, so Phrase 3 starts Close.

| Stat | Value |
|------|-------|
| Phrase | 3 / 3 |
| Beats | 0 / 8 |
| Stance | Close |
| Flow | 1 |
| Frame | 0 |
| Poise | 10 |

**New hand:**
- Sensual Body Roll
- Arm Frame
- Anchor Step
- Crimson Dip
- Hair Accent

### Alistair's Lead

```
┌─────────────────────────────────┐
│       ALISTAIR'S LEAD           │
│                                 │
│         Sudden Dip              │
│        Timing: Beat 7           │
│                                 │
│ He lowers his stance and        │
│ prepares to take your weight.   │
│                                 │
│ Requirement:                    │
│ • Be in Close stance            │
│ • Have at least 3 Frame before  │
│   Beat 7                        │
│                                 │
│ Success: Cinematic Dip          │
│          Huge score, +3 Bond    │
│          Bonus Lumen            │
│                                 │
│ Failure: Stumble, -3 Poise      │
│          Break multiplier       │
└─────────────────────────────────┘
```

**This is the first dangerous lead.**

Alistair's intention is known because:
- His body lowers
- The UI marks Beat 7 in red
- The Lead panel warns: Frame required
- The music swells toward a dramatic accent

So the player understands:

> *"A dip is coming. I need to prepare my posture and trust before Beat 7."*

### Player Builds the 8 Beats

**Beats 1-4: Sensual Body Roll**
- Type: Footwork
- Stance: Close → Close
- Generates: +2 Flow
- Generates: +1 Frame

**Attach: Arm Frame**
- Type: Support
- Cost: 1 Flow
- Effect: +2 Frame

**Beats 5-6: Anchor Step**
- Type: Footwork / Prep
- Stance: Close → Close
- Generates: +1 Flow
- Generates: +1 Frame

**Beats 7-8: Crimson Dip**
- Type: Finisher
- Stance: Close → Open
- Cost: 2 Flow
- Requires: 3 Frame before Beat 7

**Timeline:**

```
  1   2   3   4  │  5   6  │  7   8
├───────────────┼─────────┼─────────┤
│Sensual Body   │ Anchor  │ Crimson │
│Roll           │ Step    │ Dip     │
│ + Arm Frame   │         │         │
```

### Resource Math

**Start:**
- Flow: 1
- Frame: 0

**After Sensual Body Roll:**
- Flow: 3
- Frame: 1

**After Arm Frame:**
- Flow: 2
- Frame: 3

**After Anchor Step:**
- Flow: 3
- Frame: 4

**Before Beat 7:**
- Frame requirement for Sudden Dip: 3
- Current Frame: 4
- ✓ **Pass**

**Crimson Dip costs 2 Flow:**
- Flow after Crimson Dip: 1

### Live Resource Preview

| Metric | Value |
|--------|-------|
| Beats | 8 / 8 |
| Final stance | Open |
| Flow | Enough |
| Frame by Beat 7 | 4 / 3 |
| Lead matched | Yes |
| Risk | Safe |
| Payoff | Cinematic Dip |

### Resolution

The game checks:
- Exactly 8 beats? ✓ Yes
- Started in Close? ✓ Yes
- Had 3+ Frame before Beat 7? ✓ Yes
- Had enough Flow for Crimson Dip? ✓ Yes
- Matched Sudden Dip? ✓ Yes

**Result:**

| Metric | Value |
|--------|-------|
| Base phrase score | 260 |
| Sudden Dip success bonus | +150 |
| Perfect Support bonus | x1.5 |
| **Final Phrase Score** | **615** |
| Bond | +3 |
| Poise | 10 / 10 |
| Bonus Lumen | Yes |

### Cinematic Replay

The UI fades. The player sees:

1. **Beats 1-4:** She rolls through the body movement, staying grounded.
2. **Beats 5-6:** She anchors her weight and builds Frame.
3. **Beat 7:** Alistair dips her.
4. **Beat 8:** She recovers cleanly into Open stance. The camera performs a dramatic orbit.

**This phrase teaches:**
- Dangerous Alistair leads require preparation
- Frame must exist before the dangerous beat
- Finishers are not just expensive; they require trust, stance, and timing

---

## End of Short Session

### Performance Summary

| Phrase | Score |
|--------|-------|
| Phrase 1 | 150 |
| Phrase 2 | 340 |
| Phrase 3 | 615 |
| **Total Score** | **1,105** |

| Stat | Value |
|------|-------|
| Poise remaining | 10 / 10 |
| Stumbles | 0 |
| Bond gained | +6 |

### Dawn Payout

| Reward | Amount |
|--------|--------|
| Lumen Essence | 110 |
| No-Stumble Bonus | +25 |
| Perfect Connection Bonus | +40 |
| **Total Lumen** | **175** |

**Bond with Alistair:** +6

**Card Mastery:**
- Basic Step +XP
- Step Into Close +XP
- Sensual Body Roll +XP
- Crimson Dip +XP

**Possible unlock:**
> *"Alistair now reveals Close Invitation one beat earlier."*

### Return to Day Phase

Then the player returns to the day phase:
- Spend Lumen on Mirror Hall training
- Upgrade Crimson Dip
- Craft better shoes
- Improve the Music Room
- Spend time with Alistair to learn a new lead pattern

**That completes the loop:**

```
Prepare
→ Dance
→ Read Alistair
→ Respond with cards
→ Watch cinematic payoff
→ Earn growth
→ Prepare better tomorrow
```

---

## What Happens If the Player Fails?

Suppose in Phrase 3 the player tries:
- Sensual Body Roll
- Hair Accent
- Crimson Dip

But she does **not** play Arm Frame or Anchor Step.

**Before Beat 7:**
- Frame required: 3
- Current Frame: 1

**The UI warns:**

```
⚠️ Sudden Dip unsafe
Frame too low
Stumble risk
```

**If the player locks in anyway:**

Beat 7: Alistair attempts the dip. She is not prepared. The dip becomes unstable.

### Failure Result

| Effect | Value |
|--------|-------|
| Stumble | Yes |
| Poise lost | -3 |
| Phrase multiplier | Broken |
| Crimson Dip score | Reduced |
| Bond bonus | None |
| Animation | Recovery step instead of full dip |

**Important:** The player does not lose cards, the run does not end permanently, and progression does not reset.

It is a **graceful failure:**
- The dance faltered
- The night continues, unless Poise reaches 0

---

## Why This Works Better Than Giving Alistair a Turn

A separate Alistair turn would feel strange:

```
Player dances → Alistair attacks → Player dances → Alistair attacks
```

That is not romantic partner dance.

The better structure is:

```
Alistair leads → Player follows → The dance judges the connection
```

This keeps him active without making him feel like an enemy.

**He creates:**
- Pressure
- Invitation
- Risk
- Romance
- Timing objectives
- Stance objectives
- Frame requirements

**The player creates:**
- Response
- Style
- Safety
- Expression
- Connection
- Score

---

## The Clean 3-Phrase Structure

A beginner short session should follow this teaching arc:

| Phrase | Alistair's Lead | Player Lesson | Emotional Beat |
|--------|-----------------|---------------|----------------|
| 1 | Open Invitation | Learn rhythm, beats, Flow, Styling | "Stay with me." |
| 2 | Close Invitation | Learn stance change and Connection | "Come closer." |
| 3 | Sudden Dip | Learn Frame, trust, and danger | "Trust me." |

That is a strong mini-session because it has escalation:

```
Rhythm → Intimacy → Trust
```

And mechanically:

```
Footwork → Transition → Support / Finisher
```

---

## The Loop in Pseudocode

```
START DAY

Player chooses 2 Day Actions:
  train / rehearse / style / bond / improve castle

Apply day bonuses:
  outfit bonuses
  facility bonuses
  relationship bonuses
  deck changes

START NIGHT PERFORMANCE

Set:
  Poise
  Starting stance
  Active deck
  Song
  Alistair lead sequence

For phrase 1 to 3:

  Reset phrase Flow and Frame
  Apply starting Flow / Frame bonuses

  Draw hand

  Reveal Alistair's Lead:
    invitation / danger / mood / exit / accent

  Player builds exactly 8 beats:
    place Footwork and Transition cards
    attach Styling and Support cards
    obey stance requirements
    spend Flow
    build Frame if needed

  Validate:
    exactly 8 beats
    legal stance chain
    enough Flow
    enough Frame by required beat
    Alistair's lead matched or missed

  Resolve:
    score
    connection multiplier
    Bond gain
    Poise loss if stumble
    cinematic replay

  Discard played hand
  Continue to next phrase

END NIGHT

Convert score to:
  Lumen Essence
  Bond
  card mastery
  materials
  unlock progress

START DAWN

Player spends or saves rewards.
New dialogue or facility unlocks appear.
Next day begins.
```

---

## Final Recommendation

Make Alistair's system explicit in the UI as:

> **ALISTAIR'S LEAD**

not:

> ~~Alistair's Turn~~

He should feel like a romantic partner with readable intention, not an opponent.

**The player's job each phrase is:**
1. Read the lead
2. Fill 8 beats
3. Prepare enough Flow and Frame
4. Choose how expressive or safe to be
5. Lock in
6. Watch the dance
7. Grow afterward

**That gives you a clear mobile session:**
- 3 phrases
- 24 beats total
- One complete mini-performance
- One emotional arc with Alistair
- One progression payout
