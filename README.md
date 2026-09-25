# Rooftop Coins

**Rooftop Coins** is a browser-based rooftop platform game. Run, jump, double-jump, collect coins, avoid hazards, earn bonuses, and progress through increasingly difficult rooftop levels.

The project keeps **V2, V3, and V4** available as separate playable versions so newer development does not replace the earlier games.

## Playable Versions

- **V2 — Classic:** the original Rooftop Coins game.
- **V3 — Enhanced:** improved 2.5D graphics, animation, effects, scoring bonuses, power-ups, and sound effects.
- **V4 — Super Rooftop:** level-based progression with hazards, bonus time, lives, advanced power-ups, cosmetic progression, and special challenge sections.

The root `index.html` is the version-selection screen and links to `v2/`, `v3/`, and `v4/`.

## Controls

### Desktop
- **A / D** or **Left / Right Arrow** — Move
- **W / Up Arrow / Space** — Jump
- Press jump again while airborne — **Double jump**
- **P** — Pause / resume
- **R** — Restart
- **H** — End the game early
- Secret code **67** — Toggle the original secret fly mode

### iPhone / Mobile
- On-screen left/right movement
- Jump / double jump
- **P** — Pause / resume
- Hold **R** — Restart
- Hold **E** — End early
- While flying, the jump control becomes **FLY UP** and a down control appears.

## Core V4 Gameplay

V4 starts with **3 lives** and **60 seconds**. Coins are worth **100 points**. The player progresses through multiple rooftop levels with increasingly difficult hazards.

Falling, running out of time, and certain hazards can cost a life. Medical kits can increase lives to a maximum of **5**.

When a life is lost, the player retries the current V4 level rather than restarting the entire run.

## Level & Bonus-Time System

Reaching the next level adds bonus time to whatever time remains.

Current timing settings:
- Starting time: **60 seconds**
- Base level bonus: **22 seconds**
- Maximum level bonus: **38 seconds**
- Final countdown warning: final **10 seconds**

The game displays the new level and added time when the player advances.

## Medical-Kit Bonus Life

A medical kit appears every **3 levels**.

It is shown as a white medical case with a red cross and is positioned high enough that the player must jump for it.

Collecting one adds **1 life**, up to the maximum of **5**. If the player already has the maximum number of lives, the kit awards bonus points instead.

## Power-Ups

V4 uses graphical power-up objects rather than the earlier simple circles containing letters.

### Magnet
A horseshoe-magnet-style pickup that temporarily pulls nearby coins toward the player.

### Boost
An energy/lightning-style pickup that temporarily boosts movement.

### Shield
A shield-shaped pickup providing **one-hit mine protection**.

Once collected, `SHIELD READY` remains active until the player hits a mine. The Shield absorbs that hit and then disappears.

**Shield = save it until you need it.**

### Force Field
A glowing energy-orb pickup positioned high enough to encourage a **double jump**.

When collected, an energy bubble surrounds the player for approximately **7 seconds**. Mines do not hurt the player while the Force Field is active.

Force Field sections are deliberately designed as events. Immediately after the pickup, the player encounters a concentrated mine field with rooftop and moving/floating mines.

**Force Field = temporary protection; grab it and go through the dangerous section.**

### Flight Bonus
An elevated flight pickup gives approximately **9 seconds of flight**, using the same basic flying mechanics as secret code `67`.

Flight-event levels contain a large rooftop gap that ordinary jumping cannot cross. The player must grab the flight bonus and fly across before it expires.

The secret **67** code remains available separately as the original toggleable/testing fly mode.

## Force Field Challenge

The intended sequence is:

**Double-jump → collect Force Field → energy bubble activates → mine field appears → move through the danger before the field expires.**

Mine-field sections can contain:
- Stationary rooftop mines
- Horizontally moving mines
- Vertically moving/floating mines

This makes the Force Field immediately useful instead of placing it where no danger is nearby.

## Flight Challenge

The intended sequence is:

**Jump for Flight bonus → flight activates → major rooftop gap appears → fly across before the timer expires.**

Some rooftops are deliberately omitted so normal jumping cannot cross the gap.

## Pause System

V4 includes a true pause function:
- Desktop: **P**
- Mobile: tap **P**

While paused, player movement, the game timer, hazards, and power-up timers stop.

