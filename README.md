# Rooftop Coins

**Rooftop Coins** is a browser-based rooftop platform game built around
a simple loop:

**Run → jump → collect → survive → advance**

The current development build is **Super Rooftop V7.5**. It keeps the
original easy-to-learn controls while adding a more polished rooftop
world, progressive levels, scoring bonuses, power-ups, hazards, cosmetic
unlocks, desktop/mobile layouts, and persistent high scores.

## Current Version --- V7.5

V7.5 is the current main development version.

Major V7/V7.5 improvements include:

-   More detailed modular rooftop buildings and city artwork.
-   Rooftop props including water towers, skylights, planters, vents,
    ducts, pipes, antennas, railings, rooftop doors, and fire escapes.
-   Improved background-city coverage so the lower screen remains filled
    with buildings rather than exposed sky.
-   Polished rendered coins, mines, medical kits, obstacles, and
    power-up artwork.
-   Camera easing, subtle forward look-ahead, and a small landing bump.
-   Redesigned score HUD with **SCORE** and saved **BEST** score.
-   Desktop-only keyboard legend.
-   New Rooftop Coins splash/start screen.
-   Improved portrait/mobile HUD layout.
-   Raised mobile Restart / Pause / End controls.
-   Removal of the old bottom-screen fog/fade so building artwork stays
    visible to the bottom.
-   Centralized **GAME SETTINGS - SAFE VALUES TO CHANGE** section.

## Goal

Run across the rooftops, collect coins, survive hazards, and advance
through the levels before time runs out.

The course becomes more difficult as the player progresses.

## Controls

### Desktop

-   **A / D** or **Left / Right Arrow** --- Move
-   **W / Up Arrow / Space** --- Jump
-   Press jump again while airborne --- **Double jump**
-   **P** --- Pause / resume
-   **H** --- Home / end the current run
-   **R** --- Restart
-   Secret code **67** --- Toggle the original secret fly mode

A single-line shortcut legend is displayed near the bottom of the
desktop game screen. The shortcut letters are highlighted in gold.

### iPhone / Mobile

-   Large on-screen **Left / Right** controls --- Move
-   Large **Jump** button --- Jump / double jump
-   **P** --- Pause / resume
-   Hold **R** --- Restart
-   Hold **E** --- End the current run
-   **CODE** --- Enter the secret flight code

Restart and End require a short hold to reduce accidental presses.

When temporary flight or secret flight is active, the jump control
becomes **Fly Up** and the flight controls allow vertical movement.

## Lives & Time

Current default settings:

-   Starting lives: **3**
-   Maximum lives: **6**
-   Starting Level 1 time: **60 seconds**
-   Final countdown begins with **10 seconds** remaining
-   Medical kit: every **3 levels**

When the player advances to another level, bonus time is added to the
remaining clock.

Current level-time settings:

-   Base level bonus: **22 seconds**
-   Maximum level bonus: **38 seconds**
-   Bonus increases every **2 levels**
-   Increase per bonus step: **3 seconds**

## Levels

The current game supports up to **30 levels** in a run.

Each level uses the rooftop-building system with increasing variation
and difficulty. Later levels introduce more demanding rooftop heights,
moving obstacles, mines, moving mines, and special power-up challenge
sections.

Current hazard progression:

-   Obstacles begin: **Level 2**
-   Mines begin: **Level 4**
-   Moving obstacles begin: **Level 6**
-   Moving mines begin: **Level 7**

## Scoring

Current scoring values include:

-   Coin: **100 points**
-   Power-up pickup: **200 points**
-   Perfect Jump: **250 points**
-   Close Call: **150 points**
-   Full-life medical kit: **300 points**
-   Combo bonus step: **25 points**
-   Combo window: **2 seconds**

The upper-right HUD displays the current **SCORE** and saved **BEST**
score.

## Power-Ups

### Magnet

Temporarily attracts nearby coins toward the player.

Current duration: **6 seconds**

### Boost

Temporarily improves the player's movement/jump capability.

Current duration: **6 seconds**

### Shield

Provides protection from **one mine hit**.

Once collected, the Shield remains ready until it absorbs a hit.

**Shield = save protection until it is needed.**

### Force Field

Creates temporary protection that allows the player to move safely
through a mine-field challenge.

Current duration: **7 seconds**

Force Field event levels intentionally use this sequence:

**Collect Force Field → enter mine field → pass through while protected
→ Shield appears afterward**

The regular rotating power-up is suppressed on these event levels so
Shield and Force Field do not appear together before the mine field.

