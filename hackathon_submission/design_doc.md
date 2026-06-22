# Meta Horizon Creator Competition: Game Design

## Game Design Document

**Game Title:** Dancing with Dracula: Crimson Manor  
**Genre:** Simulation & Management  
**Platform:** Mobile, iOS and Android  
**Orientation:** Portrait  
**Session Target:** 5-10 minutes  

---

## 1. Concept

**Dancing with Dracula: Crimson Manor** is a gothic romance dance-life simulation where a mortal follower trains by day, styles herself for the ballroom, restores a haunted manor, and dances Bachata by night with Alistair, a cursed vampire lord. The player's goal is to become a more confident, expressive, and trusted dance partner while transforming Crimson Manor from a cold, silent estate into a living performance space.

This is **Simulation & Management first**: every night is shaped by how the player managed the day. Training changes starting resources, wardrobe changes performance builds, card rehearsal changes available choreography, manor restoration unlocks better preparation spaces, and Bond with Alistair changes how clearly the player reads his lead. The card play is the nightly test of those management decisions, not a separate roguelike run. Nothing meaningful resets between sessions. The player keeps her cards, outfits, skills, manor upgrades, and Bond with Alistair.

The signature interaction is building short 8-beat Bachata phrases from cards. Footwork and Transition cards fill the musical count. Styling and Support cards add expression, romance, safety, and scoring. Once a phrase is locked, the interface fades and the characters perform the chosen movement as a cinematic partner dance. The player is not playing abstract attacks or defenses. She is choosing posture, timing, connection, and confidence.

**The first game where deck-construction IS choreography.**

The fantasy is intimate and aspirational: a mortal dancer enters a supernatural ballroom underprepared, then gradually becomes someone who can meet a vampire lord's lead without losing herself. Every system should answer one question: **how did tonight's preparation make tomorrow's dance more beautiful, more controlled, or more emotionally charged?**

---

## 2. Target Player

The primary player is a mobile-first romance, fashion, and cozy-progression player, especially women 18-35, who wants short daily sessions with visible long-term growth. She enjoys character bonding and style expression, but does not want harsh resets or combat-first pressure.

The secondary player is a light strategy or deck-construction player who likes sequencing and optimization. The Bachata phrase system gives that player a tactical puzzle while keeping the fantasy romantic, stylish, and nonviolent.

| Motivation | How the Game Serves It |
|---|---|
| Romance and connection | Alistair is both the love interest and the lead pattern the player learns to read. |
| Style with consequences | Outfits change appearance and performance stats, making fashion a management choice. |
| Tactical expression | Each 8-beat phrase asks the player to solve timing, stance, Flow, and Frame through choreography. |

The game is for players who want a stylish, emotionally charged management loop where tactical decisions are expressed through dance, not combat.

---

## 3. Core Loop

The core loop is:

```text
Prepare by day -> Dance by night -> Grow at dawn -> Return stronger tomorrow
```

### Day: Prepare

Each day gives the player a small number of meaningful preparation choices. The player chooses whether to train, rehearse cards, style the follower, spend time with Alistair, or improve a manor space. The limit matters because the player cannot optimize everything at once. A player preparing for a risky dip might train Frame or equip gloves. A player chasing higher style rewards might rehearse a Close-stance combo or wear a gown that reduces Styling costs.

### Night: Dance

At night, the player performs a short dance made of 8-beat phrases. Each phrase asks the player to:

- Fill exactly 8 Beats with movement.
- Stay in legal stances. The MVP proves Open and Close; the full game adds riskier Wrap and vampire-specific Shadow.
- Generate Flow through movement.
- Spend Flow on Styling or Support.
- Build enough Frame to answer demanding lead patterns.
- Avoid Stumbles that reduce Poise and break momentum.
- Match Alistair's lead for Connection rewards.

The player sees the tactical result immediately because the cards become a dance replay. If a phrase was clean, the dancers look connected and the camera rewards the moment. If the player rushed into the wrong stance or lacked Frame, the Stumble is visible in the animation.

### Dawn: Grow

Dawn converts the dance into persistent progress. The player earns Lumen Essence, Bond, card materials, wardrobe materials, and facility progress. These rewards are then spent on improvements that change future preparation and performance.

