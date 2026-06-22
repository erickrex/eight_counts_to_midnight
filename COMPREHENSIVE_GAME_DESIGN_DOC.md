# Dancing with Dracula: Crimson Manor

Comprehensive Game Design Document

Version: 0.1  
Platform: Mobile, iOS and Android  
Orientation: Portrait  
Genre: Simulation and Management / Persistent RPG Card Game / Romance Deck Construction  
Core Theme: Gothic romance, Bachata choreography, estate restoration, tactical card play  

---

## 1. Design Canon

This document is the current source of truth for the Bachata deckbuilder mobile game.

The most important design constraint is that this is **not a roguelike**. The game borrows pacing ideas from tactical card games, but it does not use permadeath, disposable decks, random map runs, or run-based progression resets.

The game uses short card-driven dance decisions inside each nightly performance, but all meaningful progression is persistent. Cards, room upgrades, outfits, social bonds, unlocked mechanics, and manor state carry forward permanently.

### Canon Rules

- The player owns a persistent card collection.
- The standard active dance deck is 20 cards.
- Early tutorial days use restricted starter decks before the full 20-card format unlocks.
- Each night is a performance, not a run.
- Each performance contains several 8-beat phrases.
- Each phrase must resolve to exactly 8 Beats once full play is unlocked.
- There is no permadeath.
- Failure causes a stumble, score loss, Poise loss, reduced rewards, or early song end.
- The player restores the manor permanently with Lumen Essence.
- Relationship progression with Alistair unlocks dialogue, lore, passive buffs, and temporary performance bonuses.

---

## 2. Executive Summary

### Working Title

**Dancing with Dracula: Crimson Manor**

### Logline

A gothic estate-management romance game where players restore a cursed manor by day, then construct persistent Bachata card decks to dance with its brooding Vampire Lord by night.

### High Concept

The player inherits or discovers the ruined Crimson Manor, a gothic estate sealed under a centuries-old curse. At its center is Alistair, a Vampire Lord frozen in stone inside the Grand Ballroom. By dancing with him each night, the player generates Lumen Essence, restores the manor, unlocks new rooms, upgrades cards, deepens their bond with Alistair, and gradually breaks the curse.

The moment-to-moment gameplay is a portrait-mode dance card engine built around short 8-count Bachata phrases. Players combine Footwork, Transition, Styling, and Support cards to build musically accurate dance routines. At the end of each phrase, the UI disappears and the characters perform the chosen movement as a cinematic 3D sequence.

The long-term gameplay is a persistent simulation loop: collect cards, merge duplicates, restore rooms, unlock new mechanics, equip outfits, improve social links, and build a stronger deck for future nightly performances.

### Target Audience

- Women 18-35 interested in romance, cozy games, fashion, narrative progression, and character bonding.
- Cozy simulation players who enjoy visible restoration and daily routines.
- Tactical CCG and deck-construction players who enjoy combo optimization.
- Mobile players who want short but satisfying sessions.

### Hackathon / Pitch Positioning

The game fits a Simulation and Management category by making estate restoration, relationship management, deck collection, and daily planning the main persistent structure. It replaces simple tycoon tapping with a deep musical card system wrapped in high-end gothic romance visuals.

The loop is:

```text
Invest by day -> Perform by night -> Restore at dawn -> Expand tomorrow
```

---

## 3. Design Pillars

### Pillar 1: Persistent Romance Simulation

The player is not just completing isolated dances. They are living through an in-game calendar, restoring an estate, and developing a relationship with Alistair. The manor, deck, wardrobe, and relationship state all persist.

### Pillar 2: Bachata as Tactical Language

Every dance phrase is built from real-feeling Bachata concepts: 8-count timing, stance changes, frame, lead/follow connection, sensual styling, and musical accents.

### Pillar 3: Easy to Read, Hard to Master

The UI treats each turn as an 8-beat musical phrase. Beginners can play obvious legal cards. Advanced players optimize Flow, Frame, stance chains, multipliers, and Alistair's lead patterns.

### Pillar 4: Visible Restoration

Every major restoration must visibly transform the estate. Thorns burn away, stained glass repairs itself, moonlight returns, dead vines bloom, rooms unlock, and the dance floor becomes more spectacular over time.

### Pillar 5: Cinematic Payoff

The player must see the routine they built. Cards are not abstract effects; they become animated partner-dance phrases. The game regularly rewards good play with camera movement, close-ups, and visual flourishes.

### Pillar 6: One-Handed Mobile First

The game is built for portrait play. The top half of the screen showcases the 3D dance and manor environment. The bottom half contains the hand, timeline, and drag targets.

---

## 4. Game Structure

## 4.1 The Core Day/Night Loop

The game follows a continuous in-game calendar.

### Day: Invest and Prepare

During the day, the player navigates the manor hub and prepares for the night. To make the simulation layer explicit, each day gives the player **2 Day Action slots**.

Each day, choose 2 of 4:

