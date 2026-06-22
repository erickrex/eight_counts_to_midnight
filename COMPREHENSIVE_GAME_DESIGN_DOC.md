# Dancing with Dracula: Crimson Manor

Comprehensive Game Design Document

Version: 0.1  
Platform: Mobile, iOS and Android  
Orientation: Portrait  
Genre: Simulation and Management / Dance-Life Sim / Persistent Romance Card Game  
Core Theme: Gothic romance, Bachata skill growth, style management, castle lifestyle progression, dance card play  

---

## 1. Design Canon

This document is the current source of truth for the Bachata deckbuilder mobile game.

The most important design constraint is that this is **not a roguelike**. The game borrows pacing ideas from tactical card games, but it does not use permadeath, disposable decks, random map runs, or run-based progression resets.

The game uses short card-driven dance decisions inside each nightly performance, but all meaningful progression is persistent. Dance skill, card mastery, outfits, accessories, social bonds, unlocked castle facilities, and visual identity carry forward permanently.

### Canon Rules

- The player owns a persistent card collection.
- The standard active dance deck is 20 cards.
- Early tutorial days use restricted starter decks before the full 20-card format unlocks.
- Each night is a performance, not a run.
- Each performance contains several 8-beat phrases.
- Each phrase must resolve to exactly 8 Beats once full play is unlocked.
- There is no permadeath.
- Failure causes a stumble, score loss, Poise loss, reduced rewards, or early song end.
- The player is a mortal follower improving her technique, style, confidence, and relationship with Alistair.
- Lumen Essence funds personal growth, wardrobe pieces, rehearsal upgrades, and castle facility improvements.
- Castle spaces support the player's growth; they are training, styling, music, relationship, and performance facilities rather than the sole goal.
- Relationship progression with Alistair unlocks dialogue, lore, passive buffs, temporary performance bonuses, and more demanding lead patterns.

---

## 2. Executive Summary

### Working Title

**Dancing with Dracula: Crimson Manor**

### Logline

A gothic dance-life simulation where a mortal follower trains by day, refines her style, improves a haunted castle's performance spaces, and dances Bachata by night with a brooding Vampire Lord.

### High Concept

The player arrives at Crimson Manor as a mortal follower: inexperienced, underdressed for the supernatural ballroom, and drawn into Alistair's curse through the first dance. The castle is a gothic performance hub where each space helps her become a better partner: the Mirror Hall trains technique, the Wardrobe Atelier shapes style, the Music Room unlocks songs, the Conservatory provides sensual styling materials, and the Grand Ballroom hosts the nightly performance.

The moment-to-moment gameplay is a portrait-mode dance card engine built around short 8-count Bachata phrases. Players combine Footwork, Transition, Styling, and Support cards to build musically accurate dance routines. At the end of each phrase, the UI disappears and the characters perform the chosen movement as a cinematic 3D sequence.

The long-term gameplay is a persistent simulation loop: train the mortal follower, rehearse and merge cards, assemble outfits, improve castle facilities, deepen the bond with Alistair, and return each night as a more confident and expressive dancer.

### Target Audience

- Women 18-35 interested in romance, cozy games, fashion, self-improvement arcs, narrative progression, and character bonding.
- Cozy simulation players who enjoy visible growth, daily routines, style collection, and character progression.
- Tactical CCG and deck-construction players who enjoy combo optimization.
- Mobile players who want short but satisfying sessions.

### Hackathon / Pitch Positioning

The game fits a Simulation and Management category by making daily growth planning, skill training, wardrobe management, relationship management, deck collection, and castle facility upgrades the main persistent structure. It replaces simple tycoon tapping with a stylish dance-life routine wrapped in high-end gothic romance visuals.

The loop is:

```text
Train and style by day -> Perform by night -> Grow at dawn -> Unlock tomorrow
```

---

## 3. Design Pillars

### Pillar 1: Mortal Follower Growth Simulation

The player is not just completing isolated dances. She is managing the growth of a mortal follower: technique, confidence, style, deck mastery, social bond, and access to supernatural castle facilities all persist.

### Pillar 2: Bachata as Tactical Language

Every dance phrase is built from real-feeling Bachata concepts: 8-count timing, stance changes, frame, lead/follow connection, sensual styling, and musical accents.

### Pillar 3: Easy to Read, Hard to Master

The UI treats each turn as an 8-beat musical phrase. Beginners can play obvious legal cards. Advanced players optimize Flow, Frame, stance chains, multipliers, and Alistair's lead patterns.