| Loop Step | Player Question | Satisfaction |
|---|---|---|
| Day | What should I prepare for tonight? | Strategic anticipation. |
| Night | Can I build a clean, expressive phrase? | Tactical execution and cinematic payoff. |
| Dawn | What did this dance change? | Visible growth and tomorrow's hook. |

One cycle feels complete on its own, but every cycle also leaves a reason to return: a card to upgrade, an outfit to finish, a room to restore, a Bond threshold to reach, or a lead pattern the player now knows how to answer.

---

## 4. Progression, Depth & Retention

The game's depth comes from interconnected persistent systems rather than a large number of disconnected features. The player is always improving the same fantasy from several angles: her body, her style, her deck, her relationship, and her home base.

### Persistent Growth Model

The protagonist grows through six practical skill tracks:

| Skill | Managed Through | Why It Matters |
|---|---|---|
| Technique | Mirror Hall drills and rehearsal | Cleaner Footwork and more reliable phrase construction. |
| Musicality | Music Room practice | Stronger Flow generation and Beat 4/8 accent rewards. |
| Frame | Support practice, gloves, partner drills | Safer dips and demanding lead responses. |
| Styling | Wardrobe Atelier upgrades | More efficient flourishes and stronger style scoring. |
| Confidence | Successful performances and outfits | More Poise and softer Stumble penalties. |
| Connection | Time with Alistair and lead study | Earlier lead previews and better Perfect Connection rewards. |

These tracks are intentionally tied to other systems. A player does not raise "Frame" as a number in isolation; she can train it, wear for it, rehearse cards that support it, and test it against Alistair's lead. That interconnection is what makes the simulation layer feel alive.

### Dance-Card Depth

The card system is built around readability first. Every phrase has a strict 8-beat timing limit, so the player always understands the frame of the puzzle. Within that frame, depth comes from four card roles:

| Card Role | Function |
|---|---|
| Footwork | Base movement, score foundation, Flow generation. |
| Transition | Stance changes that set up legal future movement. |
| Styling | Visual flourish, score bonuses, Bond accents. |
| Support | Frame, Poise protection, safer response to difficult leads. |

The important design choice is that cards describe dance intentions. "Step Into Close" is not a generic buff. It changes the partner relationship on screen and prepares the player for a Close Invitation. "Eye Contact" is not just a point bonus. It reinforces Bond when played in a connected phrase. The game earns its novelty by making the mechanics and the fantasy use the same language.

**Shadow stance** is the vampire-flavor differentiator. Open and Close teach readable partner dancing; Shadow is unlocked through Bond and lets the follower move inside Alistair's supernatural silhouette. It offers higher Lumen and unique vampire choreography, but it is risky if the player rushes intimacy without enough trust or Frame. In one rule, Shadow ties romance, vampire fantasy, and tactical stance management together.

Example phrase:

```text
Alistair's Lead: Close Invitation
Goal: Enter Close before Beat 5

Start Stance: Open

Bar A, Beats 1-4:
Foil Basic Step
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
8 Beats complete, lead matched, Perfect Connection x2.
The replay shows the player stepping into Alistair's frame as the camera tightens on Beat 8.
```

### Wardrobe as Management, Not Decoration

Wardrobe is a progression system and a tactical layer. Shoes, gloves, gowns, jewelry, hairstyles, and perfume create builds. A beginner outfit might grant Starting Frame and extra Poise. A more confident style build might reduce the Flow cost of the first Styling card in each phrase. A romance-focused jewelry piece might add Bond when Eye Contact lands during a matched lead.

This gives fashion a reason to exist beyond collection. The player is not only asking, "What looks good?" She is asking, "What kind of dancer am I becoming tonight?"

### Manor Restoration

Crimson Manor is the persistent hub. Restoring a room should do three things: change the environment visually, unlock or improve a mechanic, and give the player a reason to revisit the space during the day. The key facilities are the Grand Ballroom, Mirror Hall, Wardrobe Atelier, and Music Room.