- **Rehearse cards:** Use the Rehearsal Grid to merge duplicates, refine the active deck, and prepare a specific dance plan.
- **Restore a room:** Spend Lumen Essence to repair part of the manor and unlock new systems.
- **Spend time with Alistair:** Trigger dialogue, gain Bond, reveal lore, or earn a temporary performance boon.
- **Search manor debris:** Find duplicate cards, restoration materials, wardrobe pieces, or room clues.

Free supporting actions, such as reviewing the Binder, inspecting unlocked rooms, or changing outfits, can happen without spending a Day Action slot.

The day phase is slow, intimate, and strategic. It should feel like preparing for a dance.

### Night: Perform and Harvest

At night, the player enters the Grand Ballroom for a short dance performance. For the hackathon pitch and MVP, one performance is three playable 8-beat phrases. The full game can expand this into longer songs after the core loop is proven.

Night actions include:

- Draw hands from the active deck.
- Build 8-beat phrases.
- Read Alistair's lead pattern.
- Match stance requirements.
- Generate and spend Flow.
- Build Frame to handle dips and demanding leads.
- Trigger cinematic phrase replays.
- Build score multipliers.
- Preserve Poise.
- Generate Lumen Essence.

The night phase is tactical and expressive. The player should feel like they are choreographing with a dangerous but elegant partner.

### Dawn: Restore and Grow

At dawn, the player spends rewards and sees permanent progress.

Dawn actions include:

- Spend Lumen Essence on manor restoration.
- Unlock rooms and systems.
- Gain access to new card pools.
- Improve visual state of the estate.
- Resolve narrative beats from the night's dance.
- Bank relationship progress.
- Preview the next day's objectives.

The dawn phase is the emotional release. The player sees proof that the dance mattered.

---

## 5. Persistent Progression

The game has several interconnected progression tracks.

### 5.1 Card Collection

The player owns a persistent collection called the Binder. Cards are not discarded between nights. They can be earned, found, upgraded, merged, and slotted into the active dance deck.

The standard active deck contains exactly 20 cards once fully unlocked. Tutorial days use smaller controlled decks to avoid overwhelming new players.

Suggested deck-size onboarding:

| Day / Milestone | Active Deck Format | Purpose |
| --- | ---: | --- |
| Day 1 | Guided 8-card starter deck | Teach Open stance, Beats, Flow, and simple Styling |
| Day 2 | 12-card deck | Teach stance transition, Alistair's lead patterns, and merging |
| Day 3 | 16-card deck | Teach Frame, Poise, and Support planning |
| Day 7 | Full 20-card deck | Full deck construction unlocked |

### 5.2 Merge Progression

Duplicate cards can be merged during the day through the Rehearsal Grid.

Base merge rule:

```text
3 duplicate cards -> 1 upgraded version
```

Examples:

- 3 Basic Step cards -> 1 Foil Basic Step
- 3 Basic Side-Step cards -> 1 Cathedral Walk
- 3 Arm Frame cards -> 1 Iron Frame

Merge upgrades can improve:

- Base points.
- Flow generated.
- Flow cost.
- Frame value.
- Slot count.
- Stance flexibility.
- Multiplier tags.
- Animation flourish.
- Rarity.

Merge upgrades are permanent. This reinforces the non-roguelike structure.

### 5.3 Manor Restoration

Lumen Essence is spent to restore rooms.

Each room provides:

- A visible environmental transformation.
- A new card pool or card type.
- A passive system upgrade.
- A narrative beat.
- A reason to return to the day phase.

Example rooms:

| Room | Visual Restoration | System Unlock |
| --- | --- | --- |
| Grand Ballroom | Thorns burn away, marble floor returns | Nightly performances |
| Stained-Glass Gallery | Moonlight returns, lighting changes | Improved score multipliers |
| Grand Library | Shelves repair, ghostly pages return | Advanced Footwork and later Syncopation cards |
| Wardrobe Atelier | Gowns, gloves, jewelry, and restored heirlooms | Outfit stats and Starting Frame |
| Gothic Conservatory | Dead vines bloom into midnight roses | Sensual Styling and botanical buff cards |
| Music Room | Instruments retune themselves | New songs, tempo modifiers, audio layers |
| Mirror Hall | Broken mirrors reform | Cinematic replay upgrades |

### 5.4 Relationship Progression

Alistair is both the main romantic interest and the dance partner. His relationship track should be mechanically relevant without reducing the romance to pure optimization.

Relationship progression can unlock:

- Visual-novel scenes.
- Lore memories.
- New lead patterns.
- Passive buffs.
- Temporary night-specific boons.
- Unique card rewards.
- Cosmetic poses and camera moments.
- Alternate endings or route scenes.

Relationship currency is separate from Lumen Essence.

Recommended currency split:

| Currency | Source | Primary Use |
| --- | --- | --- |
| Lumen Essence | Nightly score and restored room bonuses | Restore manor, unlock rooms, upgrade estate |
| Intimacy / Bond | Dialogue, gifts, matching Alistair's lead, story milestones | Unlock relationship scenes and social buffs |
| Card Shards / Duplicates | Manor discoveries, room rewards, dance rewards | Merge and upgrade cards |

### 5.5 Wardrobe and Equipment

Outfits are not just cosmetics. Gowns and accessories alter starting conditions and encourage different play styles.

Example outfit stats:

- +1 Starting Flow.
- +5 Starting Frame.
- +10% Lumen from Close stance phrases.
- First Stumble each night costs no Poise.
- Styling cards cost 1 less Flow once per phrase.
- Wrap cards score higher but Transition cards cost more.

Outfits should visually reinforce the gothic romance fantasy and create build identity without invalidating card strategy.

---

## 6. The Dance Engine

The Dance Engine is the main interactive system.

### 6.1 Performance, Phrase, and Beat

The night performance is divided into phrases.

Definitions:

- **Performance:** One nightly dance/song.
- **Phrase:** One playable turn in the dance.
- **Beat:** The timing unit used by Footwork and Transition cards.
- **8-count:** One full Bachata phrase, counted 1-2-3-4-5-6-7-8.

Recommended performance structure:

| Element | Target |
| --- | ---: |
| MVP performance length | 3 short phrases |
| Full-game performance length | Expandable after MVP |
| Phrase length | Exactly 8 Beats |
| Cinematic replay | Phrase-by-phrase playback after each lock-in |

The player does not need to manually place every beat. The UI presents the phrase as two musical bars:

```text
Bar A: Beats 1-4
Bar B: Beats 5-8
```

Each bar can hold:

- one 4-beat Footwork card, or
- two 2-beat cards, usually Transition plus Footwork, or
- one 4-beat Footwork card when stance requirements are met.

### 6.2 Base + Modifier System

The core UI solution is vertical layering.

Instead of every card occupying horizontal timeline space, cards are split into base cards and modifier cards.

Base cards create the visible routine block:

- Footwork
- Transition

Modifier cards attach vertically to base cards:

- Styling
- Support

Example:

```text
Madrid Step
  Slot 1: Arm Throw
  Slot 2: Sensual Hip Roll
```

The player has played multiple cards, but the UI displays one coherent routine block. This keeps the phone screen readable while preserving combo depth.

### 6.3 Beats

Beats are the hard timing limit of a phrase.

Rules:

- A full phrase must total exactly 8 Beats.
- Footwork and Transition cards usually cost Beats.
- Styling and Support cards usually do not cost Beats.
- Tutorial Day 1 may use a guided half-phrase before introducing full 8-count play, but the canonical system is 8 Beats.

Allowed Beat costs:

- 1 Beat: rare accents or advanced technical cards.
- 2 Beats: transitions, short payoff moves, preparation steps.
- 4 Beats: standard Bachata movement chunks.
- 8 Beats: full macro-routines.

### 6.4 Flow

Flow is the secondary combo resource.

Flow exists to let players play expressive modifier cards without breaking the strict 8-beat structure.

Rules:

- Footwork usually generates Flow.
- Styling and Support cards usually cost Flow.
- Flow is phrase-local by default.
- Unspent Flow disappears at the end of the phrase.
- Some outfits, relationship buffs, and room upgrades can grant Starting Flow.
- Starting Flow should be small in early balance, usually +1 to +3.

Example:

```text
Basic Side-Step costs 4 Beats and generates 1 Flow.
The player spends 1 Flow to attach Head Accent.
```

### 6.5 Advanced Library Unlock: Syncopation

Syncopation is not part of the first pitch or MVP. It is a later Grand Library unlock for players who already understand the core loop.

When introduced, Syncopation cards act as 0-Beat flourish cards tied to specific anchors. For example, Hair Toss can only be played immediately after Body Roll. This gives advanced players combo depth without adding complexity to the first-session experience.

### 6.6 Stances

Every movement card has a Prerequisite Stance and Ending Stance.

If a card does not match the current stance, it is greyed out in the player's hand.

Core stances:

| Stance | Description | Gameplay Identity |
| --- | --- | --- |
| Open | Standard hand-to-hand position | High mobility, low intimacy multiplier |
| Close | Close embrace | Required for sensual moves, high tension multiplier |
| Wrap | Follower is wrapped against the leader | High scoring, restrictive exits |

Stance creates the deckbuilding puzzle. A powerful card is only useful if the player can enter the required stance at the right time.

### 6.7 Frame

Frame is the support resource used to handle demanding partner moves.

Rules:

- Frame is generated by certain Transition and Support cards.
- Frame is phrase-local by default.
- Frame resets after each phrase.
- Heavy dips and demanding lead patterns require minimum Frame.
- If the player lacks required Frame, they stumble.

Example:

```text
Sudden Dip
Lead Pattern
Timing: Beat 7
Requirement: 20 Frame by Beat 7
Failure: Stumble, lose Poise, break multiplier
Success: Perfect Support, bonus Lumen
```

Frame should feel like poise, posture, and trust, not a generic protection stat.

### 6.8 Poise

Poise is the player's nightly mistake buffer.

Rules:

- The player starts each performance with a set amount of Poise.
- Stumbles reduce Poise.
- Reaching 0 Poise can end the song early.
- Ending early still awards partial Lumen Essence.
- There is no permadeath and no loss of owned cards.

Poise preserves stakes while avoiding roguelike punishment.

### 6.9 Alistair's Lead

Alistair's lead is the telegraphed dance pattern the player responds to.

The lead tells the player what Alistair is inviting or what support he needs. The player can score better by matching him or protect themselves by preparing Frame.

Examples:

- "Close on Beats 5-8"
- "Sudden Dip on Beat 7"
- "Wrap exit expected"
- "Sensual phrase"
- "Aggressive lead"

Matching the lead creates a Perfect Connection bonus. Missing a dangerous lead can reduce score, break multiplier, or trigger a Stumble depending on severity.

---

## 7. Card Taxonomy

### 7.1 Card Types

The competition version uses exactly four card categories. Future mechanics can add tags or subsets, but they should still map back to one of these four categories.

| Type | Beat Cost | Flow Cost | Primary Purpose |
| --- | ---: | ---: | --- |
| Footwork | Usually 4 or 8 | 0 | Base movement, Flow generation |
| Transition | Usually 2 | 0 | Change stance, prepare card chains |
| Styling | 0 | 1-3 | Add score, multipliers, visual layers |
| Support | 0 | 1-3 | Build Frame, match Alistair's lead, stabilize phrase |

### 7.2 Card Anatomy

Every card should be defined with the following fields:

```text
Card Name
Type
Rarity
Beat Cost
Flow Cost
Flow Generated
Prerequisite Stance
Ending Stance
Base Points
Multiplier Tags
Frame Value
Slot Count
Anchor Requirement
Timing Requirement
Animation Tag
Upgrade Path
Room Unlock Source
Flavor Text
```

### 7.3 Rarity and Upgrade Tiers

Suggested rarity:

- Common
- Uncommon
- Rare
- Epic
- Legendary

Suggested upgrade tiers:

- Standard
- Foil
- Embroidered
- Moonlit
- Crimson

Upgrade tiers should improve mechanics and visuals. A merged card should feel more elegant on the dance floor, not just stronger in numbers.

---

## 8. Example Cards

The full working card list lives in [card_catalog_file.md](/Users/erickrea/Documents/Dancing%20with%20Dracula%20-%20Bachata%20deckbuilder/card_catalog_file.md). The main GDD only needs enough examples to show how the dance loop works.

| Card | Type | Cost | Stance | Pitch Purpose |
| --- | --- | --- | --- | --- |
| Basic Side-Step | Footwork | 4 Beats | Any -> Same | Beginner base move. Generates Flow and creates a Styling slot. |
| Madrid Step | Footwork | 4 Beats | Open -> Open | Stronger base move that generates more Flow. |
| Step Into Close | Transition | 2 Beats | Open -> Close | Teaches stance change and prepares sensual moves. |
| Sensual Body Roll | Footwork | 4 Beats | Close -> Close | Shows why Close stance matters. |
| Head Accent | Styling | 1 Flow | Attach to Footwork | First vertical modifier. Adds visual flair without using Beats. |
| Arm Frame | Support | 2 Flow | Any | Builds Frame to safely handle a dip. |
| The Sensual Dip | Footwork | 4 Beats | Close -> Open | High-payoff move that requires enough Frame. |

---

## 9. Alistair Lead Patterns

Alistair's lead patterns are the dance equivalent of goals and pressure. They should be framed as dance invitations and support requirements. The player is reading, matching, and supporting a partner.

For the hackathon-facing design, keep only a few patterns:

| Lead Pattern | Timing | Player Response | Success | Miss |
| --- | --- | --- | --- | --- |
| Open Invitation | Beats 1-8 | Stay in Open and maintain rhythm | Small Connection bonus | No penalty |
| Close Invitation | Beats 5-8 | Enter Close before Beat 5 | x2 Perfect Connection | Reduced multiplier |
| Sudden Dip | Beat 7 | Be in Close and reach 20 Frame | Cinematic supported dip, bonus Lumen | Stumble, lose Poise |
| Sensual Phrase | Beats 5-8 | Play a Close stance move | Higher Lumen and romance tension | Missed bonus |

This gives the pitch enough tactical clarity without making the system sound like a large challenge catalog.

---

## 10. Scoring and Reward Formula

The scoring model should be easy to explain. The pitch only needs one formula that connects dance performance to manor restoration.

### 10.1 Phrase Score

Simple formula:

```text
Phrase Score = Card Points x Connection Multiplier
```

Example:

```text
Madrid Step: 60 points
Head Accent: 25 points
Close Invitation matched: x2

Phrase Score = (60 + 25) x 2 = 170
```

### 10.2 Lumen Essence

At dawn, phrase scores convert into Lumen Essence for room restoration.

```text
Lumen Essence = Floor(Total Performance Score / Essence Divisor) + Objective Bonuses
```

Objective bonuses can include:

- First time matching a new lead pattern.
- No Stumbles.
- Perfect Support on a dip.
- Completing a room-related objective.
- Ending with high Poise.

### 10.3 Bond / Intimacy

Bond should reward emotional and expressive play, not just raw score.

Sources:

- Dialogue choices.
- Matching Alistair's lead.
- Playing Eye Contact or similar Support cards.
- Clearing story objectives.
- Choosing vulnerable or trusting responses in VN scenes.

Uses:

- Unlock relationship scenes.
- Unlock lore memories.
- Gain temporary night buffs.
- Unlock Alistair-specific cards.
- Unlock alternate camera moments.

---

## 11. Failure Model

Failure must create tension without roguelike punishment.

### 11.1 Stumble

A Stumble occurs when:

- The player fails a required Frame check.
- The player is in the wrong stance for a dangerous lead.
- Poise is reduced by a demanding lead pattern.
- A required exit from Wrap is missed.

Stumble effects:

- Break current multiplier.
- Lose Poise.
- Reduce phrase score.
- Interrupt or alter animation.
- Possibly end song early if Poise reaches 0.

### 11.2 Early Song End

If the player loses all Poise, the song can end early.

The player still receives:

- Partial Lumen Essence.
- Any earned Bond.
- Any tutorial completion progress.
- No loss of owned cards.
- No reset of manor state.

The tone should be graceful: the player stumbled, the dance ended, and dawn came with fewer rewards.

---

## 12. Visual and Audio Design

### 12.1 Visual Direction

Style target:

- High-end cel-shaded 3D.
- Gothic romance.
- Dramatic moonlight.
- Elegant but readable character silhouettes.
- Expressive cloth, hair, and hand animation.
- Restored rooms become progressively richer and warmer.

The game should avoid generic dark fantasy mud. The manor is cursed, but restoration should bring color, glow, and romance back into the space.

### 12.2 Screen Layout

Portrait layout:

```text
Top 50%: 3D stage, dancers, manor environment, lead telegraphs
Middle: 8-beat phrase timeline / two-bar routine display
Bottom 50%: hand, deck controls, drag targets
```

Interaction:

- Drag cards upward from hand.
- Drop Footwork and Transition cards onto Bar A or Bar B.
- Drop Styling and Support cards directly into card slots.
- Illegal cards grey out.
- Alistair's lead appears near him or above the timeline.
- The player's thumb should be able to reach most controls one-handed.

### 12.3 Cinematic Phrase Replay

After the player locks in an 8-beat phrase:

- UI fades or collapses.
- Camera focuses on the dancers.
- Base Footwork animation plays.
- Styling cards apply additive upper-body, hair, cloth, or hand layers.
- VFX and lighting respond to score events.

### 12.4 Tornado Camera

The Tornado Camera is a dramatic reward camera.

Trigger examples:

- Open -> Close -> Wrap chain.
- Perfect Connection with high multiplier.
- Successful Supported Dip.
- Final phrase climax.

Behavior:

- Camera orbits 180 degrees around the couple.
- Speed ramp on Beats 4 and 8.
- Shallow depth-of-field close-up on key accents.
- Returns to stable view after the phrase.

### 12.5 End-of-Performance Cinematic

At the end of a performance, the game briefly recaps the strongest phrase as an in-app cinematic moment. For the hackathon pitch, this is a visual payoff inside the game.

---

## 13. Audio Design

The audio design must make the 8-beat structure legible.

Core requirements:

- Bachata instrumental foundation.
- Clear 1-2-3-tap, 5-6-7-tap phrasing.
- Musical accents on Beats 4 and 8.
- Layered percussion for multiplier growth.
- Subtle heartbeat or vampiric ambience during demanding lead patterns.
- Warm musical swell when rooms restore.
- Distinct audio stingers for Perfect Connection, Stumble, and Perfect Support.

The player should learn timing partly by ear.

---

## 14. Narrative Design

### 14.1 Premise

The protagonist arrives at Crimson Manor and discovers Alistair, a Vampire Lord frozen in stone by a centuries-old curse. The Grand Ballroom is choked by black thorns, stained glass is shattered, and the manor has fallen into ruin.

The curse can only be weakened through dance. Each night, the protagonist dances with Alistair, drawing Lumen Essence from rhythm, trust, and connection. Each dawn, that essence restores part of the manor.

### 14.2 Player Character

The protagonist should be a romantic but capable lead. She is not a passive observer. She restores the manor, makes strategic choices, builds the deck, chooses how to respond to Alistair, and decides how much to trust him.