## Cosmetic Progression

Character outfits and city backgrounds use a **hybrid permanent-unlock / per-run progression system**.

The browser remembers the highest cosmetics permanently unlocked, but every new run starts visually simple again. As the player advances, the game progresses through cosmetics already unlocked:

- **Levels 1–2:** basic/Rookie look
- **Levels 3–4:** next unlocked look
- **Levels 5–6:** next
- **Levels 7–8:** next
- **Level 9+:** highest available unlocked look

Current outfit names:
1. Rookie
2. Street Runner
3. Rooftop Pro
4. Sky Racer
5. Rooftop Legend

If the player has not unlocked every tier, the run stops visually progressing at the highest tier owned.

This fixes the earlier issue where, after all outfits/backgrounds had been earned, later games contained no visual progression.

## Persistent Browser Data

Rooftop Coins uses browser `localStorage` for information including:
- Play count
- Cosmetic unlock progression
- High scores

Closing and reopening the game normally does not erase this information. Different browsers or devices can therefore have different progression.

## Major V3/V4 Improvements

Development beyond the original game includes 2.5D rooftops, parallax city backgrounds, animated character movement, improved coins, particles, rooftop details, dynamic camera behavior, perfect-jump and close-call bonuses, coin combos, power-ups, moving obstacles, mines, moving/floating mines, sound effects, dramatic final countdown, level progression, bonus time, cosmetic unlocks, per-run cosmetic progression, medical-kit bonus lives, one-hit Shield, timed Force Field, mine-field events, temporary flight, flight-required gaps, and pause/resume controls.

## On-Screen Bonus Displays

During play, active effects can display messages such as:

`MAGNET` · `BOOST` · `SHIELD READY` · `FIELD 6.4` · `FLY 8.2`

Temporary messages also appear for bonus lives, new cosmetics, level time, Shield hits, Force Fields, and flight events.

The active-power-up bar is drawn near the bottom of the V4 JavaScript with code similar to:

```javascript
roundRect(x,W/2-150,58,300,31,11);
x.fillText(active.join('  •  '),W/2,79);
```

Increasing `58` and `79` moves this display **lower** on the screen.

Temporary bonus text uses:

```javascript
x.fillText(bonusText,W/2,H*.28);
```

Increasing `.28` (for example to `.38`) moves that message lower.

## Important V4 Settings

Frequently adjusted values include:

```javascript
ROUND_TIME_SECONDS = 60
STARTING_LIVES = 3
MAX_LIVES = 5
BONUS_LIFE_EVERY_LEVELS = 3

LEVEL_BONUS_BASE_SECONDS = 22
LEVEL_BONUS_MAX_SECONDS = 38
LEVEL_BONUS_EVERY_LEVELS = 2

FORCE_FIELD_SECONDS = 7
FLY_BONUS_SECONDS = 9

COIN_POINTS = 100
COMBO_WINDOW_SECONDS = 2.0
PERFECT_JUMP_POINTS = 250
CLOSE_CALL_POINTS = 150
FINAL_COUNTDOWN_SECONDS = 10
```

## GitHub Pages Structure

```text
rooftop-coins/
├── index.html
├── README.md
├── rooftop-coins-icon.png
├── v2/
│   └── index.html
├── v3/
│   └── index.html
└── v4/
    └── index.html
```

The root page lets players choose V2, V3, or V4 while keeping each version independent.

## iPhone Home-Screen Icon

Store the custom icon in the repository root as `rooftop-coins-icon.png`.

The root HTML can reference it with:

```html
<link rel="apple-touch-icon" sizes="180x180" href="/rooftop-coins/rooftop-coins-icon.png">
```

iOS can cache Home Screen icons. If the artwork changes but the old icon remains, remove the existing Home Screen shortcut and add it again.

## Design Direction

The basic Rooftop Coins formula remains:

**Run → jump → collect → survive → advance**

New mechanics should add replay value without making the controls complicated.

V4 also follows this design principle:

**Give the player a special ability, then immediately present a challenge that makes that ability useful.**

Examples:
- **Force Field → mine field**
- **Flight → otherwise impossible rooftop gap**
- **Shield → protection saved for a future mine hit**

---

**Current development version documented here: Super Rooftop V4.3 — Power Events**