Force Field events currently occur every **4 levels**, beginning once
mines are active.

### Flight

Provides temporary flight.

Current duration: **9 seconds**

Flight-event levels intentionally create a rooftop gap that normal
jumping cannot cross.

The intended sequence is:

**Jump for Flight → flight activates → cross the large gap → land before
Flight expires**

The first Flight event begins at **Level 6** and repeats every **6
levels**.

### Medical Kit / Extra Life

A medical kit appears every **3 levels**.

Collecting it adds **1 life**, up to the maximum of **6**.

If the player is already at maximum lives, the kit awards bonus points
instead.

## Special Gameplay Philosophy

Rooftop Coins uses an **ability → challenge** design whenever possible.

Examples:

-   **Force Field → mine field**
-   **Flight → otherwise impossible rooftop gap**
-   **Shield → protection for a later hit**
-   **Medical Kit → jump/risk for another life**

This keeps power-ups connected to gameplay instead of making them purely
decorative collectibles.

## Camera & Presentation

V7 introduced additional camera polish:

-   Smooth horizontal camera easing.
-   Subtle forward look-ahead based on player movement.
-   Small landing bump on stronger landings.
-   Player framing controlled by an adjustable screen-position setting.

The building system also includes modular visual details such as rooftop
access doors, railings, pipes, AC ducts, antennas, fire escapes, water
towers, vents, skylights, planters, and other rooftop equipment.

## Splash Screen

V7.5 uses a new illustrated Rooftop Coins start screen designed to match
the game's current visual style.

The splash includes:

-   Rooftop Coins title artwork.
-   Rooftop/city scene.
-   **START GAME** button.
-   Desktop control guide.
-   Power-up guide.

The splash artwork itself does not need to carry the development version
number.

## Desktop HUD

The desktop HUD includes:

-   Lives
-   Coin information
-   Timer
-   Current level
-   Current score
-   Best score
-   Active power-up status
-   Single-line keyboard shortcut legend near the bottom

The former eagle and top pause icons were removed to simplify the HUD.

## Mobile / Portrait Layout

V7.5 includes dedicated portrait-mode layout adjustments.

The mobile HUD is scaled and positioned separately so lives, coin
information, timer, level, and score do not overlap.

The mobile **R / P / E** action buttons are raised above the large
movement controls.

The old lower-screen fade/fog effect has been removed so
rooftop/building artwork remains visible to the bottom of the screen.

## Cosmetic Progression

Character outfits and city backgrounds use persistent browser
progression.

Current settings:

-   New character/outfit unlock: every **10 plays**
-   New background unlock: every **5 plays**
-   Cosmetic progression during a run: every **2 levels**

The game remembers unlocked cosmetics, while a new run can still
progress visually through the unlocked tiers.

## Persistent Browser Data

Rooftop Coins uses browser `localStorage` for information such as:

-   Play count
-   Cosmetic unlock progression
-   High scores

Closing and reopening the game normally preserves this information.

Different browsers or devices can therefore have different scores and
unlock progress.

## High Scores

The game stores up to **5 high scores**.

A qualifying score can prompt the player for a name of up to **10
characters**.

The highest saved score is also shown as **BEST** in the in-game score
HUD.

## GAME SETTINGS --- SAFE VALUES TO CHANGE

The current HTML keeps the main creator-adjustable values together near
the beginning of the JavaScript under:

``` javascript
// ============================================================
// GAME SETTINGS - SAFE VALUES TO CHANGE
// ============================================================
```

This is the preferred place to tune the game rather than searching
through the main gameplay code.

### World / Levels

``` javascript
LEVEL_WIDTH = 4300
MAX_LEVELS = 30
ROOFTOP_VARIATION_START_LEVEL = 3
ROOFTOP_VARIATION_MAX = 58
ROOFTOP_VARIATION_PER_LEVEL = 4
```

### Cosmetics

``` javascript
CHARACTER_UPGRADE_EVERY = 10
BACKGROUND_CHANGE_EVERY = 5
COSMETIC_LEVELS_PER_STEP = 2
```

### Time

``` javascript
ROUND_TIME_SECONDS = 60
LEVEL_BONUS_BASE_SECONDS = 22
LEVEL_BONUS_MAX_SECONDS = 38
LEVEL_BONUS_EVERY_LEVELS = 2
LEVEL_BONUS_GROWTH_SECONDS = 3
FINAL_COUNTDOWN_SECONDS = 10
```

### Lives & Power-Ups

