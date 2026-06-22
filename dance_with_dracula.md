# Dancing with Dracula: Crimson Manor

Hackathon-Facing Game Design Document

Category: Simulation and Management  
Platform: Mobile, iOS and Android  
Orientation: Portrait  
Genre: Gothic romance dance-life sim / persistent card game  
Core loop: Prepare by day, dance by night, transform at dawn  

---

## 1. High Concept

### Logline

A gothic romance dance-life sim where a mortal follower trains, styles herself, restores a haunted manor, and performs cinematic Bachata phrases with a cursed vampire lord.

### Pitch

The player arrives at Crimson Manor as an inexperienced mortal dancer. The castle is silent, its ballroom dark, and its master, Alistair, is bound by a supernatural curse. Dance is the only language the manor still answers.

By day, the player chooses how to prepare: train technique, rehearse cards, improve wardrobe, restore manor spaces, or spend time with Alistair. By night, the player builds short 8-beat Bachata phrases from cards. At dawn, performance rewards become visible growth: sharper technique, stronger cards, better outfits, warmer rooms, and a deeper bond with Alistair.

The game is not a roguelike. Progress is persistent. Cards, wardrobe, skills, relationship scenes, and manor upgrades all carry forward.

### Core Fantasy

The player becomes a more confident, stylish, emotionally connected dance partner. Every system should support that transformation.

```text
Day: choose two preparations
Night: build three 8-beat dance phrases
Dawn: spend rewards on visible growth
```

---

## 2. Target Audience

- Women 18-35 interested in romance, fashion, supernatural drama, cozy progression, and character bonding.
- Mobile players who enjoy short daily loops with visible long-term growth.
- Deck-construction players who like tactical sequencing without harsh roguelike resets.
- Style and life-sim players who want outfits to affect gameplay, animation, and relationship tone.

The pitch combines proven audience signals from romance mobile games, fashion progression games, and management deckbuilders, but the Bachata partner-dance structure gives it a distinct identity.

---

## 3. Design Pillars

### Mortal Growth, Not Combat

The protagonist is not defeating enemies. She is learning posture, timing, trust, style, and musical expression. Her progress is visible in animation, wardrobe, confidence, and the restored manor.

### Bachata as Tactical Language

Cards represent real dance intentions: steps, transitions, styling, support, frame, and connection. The player is not playing abstract attacks. She is building a phrase that becomes an animated partner dance.

### Fashion With Function

Wardrobe pieces change how the player dances. Gloves improve Frame, shoes stabilize transitions, gowns create Styling bonuses, jewelry affects Bond gain, and perfume can add one-time Flow or romance effects.

### Intimate 3D Romance

Alistair is not only a story reward. He is the dance partner, the lead-pattern source, and the emotional pressure in each performance. Bond changes dialogue, camera moments, lead readability, and the kinds of dance invitations he offers.

### One-Handed Mobile First

The game is built for portrait play. The top half shows dancers and lead cues. The lower half shows cards, the phrase timeline, and drag targets. The player should be able to complete a daily loop in 5-10 minutes.

---

## 4. Core Game Loop

### Day: Train, Style, Rehearse

Each day gives the player 2 Day Action slots. The limit creates meaningful management tradeoffs.

| Day Action | Purpose | Example Reward |
| --- | --- | --- |
| Train Technique | Improve rhythm, posture, or musicality | +1 Starting Flow tonight |
| Rehearse Cards | Merge duplicates or tune the active deck | 3 Basic Step cards -> 1 Foil Basic Step |
| Style the Follower | Equip or enhance wardrobe pieces | Moon Practice Gloves: +5 Starting Frame |
| Spend Time with Alistair | Build Bond and learn his lead style | Lead preview or +1 Starting Flow |
| Improve the Manor | Restore a facility that supports growth | Mirror Hall unlocks repeatable drills |

Free actions, such as inspecting the card binder or previewing outfits, do not cost a Day Action.

### Night: Build the Dance

Each night is one short performance. For the MVP, a performance contains three playable 8-beat phrases.

During each phrase, the player:

- Draws cards from the active deck.
- Builds exactly 8 Beats of movement.
- Reads Alistair's lead pattern.
- Uses Footwork and Transition cards to create a legal stance path.
- Generates Flow from movement.
- Spends Flow on Styling and Support.
- Builds Frame to survive demanding leads.
- Locks in the phrase and watches it become a cinematic dance moment.

### Dawn: Transform