### Pillar 4: Visible Self and Space Transformation

Every major improvement should be visible on either the player character or the castle. Her posture sharpens, outfits become more elaborate, accessories change her silhouette, and castle spaces become more useful, beautiful, and performance-ready over time.

### Pillar 5: Cinematic Payoff

The player must see the routine they built. Cards are not abstract effects; they become animated partner-dance phrases. The game regularly rewards good play with camera movement, close-ups, and visual flourishes.

### Pillar 6: Fashion and Function

Outfits are not only cosmetics. Dresses, gloves, shoes, jewelry, hairstyles, and perfumes affect starting Flow, Frame, Styling costs, Bond gains, and performance scoring. Style is a management layer and a visual reward.

### Pillar 7: One-Handed Mobile First

The game is built for portrait play. The top half of the screen presents the 3D dance, the player's styling, Alistair, and the castle environment. The bottom half contains the hand, timeline, and drag targets.

---

## 4. Game Structure

## 4.1 The Follower Growth Loop

The game follows a continuous in-game calendar.

### Day: Train, Style, and Prepare

During the day, the player navigates Crimson Manor as a living performance hub and prepares the mortal follower for the night. To make the simulation layer explicit, each day gives the player **2 Day Action slots**.

Each day, choose 2 of 5:

- **Train technique:** Practice posture, timing, turns, musicality, or Frame in a castle facility. Grants skill progress or a temporary performance boon.
- **Rehearse cards:** Use the Rehearsal Grid to merge duplicates, refine the active deck, and prepare a specific dance plan.
- **Style the follower:** Visit the Wardrobe Atelier to craft, equip, or enhance outfits, shoes, gloves, accessories, perfumes, and hairstyles.
- **Spend time with Alistair:** Trigger dialogue, gain Bond, reveal lore, or learn how to read one of his lead patterns.
- **Improve a castle space:** Spend Lumen Essence and materials to improve a facility such as the Ballroom, Mirror Hall, Music Room, Atelier, Library, or Conservatory.

Free supporting actions, such as reviewing the Binder, inspecting unlocked spaces, or previewing outfits, can happen without spending a Day Action slot.

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

### Dawn: Reflect and Grow

Dawn is the growth payout. The player sees what the night's performance earned and chooses how to convert it into long-term improvement.

Dawn actions include:

- Spend Lumen Essence on training, wardrobe work, card rehearsal, or castle facility improvements.
- Unlock skills, outfits, facilities, and systems.
- Gain access to new card pools.
- Improve the visual identity of the follower and the castle.
- Resolve narrative beats from the night's dance.
- Bank relationship progress.
- Preview the next day's objectives.

The dawn phase is the emotional release. The player sees proof that the dance mattered because the follower looks, moves, and prepares differently tomorrow.

---

## 5. Persistent Progression

The game has several interconnected progression tracks.

### 5.1 Mortal Follower Skill Growth

The main long-term fantasy is that the protagonist becomes a better dancer and a more captivating partner. Her growth is not abstract; it changes what cards are viable, how much Flow or Frame she can access, how she looks in animation, and how confidently she responds to Alistair.

Skill tracks:

| Skill Track | Managed Through | Gameplay Impact |
| --- | --- | --- |
| Technique | Mirror Hall drills, Rehearsal Grid practice | Unlocks cleaner Footwork, better draw consistency, and fewer illegal-card mistakes |
| Musicality | Music Room practice, song study | Improves Flow generation, timing bonuses, and Beat 4/8 accent rewards |
| Frame | Partner drills, Support practice, shoes/gloves | Increases Starting Frame or improves dip support checks |
| Styling | Wardrobe Atelier, Conservatory materials | Reduces Styling costs, unlocks visual flourishes, improves style scoring |
| Confidence | Successful performances, Bond scenes, outfits | Raises Poise and reduces penalties from Stumbles |
| Connection | Time with Alistair, lead-pattern study | Reveals lead patterns earlier and improves Perfect Connection rewards |

Skill growth should be visible in animation. Early movement feels careful and small. Later movement is smoother, more grounded, and more expressive.

### 5.2 Card Collection and Rehearsal

The player owns a persistent collection called the Binder. Cards are not discarded between nights. They can be earned, found, upgraded, merged, and slotted into the active dance deck.

The standard active deck contains exactly 20 cards once fully unlocked. Tutorial days use smaller controlled decks to avoid overwhelming new players.