The GDD does not need to specify every upgrade tier; the important rule is that the manor is not a passive backdrop. It is the physical expression of the player's growth. As the follower becomes more capable, the manor becomes warmer, brighter, and more musically alive.

### Complexity Over Time

The game layers complexity deliberately:

| Moment | Player Understands | New Depth Introduced |
|---|---|---|
| Minute 1 | The manor responds to dance. | Basic movement and the 8-beat phrase. |
| Minute 15 | Preparation affects the dance. | Day choices, first lead match, first visible reward. |
| Third session | Builds create different outcomes. | Wardrobe stats, card rehearsal, Bond benefits, safer risky moves. |
| Later play | The player has a style identity. | Specialized outfits, advanced stance chains, higher-scoring lead responses. |

Retention comes from overlapping hooks:

- **Daily planning:** The player has limited preparation actions and must choose a focus.
- **Collection growth:** Cards and wardrobe pieces create new build options.
- **Visible transformation:** The follower's movement, outfits, and manor spaces improve.
- **Relationship thresholds:** Bond unlocks dialogue, lead readability, and more intimate dance invitations.
- **Mastery goals:** A player can replay a song to match leads cleaner, avoid Stumbles, or land a perfect phrase.

The result is a game that can support a casual daily ritual while still giving invested players meaningful optimization.

---

## 5. What Makes It Fun

The emotional core is **becoming worthy of the dance**. The player begins as a mortal outsider in a supernatural space. She is not powerful because she defeats Alistair or conquers the manor. She becomes powerful by learning rhythm, trust, posture, and presence.

The fun comes from three connected feelings.

First, there is the satisfaction of preparation paying off. The player chooses gloves because she expects a demanding lead, then survives the dip because that decision mattered. The game creates a clear link between management and performance.

Second, there is the pleasure of expression under constraint. The 8-beat phrase gives the player a small, understandable puzzle. The player can simply complete it, or she can complete it beautifully: correct stance, enough Frame, a timed accent, a Styling flourish, and a lead match that becomes a cinematic moment.

Third, there is romantic tension. Alistair's lead is both a mechanic and a character signal. Early leads feel cold, formal, and partially hidden. As Bond grows, the player reads him sooner and earns more intimate choreography. The relationship is not a separate visual-novel layer pasted onto a card game. It changes how the dance is played.

The "one more round" pull is practical and emotional at the same time:

- "I almost matched that lead cleanly."
- "If I train Frame tomorrow, I can land the dip."
- "If I finish this outfit, my Close-stance build will work."
- "If I reach the next Bond level, Alistair may reveal a new invitation."

The design is innovative because **deck-construction is choreography**. Instead of battling monsters or managing generic buildings, the player manages confidence, technique, wardrobe, and intimacy, then proves those choices through a danced phrase. That gives the game a recognizable identity in the Simulation & Management category while still being buildable as a mobile loop.

---

## 6. If I Had More Time

The first version should prove the daily preparation loop, the 8-beat phrase builder, persistent growth, wardrobe function, and one strong relationship arc. A second version would expand the fantasy without changing the foundation.

The most valuable additions would be:

| Addition | Why It Matters |
|---|---|
| More songs and rhythm profiles | Lets Musicality matter more and gives players new phrase pressures. |
| Additional manor facilities | Expands the simulation layer with specialized growth paths. |
| Seasonal dance events | Creates time-limited goals around costumes, songs, and themed lead patterns. |
| Deeper wardrobe sets | Supports build identity and stronger visual transformation. |
| Social showcase features | Allows players to share outfit builds, phrase replays, or restored manor snapshots. |
| Advanced dance vocabulary | Adds higher-skill cards after the core 8-beat system is proven. |
| Optional romance routes | Expands the character layer if the Alistair relationship loop validates. |

The features deliberately scoped out of the first version are full monetization design, multiple romance routes, a large song library, complex syncopation, and a full endgame facility roster. Those systems could make the game richer, but they are not required to prove the core. The winning version of this design starts with one partner, one manor, one clear daily loop, and one elegant dance-card engine that turns preparation into performance.

The long-term vision is a gothic mobile dance-life sim where players return not because they lost a run, but because tomorrow they can dance with more style, more trust, and more control than they could tonight.