At dawn, the player converts performance results into long-term progress.

Rewards include:

- Lumen Essence for training, wardrobe, card rehearsal, and manor upgrades.
- Bond progress with Alistair.
- Style Materials for clothing, gloves, shoes, jewelry, hairstyles, and perfume.
- Card duplicates or upgrade materials.
- Visible changes to the protagonist or manor.

Dawn is the emotional proof that the dance mattered.

---

## 5. Dance Card System

### Phrase Structure

Every full phrase is an 8-count Bachata phrase.

```text
Bar A: Beats 1-4
Bar B: Beats 5-8
```

The UI uses two readable bars instead of eight cramped beat slots. Base movement cards occupy the bars. Modifier cards attach vertically to base cards.

### Card Types

| Type | Beat Cost | Flow Cost | Role |
| --- | ---: | ---: | --- |
| Footwork | Usually 4 | 0 | Base movement, Flow generation, score foundation |
| Transition | Usually 2 | 0 | Change stance and prepare chains |
| Styling | 0 | 1-3 | Add flair, points, multipliers, animation layers |
| Support | 0 | 1-3 | Build Frame, protect Poise, match Alistair's lead |

### Core Resources

| Resource | Meaning | How It Works |
| --- | --- | --- |
| Beats | Musical timing limit | Each phrase must total exactly 8 Beats |
| Flow | Expressive momentum | Generated by movement, spent on Styling and Support |
| Frame | Posture and partner support | Needed for dips and demanding leads |
| Poise | Mistake buffer | Lost on Stumbles; reaching 0 can end the song early |
| Bond | Relationship trust | Unlocks scenes, buffs, lead readability, and unique cards |

### Stances

Stance is the main sequencing puzzle.

| Stance | Gameplay Identity |
| --- | --- |
| Open | Safe, mobile, beginner-friendly |
| Close | Required for sensual moves and higher connection bonuses |
| Wrap | Higher scoring, but restrictive and riskier |
| Shadow | Supernatural intimacy within Alistair's aura; high Lumen, requires Bond |

Shadow is the vampire-specific stance. The follower moves into Alistair's supernatural silhouette, partially obscured by his dark presence. Shadow generates bonus Lumen and unlocks unique vampire-themed moves, but entering Shadow safely requires minimum Bond. Without enough trust, Shadow cards risk Poise loss. Shadow exits only to Close or Open.

If a card does not match the current stance, it greys out and explains why.

### Example Phrase

Alistair's lead:

```text
Close Invitation
Timing: Beats 5-8
Response: Enter Close before Beat 5
Reward: Perfect Connection x2
```

Player phrase:

```text
Start Stance: Open

Bar A, Beats 1-4:
Madrid Step
Open -> Open
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
8 Beats complete, lead matched, Perfect Connection x2
```

The UI fades after lock-in. The dancers perform the phrase, the camera tightens on Beat 8, and Alistair reacts to the improved connection.

### Example Phrase: Shadow Stance

Alistair's lead:

```text
Dark Embrace
Timing: Beats 5-8
Response: Enter Shadow before Beat 5
Requirement: Bond 3+
Reward: Shadow Resonance x3 Lumen
```

Player phrase:

```text
Start Stance: Close
Bond: 4 (requirement met)

Bar A, Beats 1-4:
Close Sway
Close -> Close
Generates 1 Flow

Bar B, Beats 5-6:
Fade Into Shadow
Close -> Shadow
Generates 2 Flow, +15 Frame

Bar B, Beats 7-8:
Eternal Waltz
Shadow -> Shadow
+50% Lumen this phrase

Modifier:
Vampire's Whisper attaches to Eternal Waltz
Costs 2 Flow

Result:
8 Beats complete, Dark Embrace matched, Shadow Resonance x3 Lumen
```

During the cinematic replay, the protagonist's silhouette merges with Alistair's shadow. Her outline glows faintly crimson as they move as one form. The camera pulls back to show a single elegant shadow dancing across the ballroom floor.

---

## 6. Example Cards

The pitch only needs enough cards to prove the system.