Possible framing:

- A dancer who has inherited the manor.
- A restoration specialist drawn to a cursed estate.
- A musician or choreographer researching a forgotten ballroom.
- A descendant of the person who sealed Alistair.

### 14.3 Alistair

Alistair is the Vampire Lord of Crimson Manor.

Character identity:

- Brooding but not cruel.
- Dangerous but controlled.
- Guarded early, increasingly vulnerable.
- Expresses emotion through dance before words.
- His power is tied to the manor's state.
- His lead patterns become more complex as his strength returns.

### 14.4 Romance Arc

The romance should escalate through trust and embodied connection.

Arc:

1. Contact: touch the statue, first dance.
2. Speech: Alistair can speak but remains guarded.
3. Trust: he begins telegraphing more honestly.
4. Vulnerability: VN scenes reveal curse history.
5. Partnership: advanced dances require mutual trust.
6. Choice: the player decides how to resolve the curse.

---

## 15. First Three Days Journey Map

This section defines the onboarding sequence and resolves the current deck-size and phrase-length contradictions.

### Day 1: The Awakening and the First 8-Count

Objective:

- Introduce the Day/Night/Dawn loop.
- Introduce Open stance.
- Introduce Beats.
- Introduce simple Flow.
- Introduce one Styling modifier.
- Show visible restoration.

#### Day Narrative

The protagonist arrives at the ruined Crimson Manor. The Grand Ballroom is choked by black thorns. In the center of the room stands Alistair, the Vampire Lord, frozen in stone.

The player touches his hand. The ballroom reacts. Music begins faintly under the stone floor.

#### Day Invest

The player opens the Binder for the first time. The starter deck is guided and restricted.

Day 1 deck:

- 8-card guided starter deck.
- Only Open stance cards.
- Only Basic Footwork and simple Styling.
- No manual deck construction yet.

Example cards:

- Basic Side-Step.
- Basic Step.
- Head Accent.
- Breath Sync.

#### Night Harvest

Tutorial phrase:

```text
Start Stance: Open

Bar A, Beats 1-4:
Basic Side-Step
Generates 1 Flow

Bar B, Beats 5-8:
Basic Side-Step
Generates 1 Flow

Modifier:
Head Accent attaches to Bar B
Costs 1 Flow

Result:
Complete 8-beat phrase, simple visual flourish on Beat 8
```

Animation:

- The UI drops away.
- The protagonist and Alistair execute a simple Bachata side-step phrase.
- The Head Accent lands on Beat 8.
- Alistair's stone shell cracks.

#### Dawn Restoration

The player earns first Lumen Essence. They spend it to burn away the thorns in the center of the ballroom. A polished marble floor is revealed. Alistair breaks fully out of stone and breathes again.

Unlocks:

- Dawn restoration screen.
- Grand Ballroom restored to Level 1.
- Alistair can now speak.

### Day 2: The Stance Shift and the Rehearsal Grid

Objective:

- Introduce Close stance.
- Introduce Alistair's lead patterns.
- Introduce Transition cards.
- Introduce merging duplicates.
- Introduce first camera reward.

#### Day Narrative

Alistair can now speak, but he is guarded and weak. He explains that the ballroom still suppresses his power because the stained-glass windows are shattered and the moonlight cannot enter properly.

#### Day Invest

The player finds duplicate Basic Step cards in the debris.

The Rehearsal Grid unlocks:

```text
3 Basic Step cards -> 1 Foil Basic Step
```

The player performs the first merge and slots the upgraded card into the active deck.

Day 2 deck:

- 12-card active deck.
- Open and Close stance cards.
- First Transition card: Step Into Close.
- First lead-pattern tutorial.

#### Night Harvest

Alistair's lead appears:

```text
Close Invitation
Timing: Beats 5-8
Response: Enter Close before Beat 5
Reward: x2 Perfect Connection
```

Tutorial phrase:

```text
Start Stance: Open

Bar A, Beats 1-4:
Foil Basic Step
Generates 2 Flow

Bar B, Beats 5-6:
Step Into Close
Open -> Close
Adds 10 Frame

Bar B, Beats 7-8:
Close Sway
Close -> Close

Modifier:
Eye Contact attaches to Close Sway
Costs 1 Flow

Result:
Lead matched, Perfect Connection x2
```

Camera payoff:

- Because the player matched Alistair's lead and transitioned Open -> Close smoothly, the Tornado Camera triggers.
- The camera orbits 180 degrees and slows into a close-up on Beat 8.

#### Dawn Restoration

The player spends Lumen Essence to restore the broken stained-glass windows. Moonlight streams into the ballroom and permanently changes the lighting of future dances.

Unlocks:

- Stained-Glass Gallery Level 1.
- Lead preview for future dances.
- Slight score bonus for Perfect Connection.

### Day 3: Frame, Support, and Expansion

Objective:

- Introduce Frame.
- Introduce Poise loss and Stumble.
- Introduce a demanding lead pattern.
- Introduce relationship buff.
- Unlock the next manor room.

#### Day Narrative

Alistair warns that tonight's rhythm will be more demanding. He gives the player a key to a locked wing of the manor. The player learns that the curse reacts violently as the manor wakes.

Depending on chosen structure, Day 3 can unlock either:

- Grand Library, if the focus is advanced card knowledge and later Syncopation.
- Gothic Conservatory, if the focus is sensual styling and botanical restoration.

Recommended canon for current build:

- Day 3 unlocks the **Grand Library**.
- The Conservatory becomes a Week 1 or Day 4-5 unlock.

#### Day Invest

The player spends banked Bond / Intimacy to unlock a visual-novel dialogue sequence with Alistair.

Dialogue reward example:

```text
Choice: Flirty
Reward: +2 Starting Flow for tonight's first phrase
```

The player edits the deck to include Support cards.

Day 3 deck:

- 16-card active deck.
- Open and Close stance cards.
- Basic Support cards.
- First Frame check response.

#### Night Harvest

Lead Pattern:

```text
Sudden Dip
Timing: Beat 7
Requirement: Be in Close and have 20 Frame before Beat 7
Success: Perfect Support
Failure: Stumble, lose Poise, break multiplier
```

Tutorial phrase:

```text
Start Stance: Open
Starting Buff: +2 Flow

Bar A, Beats 1-4:
Madrid Step
Generates 2 Flow

Modifier:
Arm Frame
Costs 2 Flow
Adds 10 Frame

Modifier:
Grounded Posture
Costs 1 Flow
Adds 5 Frame

Bar B, Beats 5-6:
Step Into Close
Open -> Close
Adds 10 Frame

Bar B, Beats 7-8:
Supported Dip / The Sensual Dip
Requires 20 Frame

Result:
Frame total reaches 25
Perfect Support triggers
```

Animation:

- The player supports the dip instead of stumbling.
- Alistair and the protagonist execute a gravity-defying dip.
- The Tornado Camera or a special dip camera triggers.

#### Dawn Restoration

The player earns a large Lumen payout for successfully supporting the demanding dance. They unlock the Grand Library. Dead vines withdraw from the shelves, ghostly pages return to floating books, and moonlit dust fills the room.

Unlocks:

- Grand Library Level 1.
- Advanced Footwork card pool.
- First optional Library flourish cards begin appearing in loot.
- Hair Toss becomes available later as an advanced Body Roll anchor card.

---

## 16. Week One Progression Outline

Only the first three days are fully specified above, but the broader first-week shape should be:

| Day | Main Unlock | Player Learning |
| --- | --- | --- |
| Day 1 | Ballroom Level 1 | Beats, Flow, Open stance |
| Day 2 | Stained-Glass Gallery | Close stance, lead patterns, merging |
| Day 3 | Grand Library | Frame, Poise, demanding leads |
| Day 4 | Library flourish cards | Optional Syncopation unlock |
| Day 5 | Wardrobe Atelier | Outfits and starting stats |
| Day 6 | Mirror Hall | In-app cinematic replay upgrades |
| Day 7 | Full 20-card deck | Complete deck construction format |

---

## 17. Economy and Balance Targets

### 17.1 Session Length

| Activity | Target Length |
| --- | ---: |
| Day preparation | 1-3 minutes |
| Night performance | Three short phrases for MVP |
| Dawn restoration | 30-90 seconds |
| Full daily loop | 5-10 minutes |

### 17.2 Early Reward Cadence

The first three days should each provide:

- One new mechanic.
- One visible restoration.
- One emotional beat with Alistair.
- One deck or card improvement.
- One reason to return tomorrow.

### 17.3 Restoration Costs

Early restorations should be affordable enough to guarantee visible progress.

Suggested early costs:

| Restoration | Cost | Notes |
| --- | ---: | --- |
| Clear Ballroom Thorns | 10 Lumen | Guaranteed after Day 1 |
| Restore Stained Glass | 25 Lumen | Guaranteed or near-guaranteed after Day 2 |
| Unlock Grand Library | 50 Lumen | Achievable after Day 3 with good play |
| First Outfit Repair | 40 Lumen + material | Optional side path |
| First Card Merge | 3 duplicate cards | Tutorial-driven |

Exact values should be tuned after prototype scoring exists.

---

## 18. Mobile UX Requirements

### 18.1 Hand and Timeline

The UI must stay readable on a phone.

Requirements:

- Hand size should start small, likely 4 cards in Day 1.
- Standard hand size should be 5 cards.
- Advanced upgrades may draw 6.
- The phrase display should show Bar A and Bar B, not 8 cramped columns.
- Cards should be large enough to read by thumb.
- Illegal cards grey out with stance or resource reason.
- Modifier slots should be visible directly on base cards.

### 18.2 Input Rules

Core interactions:

- Swipe or drag base cards upward into Bar A / Bar B.
- Drag modifiers onto visible slots.
- Tap card to inspect.
- Long-press for full details.
- Confirm phrase with a clear lock-in button.
- Undo last card before lock-in.

### 18.3 Feedback

The player must understand legality and consequences before committing.

Feedback examples:

- "Need Close" on greyed-out Body Roll.
- "Need 20 Frame by Beat 7" on Sudden Dip.
- Flow counter pulses when Footwork generates Flow.
- Frame meter rises around the couple's connected hands.
- Lead icon flashes above Alistair before the relevant beats.
- Timeline previews stance path: Open -> Close -> Open.

---

## 19. Production Deliverables

### 19.1 Prototype Deliverables

The first playable prototype should prove:

- Portrait card UI.
- 8-beat phrase construction.
- Base + Modifier layering.
- Flow generation and spending.
- Stance legality.
- One lead pattern.
- One Frame check.
- One cinematic phrase replay.
- One manor restoration moment.

### 19.2 Hackathon Deliverables

Recommended hackathon package:

1. Visual concept pack:
   - Portrait UI.
   - Day/Night/Dawn screens.
   - Base + Modifier card slotting.
   - Restored vs cursed room comparison.
   - Cel-shaded Alistair and protagonist.

2. Economy spreadsheet:
   - Lumen generated per night.
   - Room restoration costs.
   - Card merge costs.
   - Lumen conversion example.
   - Early progression pacing.

3. Player journey map:
   - Days 1-7.
   - First three days in detail.
   - Deck-size ramp.
   - Mechanic unlock ramp.
   - Manor restoration beats.

4. Vertical slice:
   - One complete nightly dance.
   - Two or three phrases.
   - One lead pattern.
   - One Frame check.
   - One cinematic replay.
   - One visible Dawn restoration.

---

## 20. Open Design Questions

These questions should be resolved during prototyping.

1. When should the full game expand beyond the MVP's three-phrase performance?
2. Should Flow always reset each phrase, or can rare cards carry small Flow between phrases?
3. Should Frame always reset each phrase, or can outfit stats provide persistent Starting Frame?
4. How many cards should a player draw each phrase in the full 20-card format?
5. Should the player discard unplayed cards after each phrase or keep some between phrases?
6. How much randomness is acceptable in a cozy romance simulation?
7. Should Alistair's lead be fully visible, partially visible, or relationship-dependent?
8. How explicit should the romance become while staying mobile-store friendly?
9. How much real Bachata terminology should the card names use versus gothic fantasy naming?

---

## 21. Recommended MVP Scope

The MVP should be small but representative.

### MVP Systems

- One character pair: protagonist and Alistair.
- One room: Grand Ballroom.
- One restoration upgrade: thorns cleared from dance floor.
- One song.
- Three playable phrases.
- 12-card starter collection.
- 8-card active tutorial deck.
- Card draw and hand UI.
- Base + Modifier card play.
- Flow.
- Open and Close stances.
- One lead pattern: Close Invitation.
- One Frame check: Sudden Dip.
- One Stumble state.
- One cinematic phrase replay.

### MVP Card Set

- Basic Side-Step.
- Basic Step.
- Madrid Step.
- Step Into Close.
- Close Sway.
- Sensual Body Roll.
- Arm Frame.
- Grounded Posture.
- Head Accent.
- Eye Contact.
- Breath Sync.
- The Sensual Dip.

### MVP Success Criteria

The MVP succeeds if a player can:

- Understand that they are constructing dance phrases.
- Build a legal 8-beat routine.
- See their cards become a dance animation.
- Understand why a card is illegal.
- Match Alistair's lead.
- Survive or fail a dip based on Frame.
- Earn Lumen.
- Restore part of the ballroom.
- Want to play the next night.

---

## 22. Glossary

| Term | Meaning |
| --- | --- |
| Active Deck | The selected cards brought into a nightly performance. Full format is 20 cards. |
| Binder | The player's persistent card collection. |
| Beat | Timing unit for phrase construction. |
| Bond / Intimacy | Relationship progression currency with Alistair. |
| Dawn | Post-performance restoration phase. |
| Flow | Phrase-local combo resource generated by Footwork and spent on modifiers. |
| Frame | Phrase-local support resource used against dips and demanding leads. |
| Lumen Essence | Main restoration currency earned from dance performance. |
| Nightly Performance | One dance/song. Not a roguelike run. |
| Phrase | One 8-beat playable turn. |
| Poise | Nightly mistake buffer. Reaching 0 can end the song early. |
| Rehearsal Grid | Daytime card rehearsal, merge, and refinement interface. |
| Stance | Couple position such as Open, Close, or Wrap. |
| Stumble | Failure event that breaks score and reduces Poise. |
| Syncopation | Later Grand Library unlock for 0-Beat flourish cards tied to specific anchors. |
| Lead Pattern | Alistair's telegraphed dance invitation or support requirement. |