Suggested deck-size onboarding:

| Day / Milestone | Active Deck Format | Purpose |
| --- | ---: | --- |
| Day 1 | Guided 8-card starter deck | Teach Open stance, Beats, Flow, and simple Styling |
| Day 2 | 12-card deck | Teach stance transition, Alistair's lead patterns, and merging |
| Day 3 | 16-card deck | Teach Frame, Poise, and Support planning |
| Day 7 | Full 20-card deck | Full deck construction unlocked |

### 5.3 Merge Progression

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

### 5.4 Castle Facilities

Crimson Manor is no longer positioned as the main objective by itself. It is a gothic training, styling, relationship, and performance hub. Improving a castle space should feel like unlocking a new lifestyle facility for the mortal follower.

Each facility provides:

- A visible environmental transformation.
- A new training, style, music, relationship, or card function.
- A passive facility bonus.
- A narrative beat.
- A reason to return to the day phase.

Example facilities:

| Facility | Visual Improvement | System Role |
| --- | --- | --- |
| Grand Ballroom | Floor clears, chandeliers relight, stage marks appear | Nightly performances, song length, Lumen yield |
| Mirror Hall | Broken mirrors reform into practice panels | Technique drills, replay review, Confidence growth |
| Wardrobe Atelier | Dress forms, jewelry trays, and shoe racks return | Outfits, accessories, cosmetics with stats |
| Music Room | Instruments retune themselves | Songs, rhythm modifiers, Musicality training |
| Gothic Conservatory | Dead vines bloom into midnight roses | Perfumes, flowers, sensual Styling materials |
| Grand Library | Shelves awaken, annotated dance texts appear | Advanced Footwork, later flourish tags, lead-pattern study |
| Stained-Glass Gallery | Moonlight returns, color fills the castle | Mood bonuses, romantic scenes, visual identity |

### 5.5 Relationship Progression

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
| Lumen Essence | Nightly score and facility bonuses | Train skills, improve facilities, unlock progression nodes |
| Intimacy / Bond | Dialogue, gifts, matching Alistair's lead, story milestones | Unlock relationship scenes and social buffs |
| Style Materials | Atelier, Conservatory, performance rewards | Craft outfits, accessories, perfumes, hairstyles |
| Card Shards / Duplicates | Facility searches, rehearsal rewards, dance rewards | Merge and improve cards |

### 5.6 Wardrobe, Styling, and Equipment

Outfits are not just cosmetics. Gowns, shoes, gloves, jewelry, hairstyles, and perfumes alter starting conditions and encourage different play styles. The Wardrobe Atelier is one of the clearest ways to make the game read as a lifestyle management sim.

Example wardrobe effects:

- +1 Starting Flow.
- +5 Starting Frame.
- +10% Lumen from Close stance phrases.
- First Stumble each night costs no Poise.
- Styling cards cost 1 less Flow once per phrase.
- Wrap cards score higher but Transition cards cost more.
- Eye Contact grants extra Bond once per performance.
- Beat 4/8 accents trigger extra cloth or hair animation.

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
- Some outfits, relationship buffs, and facility improvements can grant Starting Flow.
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
Facility Unlock Source
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

The scoring model should be easy to explain. The pitch only needs one formula that connects dance performance to follower growth.

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

### 10.2 Lumen Essence and Growth Rewards

At dawn, phrase scores convert into Lumen Essence and growth rewards. Lumen is the main flexible currency for training, facility improvements, wardrobe work, and card rehearsal.

```text
Lumen Essence = Floor(Total Performance Score / Essence Divisor) + Objective Bonuses
```

Objective bonuses can include:

- First time matching a new lead pattern.
- No Stumbles.
- Perfect Support on a dip.
- Completing a skill, style, or facility objective.
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
- No reset of skills, wardrobe, cards, relationship, or castle facilities.

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
- The protagonist's look evolves from simple mortal visitor to confident supernatural dance partner.
- Castle facilities become progressively richer, warmer, and more useful.

The game should avoid generic dark fantasy mud. Crimson Manor is cursed, but the player's growth should bring color, glow, romance, and personal style back into the space.

### 12.2 Screen Layout

Portrait layout:

```text
Top 50%: 3D stage, dancers, castle facility, outfit silhouette, lead telegraphs
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
- Warm musical swell when the player unlocks a skill, outfit, or facility improvement.
- Distinct audio stingers for Perfect Connection, Stumble, and Perfect Support.

The player should learn timing partly by ear.

---

## 14. Narrative Design

### 14.1 Premise

The protagonist arrives at Crimson Manor as a mortal outsider with a personal connection to dance but limited confidence as a follower. In the Grand Ballroom she discovers Alistair, a Vampire Lord frozen in stone by a centuries-old curse. The castle is dormant and silent, but its spaces still remember music, style, etiquette, and supernatural performance.

The curse can only be weakened through dance, but the emotional arc is not just "fix the castle." Each day, the protagonist trains, rehearses, styles herself, studies Alistair's lead, and improves the castle facilities that support her growth. Each night, she dances with Alistair, drawing Lumen Essence from rhythm, trust, and connection. Each dawn, that essence becomes visible progress in her skills, wardrobe, relationship, and performance spaces.

### 14.2 Player Character

The protagonist is the mortal follower. She is not a passive observer or a blank avatar. She chooses how to train, how to dress, how to rehearse, how much to trust Alistair, and what kind of dance partner she wants to become.

Possible framing:

- A dancer who has inherited the manor.
- A mortal follower drawn to a cursed ballroom after losing confidence in dance.
- A musician or choreographer researching a forgotten ballroom.
- A descendant of the person who sealed Alistair.

### 14.3 Alistair

Alistair is the Vampire Lord of Crimson Manor.

Character identity:

- Brooding but not cruel.
- Dangerous but controlled.
- Guarded early, increasingly vulnerable.
- Expresses emotion through dance before words.
- His power is tied to the castle's music, memory, and nightly performances.
- His lead patterns become more complex as his strength returns.

### 14.4 Romance Arc

The romance should escalate through trust and embodied connection.

Arc:

1. Contact: touch the statue, first dance.
2. Speech: Alistair can speak but remains guarded.
3. Training: he teaches through lead patterns before he fully explains himself.
4. Trust: he begins telegraphing more honestly.
5. Vulnerability: VN scenes reveal curse history.
6. Partnership: advanced dances require mutual trust.
7. Choice: the player decides how to resolve the curse.

---

## 15. First Three Days Journey Map

This section defines the onboarding sequence for the new simulation framing: the player is managing a mortal follower's growth through training, style, rehearsal, relationship, and castle facilities.

### Day 1: The Awakening and the First 8-Count

Objective:

- Introduce the mortal follower fantasy.
- Introduce the Day/Night/Dawn structure.
- Introduce Open stance, Beats, simple Flow, and one Styling modifier.
- Show the first visible improvement to both the follower and the Ballroom.

#### Day Narrative

The protagonist arrives at Crimson Manor wearing practical mortal clothes, not a ballroom outfit. The Grand Ballroom is dark, thorned, and silent. In the center stands Alistair, frozen in stone.

She touches his hand. Music stirs under the floor. The first dance is not a polished performance; it is a supernatural lesson.

#### Day Management

Day 1 is mostly guided. The player receives an 8-card starter deck and sees the first growth categories, but does not yet choose freely.

Guided setup:

- Active deck: 8 cards.
- Stance: Open only.
- Facility available: Grand Ballroom.
- Outfit: simple mortal dress.
- Skill state: Beginner Technique, low Confidence.

Example cards:

- Basic Side-Step.
- Basic Step.
- Head Accent.
- Breath Sync.

#### Night Performance

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
- Her posture is careful but improving.
- The Head Accent lands on Beat 8.
- Alistair's stone shell cracks.

#### Dawn Growth

The player earns first Lumen Essence. The game introduces the growth screen.

First guaranteed growth:

- Grand Ballroom floor clears enough to become a usable practice space.
- The protagonist gains **Beginner Confidence I**.
- Alistair breaks fully out of stone and can speak.

The emotional message is: the dance changed her and woke the castle.

### Day 2: Training, Style, and the Rehearsal Grid

Objective:

- Introduce limited Day Action slots.
- Introduce Rehearsal Grid merging.
- Introduce first technique training.
- Introduce Close stance and Alistair's lead pattern.
- Show that the player's preparation affects the night's dance.

#### Day Narrative

Alistair can speak, but he is guarded. He tells the protagonist that the castle responds to rhythm, but she cannot rely on instinct alone. She needs technique, confidence, and the right preparation.

#### Day Management

The player gets 2 Day Action slots for the first time.

Recommended guided choices:

1. **Train technique:** The player practices in front of a cracked mirror panel. Reward: +1 Starting Flow for the first phrase.
2. **Rehearse cards:** The player finds duplicate Basic Step cards and uses the Rehearsal Grid.

The Rehearsal Grid unlocks:

```text
3 Basic Step cards -> 1 Foil Basic Step
```

Day 2 deck:

- 12-card active deck.
- Open and Close stance cards.
- First Transition card: Step Into Close.
- First lead-pattern tutorial.

#### Night Performance

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
Starting Preparation: +1 Flow from Technique Training

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

- Because the player trained and matched Alistair's lead, the Tornado Camera triggers.
- The protagonist's animation looks slightly more grounded than Day 1.
- The camera slows into a close-up on Beat 8.

#### Dawn Growth

The player spends Lumen to choose one early growth path:

- **Mirror Hall Level 1:** unlocks repeatable Technique drills.
- **Wardrobe Atelier Level 1:** unlocks first outfit piece with a small stat bonus.

The recommended guided unlock is **Mirror Hall Level 1**, because it reinforces the new self-improvement loop.

Unlocks:

- Mirror Hall Level 1.
- Technique drills.
- Lead preview for future dances.
- Slight score bonus for Perfect Connection.

### Day 3: Wardrobe, Frame, and Support

Objective:

- Introduce wardrobe as both visual identity and stats.
- Introduce Frame.
- Introduce Poise loss and Stumble.
- Introduce a demanding lead pattern.
- Introduce Bond as a preparation path.

#### Day Narrative

Alistair warns that tonight's rhythm will ask for trust. He cannot simply tell the protagonist what to do; she has to learn how to hold her own frame. The Wardrobe Atelier opens, revealing gowns, gloves, shoes, and jewelry preserved by the castle's magic.

#### Day Management

The player chooses 2 Day Actions:

1. **Style the follower:** Equip the first training gown or gloves.
2. **Spend time with Alistair:** Unlock a short VN scene about trust and following.

Example wardrobe reward:

```text
Moon Practice Gloves
Effect: +5 Starting Frame
Visual: Pale gloves with faint silver thread
```

Dialogue reward example:

```text
Choice: Trust his lead
Reward: +1 Bond and +1 Starting Flow for tonight's first phrase
```

Day 3 deck:

- 16-card active deck.
- Open and Close stance cards.
- Basic Support cards.
- First Frame check response.

#### Night Performance

Lead Pattern:

```text
Sudden Dip
Timing: Beat 7
Requirement: Be in Close and have 20 Frame before Beat 7
Success: Perfect Support
Miss: Stumble, lose Poise, break multiplier
```

Tutorial phrase:

```text
Start Stance: Open
Starting Preparation: +5 Frame from gloves, +1 Flow from Bond scene

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
The Sensual Dip
Requires 20 Frame