``` javascript
STARTING_LIVES = 3
MAX_LIVES = 6
BONUS_LIFE_EVERY_LEVELS = 3
POWERUP_SECONDS = 6
FORCE_FIELD_SECONDS = 7
FLY_BONUS_SECONDS = 9
FORCE_EVENT_EVERY_LEVELS = 4
FORCE_EVENT_POST_SHIELD = true
FLY_EVENT_FIRST_LEVEL = 6
FLY_EVENT_EVERY_LEVELS = 6
MAGNET_RANGE = 190
```

### Hazards

``` javascript
OBSTACLE_START_LEVEL = 2
MOVING_OBSTACLE_START_LEVEL = 6
MINE_START_LEVEL = 4
MOVING_MINE_START_LEVEL = 7
```

### Player Physics

``` javascript
RUN_SPEED = 300
FLY_HORIZONTAL_SPEED = 340
FLY_VERTICAL_SPEED = 310
RUN_ACCELERATION = 1200
JUMP_VELOCITY = -540
BOOST_JUMP_VELOCITY = -610
GRAVITY = 1450
MAX_JUMPS = 2
```

### Score

``` javascript
COIN_POINTS = 100
COMBO_WINDOW_SECONDS = 2.0
COMBO_BONUS_STEP = 25
PERFECT_JUMP_POINTS = 250
CLOSE_CALL_POINTS = 150
POWERUP_PICKUP_POINTS = 200
FULL_LIFE_MEDKIT_POINTS = 300
```

### Message / HUD Position

Screen-height values use fractions:

-   `0.00` = top
-   `0.50` = center
-   `1.00` = bottom

Current values include:

``` javascript
MESSAGE_BANNER_Y = 0.45
LEVEL_BANNER_Y = 0.24
FINAL_COUNTDOWN_Y = 0.20
MESSAGE_BANNER_SECONDS = 1.25
```

Increasing `MESSAGE_BANNER_Y` moves the temporary bonus/power-up message
**lower**.

### Desktop Shortcut Legend

``` javascript
DESKTOP_LEGEND_Y = 0.955
DESKTOP_LEGEND_FONT_SIZE = 15
DESKTOP_LEGEND_OPACITY = 0.82
DESKTOP_LEGEND_KEY_SIZE_BONUS = 2
```

### Mobile Portrait Layout

``` javascript
MOBILE_ACTION_HOLD_SECONDS = 0.7
MOBILE_PORTRAIT_ACTIONS_BOTTOM = 118
MOBILE_PORTRAIT_HUD_SCALE = 0.68
MOBILE_PORTRAIT_HUD_TOP = 22
MOBILE_PORTRAIT_TIMER_Y = 82
```

`MOBILE_PORTRAIT_ACTIONS_BOTTOM` controls how high the mobile **R / P /
E** row sits above the bottom of the screen.

### High Scores / Secret Code

``` javascript
HIGH_SCORE_COUNT = 5
HIGH_SCORE_NAME_LENGTH = 10
SECRET_FLY_CODE = '67'
```

## GitHub Pages

Repository:

`assafavi/rooftop-coins`

Rooftop Coins is designed to run directly in the browser and can be
hosted with GitHub Pages.

The active development HTML can be used as the main `index.html` when
publishing the current build.

Older versions can remain in separate folders if they are still wanted
for comparison or archival purposes.

Example structure:

``` text
rooftop-coins/
├── index.html
├── README.md
├── CHANGELOG.md
├── rooftop-coins-icon.png
├── v2/
│   └── index.html
├── v3/
│   └── index.html
├── v4/
│   └── index.html
└── archive/
    └── older-builds...
```

## iPhone Home-Screen Icon

Store the custom icon in the repository as:

`rooftop-coins-icon.png`

The HTML currently includes an Apple touch-icon reference.

If iOS continues showing an older icon after the artwork changes, remove
the existing Home Screen shortcut and add it again because iOS may cache
the previous icon.

## Development Guidelines

When adding features:

1.  Keep the core controls simple.
2.  Avoid adding controls unless they create meaningful gameplay.
3.  Put creator-adjustable values in **GAME SETTINGS - SAFE VALUES TO
    CHANGE**.
4.  Keep desktop and mobile layouts independently usable.
5.  Test both desktop landscape and iPhone portrait.
6.  Prefer **ability → challenge** gameplay.
7.  Preserve earlier working builds before major changes.
8.  Update `README.md` and `CHANGELOG.md` when a meaningful version
    milestone is reached.

------------------------------------------------------------------------

**Current development version documented here: Super Rooftop V7.5**

**README updated: September 28, 2026**
