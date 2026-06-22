# Dancing with Dracula: Card Catalog

This file contains the expanded card catalog for design and balancing. The main GDD should only include a small set of examples so the pitch stays focused on Simulation and Management.

Shadow stance cards and complex Syncopation cards are preserved here as future or expansion content. They should not be foregrounded in the hackathon-facing pitch.

---

## Card Anatomy

Every card should be defined with the following fields when it moves from concept to implementation:

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

---

## Basic Movement Cards

| Card | Type | Beat Cost | Req. Stance | End Stance | Effect |
| --- | --- | ---: | --- | --- | --- |
| Basic Side-Step | Footwork | 4 | Any | Same as Start | +40 points. Generates +1 Flow. Creates 1 Styling slot. |
| Basic Step | Footwork | 4 | Open | Open | +35 points. Generates +1 Flow. Simple beginner base. |
| Madrid Step | Footwork | 4 | Open | Open | +60 points. Generates +2 Flow. Creates 2 Styling slots. |
| Cathedral Walk | Footwork | 4 | Open or Close | Same as Start | +80 points. Generates +2 Flow. Upgraded from Basic Step. |
| Close Sway | Footwork | 2 | Close | Close | +30 points. Generates +1 Flow. Stabilizes Close stance. |

---

## Transition Cards

| Card | Type | Beat Cost | Req. Stance | End Stance | Effect |
| --- | --- | ---: | --- | --- | --- |
| Step Into Close | Transition | 2 | Open | Close | +20 points. Adds +10 Frame for this phrase. |
| Prep to Wrap | Transition | 2 | Open | Wrap | +15 points. Enables Wrap payoff moves. |
| Unwind to Open | Transition | 2 | Wrap | Open | +30 points. Safe exit from Wrap. |
| Shadow Entry | Transition | 2 | Close | Shadow | +40 points. Unlocks Shadow cards. Future content, not part of the hackathon pitch. |
| Reset Frame | Transition | 2 | Any | Open | +10 points. Clears a minor negative modifier. |

---

## Advanced Footwork Cards

| Card | Type | Beat Cost | Req. Stance | End Stance | Effect |
| --- | --- | ---: | --- | --- | --- |
| Sensual Body Roll | Footwork | 4 | Close | Close | +100 points. Gains x3 if played on Beats 5-8. |
| Hammerlock Turn | Footwork | 4 | Wrap | Open | +120 points. Clears one negative crowd or tension modifier. |
| The Sensual Dip | Footwork | 4 | Close | Open | +200 points. Requires 20 Frame to play safely. |
| Shadow Isolation | Footwork | 4 | Shadow | Shadow | +140 points. Creates a Syncopation anchor. Future content, not part of the hackathon pitch. |
| Moonlit Turnout | Footwork | 4 | Open | Open | +90 points. Extra multiplier if the Stained-Glass Gallery is restored. |

---

## Styling Cards

| Card | Type | Beat Cost | Flow Cost | Requirement | Effect |
| --- | --- | ---: | ---: | --- | --- |
| Head Accent | Styling | 0 | 1 | Attach to Footwork | +25 points. Beginner visual flourish. |
| Arm Throw | Styling | 0 | 1 | Attach to Open or Wrap base | +30 points. +0.5x Style Multiplier. |
| Sensual Hip Roll | Styling | 0 | 2 | Attach to Close base | +50 points. +1x if on Beat 4 or 8. |
| Eye Contact | Styling | 0 | 1 | Any base | +20 points. +1 Bond progress if Alistair's lead is matched. |
| Skirt Sweep | Styling | 0 | 2 | Requires gown equipped | +45 points. Adds cinematic cloth flourish. |

---

## Support Cards

| Card | Type | Beat Cost | Flow Cost | Requirement | Effect |
| --- | --- | ---: | ---: | --- | --- |
| Arm Frame | Support | 0 | 2 | Attach before demanding lead timing | +10 Frame. |
| Grounded Posture | Support | 0 | 1 | Any base | +5 Frame. Prevents minor Stumble. |
| Trust the Lead | Support | 0 | 2 | Lead pattern visible | Doubles lead match bonus if stance is correct. |
| Breath Sync | Support | 0 | 1 | Any base | +0.5x Mult. Draw 1 next phrase if played on beat 8 anchor. |
| Perfect Support | Support | 0 | 3 | Requires 20 Frame | Converts a dip check into a scoring bonus. |

---

## Advanced Library Flourishes

Syncopation is a Grand Library unlock, not a first-pitch core system and not a separate competition-facing card category. These cards are cataloged as advanced Styling cards.

| Card | Type | Beat Cost | Flow Cost | Anchor | Effect |
| --- | --- | ---: | ---: | --- | --- |
| Hair Toss | Styling | 0 | 0 | Immediately after Body Roll | +40 points. +0.5x Style Multiplier. Advanced Library flourish. |
| Finger Trace | Styling | 0 | 1 | Attached to Close card | +30 points. +1 Bond progress once per night. Advanced Library flourish. |
| Hip Tap Accent | Styling | 0 | 0 | Beat 4 or 8 only | +20 points. Maintains rhythm chain. Advanced Library flourish. |
| Quick Glance | Styling | 0 | 0 | After Eye Contact | +15 points. Reveals next phrase lead pattern earlier. Advanced Library flourish. |
| Rose Step | Styling | 0 | 1 | Conservatory restored | +35 points. Adds botanical VFX. Advanced Library flourish. |