Result:
Frame total reaches 30
Perfect Support triggers
```

Animation:

- The protagonist supports the dip instead of stumbling.
- The gloves catch moonlight during the close-up.
- Alistair reacts with visible surprise: she is becoming a true partner.

#### Dawn Growth

The player earns Lumen, Bond, and Style Materials. The castle offers multiple growth paths, making the management layer explicit.

Choices:

- Improve Mirror Hall for better Technique drills.
- Improve Wardrobe Atelier for stronger outfit crafting.
- Unlock Grand Library for advanced Footwork study.

Recommended guided unlock:

- **Wardrobe Atelier Level 1**, if not already chosen.
- If already chosen, **Grand Library Level 1**.

Unlocks:

- Outfit enhancement.
- Advanced Footwork card pool.
- First optional Library flourish cards begin appearing later.

---

## 16. Week One Progression Outline

Only the first three days are fully specified above, but the broader first-week shape should be:

| Day | Main Unlock | Player Learning |
| --- | --- | --- |
| Day 1 | Grand Ballroom practice space | Beats, Flow, Open stance, first Confidence growth |
| Day 2 | Mirror Hall | Technique training, Close stance, lead patterns, Rehearsal Grid |
| Day 3 | Wardrobe Atelier | Outfit stats, Frame, Poise, Support planning |
| Day 4 | Music Room | Musicality training, new song mood, Beat 4/8 accent rewards |
| Day 5 | Gothic Conservatory | Perfumes, flowers, sensual Styling materials |
| Day 6 | Grand Library | Advanced Footwork study, optional flourish tags |
| Day 7 | Full 20-card deck | Complete deck construction format and first self-directed day plan |

---

## 17. Economy and Balance Targets

### 17.1 Session Length

| Activity | Target Length |
| --- | ---: |
| Day growth planning | 1-3 minutes |
| Night performance | Three short phrases for MVP |
| Dawn growth allocation | 30-90 seconds |
| Full daily loop | 5-10 minutes |

### 17.2 Early Reward Cadence

The first three days should each provide:

- One new mechanic.
- One visible character or facility improvement.
- One emotional beat with Alistair.
- One deck or card improvement.
- One reason to return tomorrow.

### 17.3 Growth Costs

Early growth costs should be affordable enough to guarantee visible progress.

Suggested early costs:

| Growth Item | Cost | Notes |
| --- | ---: | --- |
| Clear Ballroom Practice Space | 10 Lumen | Guaranteed after Day 1 |
| Mirror Hall Level 1 | 25 Lumen | Guided Day 2 unlock |
| Moon Practice Gloves | 25 Lumen + 1 Style Material | Guided Day 3 wardrobe reward |
| Wardrobe Atelier Level 1 | 40 Lumen | Early style-management unlock |
| Grand Library Level 1 | 50 Lumen | Advanced card study unlock |
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
- One day-action choice.
- One skill or wardrobe improvement.
- One castle facility improvement.

### 19.2 Hackathon Deliverables

Recommended hackathon package:

1. Visual concept pack:
   - Portrait UI.
   - Day/Night/Dawn screens.
   - Base + Modifier card slotting.
   - Mortal follower before/after styling comparison.
   - Castle facility improvement comparison.
   - Cel-shaded Alistair and protagonist.

2. Economy spreadsheet:
   - Lumen generated per night.
   - Skill, wardrobe, and facility costs.
   - Card merge costs.
   - Lumen conversion example.
   - Early progression pacing.

3. Player journey map:
   - Days 1-7.
   - First three days in detail.
   - Deck-size ramp.
   - Mechanic unlock ramp.
   - Skill, style, Bond, and facility growth beats.

4. Vertical slice:
   - One complete nightly dance.
   - Two or three phrases.
   - One lead pattern.
   - One Frame check.
   - One cinematic replay.
   - One visible Dawn growth choice.

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
10. How many day-action choices should be available before the player feels overloaded?
11. How much of wardrobe progression should be stats, cosmetics, or both?

---

## 21. Recommended MVP Scope

The MVP should be small but representative.

### MVP Systems

- One character pair: protagonist and Alistair.
- One facility: Grand Ballroom.
- One visible facility improvement: practice space cleared.
- One skill improvement: Beginner Confidence I or Technique I.
- One wardrobe item: Moon Practice Gloves or equivalent.
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
- Improve the mortal follower or a castle facility.
- Want to play the next night.

---

## 22. Glossary

| Term | Meaning |
| --- | --- |
| Active Deck | The selected cards brought into a nightly performance. Full format is 20 cards. |
| Binder | The player's persistent card collection. |
| Beat | Timing unit for phrase construction. |
| Bond / Intimacy | Relationship progression currency with Alistair. |
| Castle Facility | A usable castle space that supports training, style, music, relationship, or performance. |
| Confidence | Persistent or temporary growth track that improves Poise and expressive performance. |
| Dawn | Post-performance growth allocation phase. |
| Day Action | Limited daytime choice spent on training, rehearsal, styling, bonding, or facility improvement. |
| Flow | Phrase-local combo resource generated by Footwork and spent on modifiers. |
| Frame | Phrase-local support resource used against dips and demanding leads. |
| Lumen Essence | Main flexible growth currency earned from dance performance. |
| Mirror Hall | Castle facility for Technique drills, replay reflection, and Confidence growth. |
| Nightly Performance | One dance/song. Not a roguelike run. |
| Phrase | One 8-beat playable turn. |
| Poise | Nightly mistake buffer. Reaching 0 can end the song early. |
| Rehearsal Grid | Daytime card rehearsal, merge, and refinement interface. |
| Style Materials | Wardrobe and cosmetic crafting resources earned from facilities and performances. |
| Stance | Couple position such as Open, Close, or Wrap. |
| Stumble | Failure event that breaks score and reduces Poise. |
| Syncopation | Later Grand Library unlock for 0-Beat flourish cards tied to specific anchors. |
| Lead Pattern | Alistair's telegraphed dance invitation or support requirement. |
| Wardrobe Atelier | Castle facility for outfits, accessories, hairstyles, perfumes, and style-based stats. |