| Card | Type | Cost | Stance | Purpose |
| --- | --- | --- | --- | --- |
| Basic Side-Step | Footwork | 4 Beats | Any -> Same | Beginner base move, +1 Flow, 1 Styling slot |
| Madrid Step | Footwork | 4 Beats | Open -> Open | Stronger movement, +2 Flow, 2 Styling slots |
| Step Into Close | Transition | 2 Beats | Open -> Close | Teaches stance change, +10 Frame |
| Close Sway | Footwork | 2 Beats | Close -> Close | Stabilizes Close stance |
| Sensual Body Roll | Footwork | 4 Beats | Close -> Close | Higher scoring Close payoff |
| Head Accent | Styling | 1 Flow | Attach to Footwork | First visual flourish |
| Eye Contact | Styling | 1 Flow | Any base | Score bonus and Bond progress on lead match |
| Arm Frame | Support | 2 Flow | Any base | +10 Frame for demanding lead checks |
| Grounded Posture | Support | 1 Flow | Any base | +5 Frame, prevents minor Stumble |
| The Sensual Dip | Footwork | 4 Beats | Close -> Open | High payoff, requires 20 Frame |
| Fade Into Shadow | Transition | 2 Beats | Close -> Shadow | Enter Shadow stance, +2 Flow, +15 Frame, requires Bond 2+ |
| Eternal Waltz | Footwork | 4 Beats | Shadow -> Shadow | +50% Lumen this phrase, supernatural aura visuals |
| Shadow Step | Footwork | 4 Beats | Shadow -> Shadow | +3 Flow, high Lumen, dark silhouette effect |
| Emerge From Darkness | Transition | 2 Beats | Shadow -> Close | Exit Shadow gracefully, +1 Bond, +10 Frame |
| Vampire's Whisper | Styling | 2 Flow | Shadow base only | x2 Lumen multiplier, intimate voice line from Alistair |
| Dark Anchor | Support | 2 Flow | Shadow base only | +20 Frame, prevents Bond-gated Stumble |

---

## 7. Alistair's Lead

Alistair's lead patterns are the game's romantic pressure system. They tell the player what he is inviting, testing, or asking them to support.

| Lead Pattern | Timing | Player Response | Success | Miss |
| --- | --- | --- | --- | --- |
| Open Invitation | Beats 1-8 | Maintain rhythm in Open | Small Connection bonus | No major penalty |
| Close Invitation | Beats 5-8 | Enter Close before Beat 5 | Perfect Connection x2 | Reduced multiplier |
| Sudden Dip | Beat 7 | Be in Close and reach 20 Frame | Cinematic dip, bonus Lumen | Stumble, lose Poise |
| Sensual Phrase | Beats 5-8 | Play a Close stance move | Higher Lumen and Bond tension | Missed bonus |
| Dark Embrace | Beats 5-8 | Enter Shadow before Beat 5 | Shadow Resonance x3 Lumen | Stumble if Bond < 3 |
| Crimson Surrender | Beat 8 | End phrase in Shadow with 25+ Frame | Unique cinematic, +2 Bond | Heavy Poise loss |

Bond can make lead patterns easier to read. Early in the relationship, Alistair's lead is cold and partially hidden. As trust grows, the player sees cues earlier and unlocks more intimate partner phrases.

Shadow lead patterns only appear after Bond reaches level 2. They offer the highest Lumen rewards but punish players who rush into supernatural intimacy without building trust first.

---

## 8. Progression

### Skill Growth

The protagonist grows across six skill tracks.

| Skill | Managed Through | Gameplay Impact |
| --- | --- | --- |
| Technique | Mirror Hall drills | Cleaner Footwork, better draw consistency |
| Musicality | Music Room practice | Beat 4/8 bonuses, stronger Flow generation |
| Frame | Support practice, gloves, partner drills | Safer dips and demanding leads |
| Styling | Wardrobe Atelier | Cheaper or stronger Styling cards |
| Confidence | Successful performances and outfits | More Poise, softer Stumble penalties |
| Connection | Bond scenes and lead study | Earlier lead previews, stronger Perfect Connection |

### Wardrobe Builds

Wardrobe pieces create play styles.

| Item Type | Example Effect |
| --- | --- |
| Gloves | +5 Starting Frame |
| Shoes | First failed Transition each night costs no Poise |
| Gown | First Styling card each phrase costs 1 less Flow |
| Jewelry | Eye Contact grants extra Bond once per night |
| Perfume | Start first phrase with +1 Flow |

Outfit sets can create archetypes:

| Set | Identity |
| --- | --- |
| Moon Practice | Safe beginner Frame and Poise |
| Crimson Waltz | Close stance and Bond bonuses |
| Glass Chapel | Beat 4/8 precision and musicality |
| Black Rose | High-risk Styling multipliers |
| Midnight Veil | Shadow stance specialist; reduced Bond requirements, +Lumen in Shadow |

### Manor Facilities

The hackathon scope uses four facilities.

| Facility | Visual Change | System Role |
| --- | --- | --- |
| Grand Ballroom | Floor clears, chandeliers relight | Night performances and Lumen yield |
| Mirror Hall | Broken mirrors reform | Technique drills and replay review |
| Wardrobe Atelier | Dress forms and jewelry trays return | Outfits, accessories, and style stats |
| Music Room | Instruments retune themselves | Songs, Musicality, Beat 4/8 rewards |

Each facility should provide one visible transformation, one mechanic, and one reason to return during the day phase.

---

## 9. First Three Days

### Day 1: The Awakening

Goal: Teach the fantasy and the simplest dance phrase. Establish that dance has power in this manor.

Setup:

- Guided 8-card starter deck.
- Open stance only.
- Grand Ballroom visible but ruined.
- Protagonist wears simple mortal clothes.
- Alistair is frozen in stone at the center of the ballroom.

Narrative:

The protagonist explores the silent manor and finds Alistair's statue. When she touches his hand, faint music stirs beneath the floorboards. She realizes the manor responds to movement. This is a solo dance — she dances alone before the frozen lord, proving herself to the cursed space.

Night phrase:

```text
Basic Side-Step + Basic Side-Step + Head Accent
```

The phrase plays as a solo performance. The protagonist moves through simple Bachata footwork while Alistair's stone form watches. On Beat 8, as the Head Accent lands, cracks spider across his surface.

Payoff:

- The protagonist completes her first 8-count alone.
- Head Accent lands on Beat 8.
- Alistair's stone shell shatters. He is freed but weak.
- He speaks for the first time: the curse binds him to the manor, and only sustained dance can restore his strength.
- Dawn clears part of the Ballroom floor.
- The protagonist gains Beginner Confidence I.

### Day 2: The First Partner Dance

Goal: Teach Day Actions, rehearsal, Close stance, and lead matching. This is the first night dancing with Alistair.

Narrative:

Alistair is free but still weakened. He offers to lead the protagonist through a proper Bachata phrase — her first true partner dance. His movements are stiff, his presence cold, but the connection is real. The player now sees Alistair's lead patterns for the first time.

Day Actions:

1. Train Technique for +1 Starting Flow.
2. Rehearse cards and merge 3 Basic Step cards into 1 Foil Basic Step.

Night lead:

```text
Close Invitation: enter Close before Beat 5.
```

Payoff:

- Player uses Step Into Close.
- Perfect Connection triggers — the first moment of true synchronization.
- The first close-up camera moment plays: Alistair's hand on her waist, her hand on his shoulder.
- Alistair's movements become slightly more fluid. The curse is weakening.
- Mirror Hall Level 1 unlocks at dawn.

### Day 3: Wardrobe and Trust

Goal: Teach Frame, Poise, wardrobe stats, and a demanding lead.

Day Actions:

1. Style the follower with Moon Practice Gloves.
2. Spend time with Alistair for +1 Bond and +1 Starting Flow.

Night lead:

```text
Sudden Dip: be in Close and reach 20 Frame by Beat 7.
```

Payoff:

- Player uses Arm Frame, Grounded Posture, and Step Into Close.
- The Sensual Dip resolves safely.
- Gloves catch moonlight in the cinematic replay.
- Alistair recognizes that the protagonist is becoming a true partner.
- Wardrobe Atelier Level 1 unlocks or improves at dawn.

---

## 10. Visual and Audio Direction

### Visual Direction

Style target:

- High-end cel-shaded 3D.
- Gothic romance with moonlight, velvet, silver, candlelight, stained glass, and crimson accents.
- Elegant silhouettes and readable mobile framing.
- Expressive hands, eye contact, cloth, hair, and posture.
- The protagonist evolves from careful mortal visitor to confident supernatural dance partner.
- The manor shifts from cold and cursed to warm, luminous, and performance-ready.

The game should avoid muddy dark fantasy. The gothic setting is dangerous, but the player's growth brings color, polish, warmth, and rhythm back into the castle.

### Screen Layout

```text
Top 50%: 3D dancers, ballroom, outfit silhouette, lead telegraphs
Middle: Bar A / Bar B phrase timeline
Bottom 50%: hand, deck controls, modifier slots, lock-in button
```

Core interactions:

- Drag Footwork and Transition cards into Bar A or Bar B.
- Drag Styling and Support cards onto visible slots.
- Tap to inspect a card.
- Undo before lock-in.
- Lock in to trigger cinematic replay.

### Audio Direction

Audio must make the 8-count structure legible.

- Bachata instrumental foundation.
- Clear 1-2-3-tap, 5-6-7-tap phrasing.
- Accents on Beats 4 and 8.
- Percussion layers for multiplier growth.
- Heartbeat or vampiric ambience during demanding lead patterns.
- Warm musical swell for dawn upgrades.
- Distinct stingers for Perfect Connection, Stumble, and Perfect Support.

---

## 11. Failure and Rewards

Failure should create tension without punishing long-term progress.

### Stumble

A Stumble can happen when the player:

- Fails a required Frame check.
- Misses a dangerous lead pattern.
- Plays into the wrong stance.
- Runs out of Poise.

Effects:

- Break current multiplier.
- Lose Poise.
- Reduce phrase score.
- Alter the animation.
- End the song early if Poise reaches 0.

The player never loses owned cards, wardrobe, manor upgrades, or relationship progress.

### Rewards

Simple scoring model:

```text
Phrase Score = Card Points x Connection Multiplier
Lumen Essence = Total Performance Score + Objective Bonuses
```

Objective bonuses include:

- First time matching a lead pattern.
- No Stumbles.
- Perfect Support on a dip.
- Beat 4/8 accent success.
- High remaining Poise.

---

## 12. MVP Scope

The MVP should prove one complete daily loop.

### Included

- One character pair: protagonist and Alistair.
- One song.
- One location: Grand Ballroom.
- One visible facility improvement.
- One wardrobe item: Moon Practice Gloves.
- One skill improvement: Beginner Confidence I or Technique I.
- Three playable 8-beat phrases.
- 12-card starter collection.
- 8-card active tutorial deck.
- Base + Modifier card play.
- Flow, Frame, Poise, and Bond.
- Open, Close, and Shadow stances.
- Three lead patterns: Close Invitation, Sudden Dip, and Dark Embrace.
- One Stumble state.
- One cinematic phrase replay.
- One dawn growth choice.

### Not Included in MVP

- Large facility roster.
- Complex rarity economy.
- Full card catalog.
- Advanced syncopation.
- Multiple romance routes.
- Multiple songs.
- Full free-to-play monetization.

### Success Criteria

The MVP succeeds if a player can:

- Understand that they are constructing dance phrases.
- Build a legal 8-beat routine.
- See cards become an animated dance sequence.
- Understand why a card is illegal.
- Match Alistair's lead.
- Recover from or avoid a Stumble.
- Spend dawn rewards on visible growth.
- Feel that the protagonist is becoming a better dance partner.

---

## 13. Production Plan

### Prototype Milestone 1: Paper and Clickable Flow

Deliverables:

- Card list for the MVP.
- One-page economy sketch.
- Day/Night/Dawn flow.
- Static portrait UI mockup.
- First three days journey map.

Goal: Confirm that the loop is readable before building animation.

### Prototype Milestone 2: Playable Card Phrase

Deliverables:

- Hand draw.
- Bar A / Bar B timeline.
- Legal stance checks.
- Flow generation and spending.
- Modifier slots.
- One lead pattern.
- Phrase lock-in.

Goal: Prove that 8-beat card construction feels tactical and mobile-readable.

### Prototype Milestone 3: Growth and Cinematic Payoff

Deliverables:

- One short dance replay.
- One Stumble animation state.
- One dawn reward screen.
- One wardrobe stat item.
- One facility improvement.
- One Bond scene or lead-preview benefit.

Goal: Prove that preparation changes the dance and the dance changes tomorrow.

---

## 14. Competition Positioning

Best category: Simulation and Management.

Why it fits:

- The main progression is daily management of training, wardrobe, relationship, cards, and manor facilities.
- The dance performance is the nightly test of those preparation choices.
- Rewards feed back into persistent growth rather than resetting between runs.

Special award potential:

- Most Innovative Design: gothic vampire Bachata deckbuilder is a distinctive genre combination.
- Best Visual Direction: strong if supported by UI mockups, character concepts, wardrobe evolution, and manor before/after images.

One-sentence positioning:

```text
Potionomics' management/deckbuilding structure, Love and Deepspace's intimate 3D romance, Shining Nikki's fashion progression, and dance-card novelty, wrapped in gothic vampire Bachata.
```
