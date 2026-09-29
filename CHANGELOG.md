# Rooftop Coins --- Change Log

This file records the development of **Rooftop Coins** from the original
browser-game prototype through the current **Super Rooftop V7.5** build.

> **History note:** The earliest builds were developed iteratively
> before formal release notes were maintained. Where an exact version
> number cannot be established confidently, changes are grouped under an
> Early Development or Transitional Development heading rather than
> assigning an invented version number.

------------------------------------------------------------------------

## Project Beginning --- Original Rooftop Game

### Initial concept

Rooftop Coins began as a simple 2D browser platform game built around
the loop:

**Run → jump → collect coins → reach the end before time runs out.**

### Original gameplay

-   Side-scrolling rooftop course.
-   Player movement left and right across buildings.
-   Jumping between rooftops.
-   Coin collection and scoring.
-   60-second game timer.
-   3 starting lives.
-   Falling off the bottom costs a life.
-   Goal: reach the final rooftop or collect all coins before time
    expires.
-   Browser-based HTML/JavaScript game requiring no installation.

### Original desktop controls

-   **A / D** or **Left / Right Arrow** --- Move.
-   **W / Up Arrow / Space** --- Jump.
-   Double jump added for larger rooftop gaps.
-   **R** --- Restart.
-   **H** --- End the game early.

------------------------------------------------------------------------

## Early Development --- Mobile, Persistence & Replay Features

### iPhone/mobile support

The game was adapted for touch devices.

Added: - On-screen Left and Right controls. - Large on-screen Jump
button. - Mobile Restart control. - Mobile End control. - Portrait and
landscape layout work. - Browser scaling and viewport adjustments.

### Safer mobile actions

Restart and End became hold actions to reduce accidental presses.

-   Hold **R** --- Restart.
-   Hold **E** --- End the run.

### Secret flight mode

Added secret code:

**67**

Entering `67` toggles the original fly mode.

While flying: - Jump becomes Fly Up. - A fly-down control is available
on mobile. - Normal gravity-based rooftop movement is replaced
temporarily by flight controls.

This hidden feature later became the basis for the normal Flight
power-up.

### High scores and persistence

Added browser `localStorage` support for: - High scores. - Play count. -
Later cosmetic unlock progression.

### Cosmetic progression foundation

Persistent play count became the basis for unlocking new outfits and
backgrounds over repeated plays.

------------------------------------------------------------------------

# V2 --- Classic

V2 preserved the original Rooftop Coins experience as the **Classic**
version.

### Major V2 features

-   Rooftop running and jumping.
-   Coin collection.
-   60-second round.
-   3 lives.
-   Double jump.
-   Desktop keyboard controls.
-   Mobile touch controls.
-   Restart and early-end controls.
-   Secret `67` flight mode.
-   High-score functionality.
-   Browser persistence.
-   Original splash/instruction screen.

V2 remained separately playable so later experiments would not overwrite
the classic game.

------------------------------------------------------------------------

# V3 --- Enhanced / Rooftop Coins 3.0

V3 was the first major visual and gameplay-polish phase.

The goal remained:

**Run → jump → collect → finish**

while making the world deeper, more animated, and more rewarding to
replay.

## Visual upgrade

### 2.5D rooftops

Buildings gained: - Visible rooftop surfaces. - Front faces. - Side
faces. - Greater visual depth.

### Parallax city

Multiple city/background layers began moving at different speeds to
create depth.

### Character presentation

The player gained more expressive movement and poses, including: -
Running. - Jumping. - Double jumping. - Falling. - Landing.

### Rooftop details

Environmental rooftop objects were added so buildings felt less empty.

### Improved coins

Coins gained: - Thicker 3D-style appearance. - Spin. - Glow. -
Sparkle. - Collection effects.

### Particle effects

Added effects for coin pickups and other gameplay events.

### Camera improvements

Camera behavior was improved to follow the player more naturally and
reveal upcoming rooftops.

## Scoring and skill bonuses

### Perfect Jump

Added bonus scoring for especially good rooftop landings.

### Close Call

Added scoring for narrowly clearing dangerous gaps or obstacles.

### Coin combos

Rapid consecutive coin collection could build combo rewards.

### Bonus messages

Temporary messages began communicating bonuses and special events.

## First power-ups

Introduced collectible gameplay bonuses: - **Magnet** --- attracts
nearby coins. - **Boost** --- temporarily improves movement/jumping. -
**Shield** --- defensive protection.

Power-up graphics became progressively more recognizable.

## Audio and countdown

Added generated sound effects for gameplay events and a dramatic final
**10-second countdown**.

------------------------------------------------------------------------

# V4 --- Super Rooftop

V4 changed Rooftop Coins from primarily a single-course timed game into
a continuing, level-based rooftop challenge.

------------------------------------------------------------------------

## V4.0 --- Levels, Hazards & Bonus Time

### Continuous level system

Added a multi-level run structure.

Players could continue advancing through increasingly difficult rooftop
courses rather than simply completing one course.

### Bonus-time system

Completing a level adds time to the remaining clock.

Core design: - Level 1 begins with the standard round time. - Later
levels add bonus seconds. - Bonus time can scale upward as difficulty
increases.

### Level announcements

Advancing began displaying: - New level number. - Added time. -
Information about upcoming challenges.

### Checkpoint-style recovery

Losing a life no longer necessarily returned the player to the beginning
of the entire game.

The current level could be restored using its entry-state information.

### Progressive hazards

Hazards were introduced progressively: - Rooftop obstacles. - Stationary
mines. - Moving obstacles. - Moving mines.

------------------------------------------------------------------------

## V4.1 --- Bonus Lives, Force Field & Pause

### Medical kit / Extra Life

Added medical-kit pickups.

Behavior: - Appears periodically. - Positioned so the player generally
must jump to collect it. - Adds one life up to the maximum. - Awards
bonus points instead when lives are already full.

### Force Field

Added a temporary defensive power-up separate from Shield.

Initial behavior: - Glowing energy pickup. - Temporary protective
bubble. - Protection from mines while active. - Countdown shown in the
active-power-up HUD.

### Improved power-up artwork

Power-ups became visually distinct: - Magnet --- horseshoe magnet. -
Boost --- lightning/energy symbol. - Shield --- shield crest. - Force
Field --- glowing energy orb. - Life --- medical case.

### Pause

Added true pause support.

-   Desktop: **P**
-   Mobile: **P**

Pausing stops: - Player movement. - Game timer. - Hazard movement. -
Power-up timers.

### Startup repair

A V4.1 initialization-order issue that prevented the splash Play button
from starting the game was identified and corrected.

------------------------------------------------------------------------

## V4.2 --- Cosmetic Progression

V4.2 improved long-term cosmetic progression.

### Problem addressed

Because the browser remembered unlocked outfits/backgrounds permanently,
players who had earned everything could begin future runs with no visual
progression left.

### Hybrid progression

Permanent unlocks remained saved, while each new run could visually
progress through the cosmetics already earned.

### Outfit tiers

The progression system included: 1. Rookie 2. Street Runner 3. Rooftop
Pro 4. Sky Racer 5. Rooftop Legend

### Background progression

Background unlocks were changed to true permanent unlock levels rather
than endlessly cycling back to earlier backgrounds.

### Cosmetic announcements

Added messages such as: - `NEW LOOK` - `CITY LOOK UPGRADE` - Permanent
outfit unlock notices. - Permanent background unlock notices.

------------------------------------------------------------------------

## V4.3 --- Power Events

V4.3 established the gameplay philosophy:

**Ability → challenge**

Instead of making special abilities isolated collectibles, the game
began placing a challenge immediately after the ability that makes it
useful.

### Shield redesign

Shield was separated clearly from Force Field.

Shield became **one-hit protection**: - Collect Shield. - `SHIELD READY`
remains active. - No normal countdown. - Mine hit consumes the Shield. -
The protected hit does not cost a life.

### Force Field redesign

Force Field remained temporary.

The pickup was elevated so it usually required a strong/double jump.

A concentrated minefield was then placed immediately after the pickup.

Intended sequence:

**Double-jump → collect Force Field → enter minefield → cross while
protected**

Minefields could include: - Stationary rooftop mines. - Horizontally
moving mines. - Vertically moving/floating mines.

### Flight power-up

The original secret `67` flight mode inspired a normal temporary Flight
pickup.

Flight-event sequence:

**Jump for Flight → flight activates → cross an otherwise impossible gap
→ land before Flight expires**

The secret `67` mode remained available separately.

### Active power-up HUD

The game began displaying active effects such as: - Magnet. - Boost. -
Shield Ready. - Force Field. - Flight.

------------------------------------------------------------------------

# Transitional Development --- V5 / V6 Era

The V5/V6 development period concentrated heavily on presentation and on
moving the game toward the polished **Super Rooftop** look later
formalized in V7.

Not every intermediate build has a complete surviving release note, so
this section records confirmed project direction without assigning every
individual change to a specific minor build.

### Visual development

-   Continued refinement of 2.5D buildings.
-   More detailed city/parallax artwork.
-   Improved roof and building surfaces.
-   More convincing windows and façade depth.
-   Increasing use of rendered-looking game objects.
-   Continued player and collectible polish.
-   More rooftop props and environmental detail.
-   Continued desktop/mobile layout refinement.

### Gameplay retained and expanded

The established systems remained central: - Multi-level progression. -
Increasing hazards. - Power-ups. - Medical kits. - Force-field events. -
Flight events. - High scores. - Cosmetic progression. - Desktop and
mobile controls.

------------------------------------------------------------------------

# V7 --- Unified Art & Presentation

V7 was a major art-direction and presentation pass intended to make the
whole game feel like one consistent rooftop world.

## Modular rendered building system

The main building artwork was strengthened with reusable
rendered/procedural modules.

Rooftop and façade details include: - Water towers. - Skylights. -
Planters. - Vents. - Chimneys. - Antennas. - Fire escapes. -
Drainpipes. - Rooftop access doors. - Safety railings. - Pipe
clusters. - AC ducts and rooftop equipment.

## Unified collectible/power-up artwork

Power-up graphics were brought into a more consistent rendered visual
language.

The V7 power-art system covers: - Magnet. - Boost. - Shield. - Force
Field. - Flight. - Life/medical kit.

Existing rendered coin, mine, HVAC/obstacle, and medical-kit artwork
continued to be used where appropriate.

## Background-city correction

The distant/midground city artwork was extended downward so tall
displays no longer exposed a large band of sky underneath the background
buildings.

This preserved the skyline while keeping the lower portion of the world
visually filled with city architecture.

## Camera polish

Added: - Smooth horizontal camera easing. - Subtle forward look-ahead
based on player velocity. - Small landing bump on stronger landings. -
Adjustable player/camera framing.

## Centralized creator settings

The code was reorganized so useful creator-adjustable values live
together under:

`GAME SETTINGS - SAFE VALUES TO CHANGE`

Settings exposed there include: - World/level values. - Cosmetic
progression. - Time and bonus time. - Lives. - Power-up timing. - Hazard
start levels. - Player physics. - Scoring. - Camera behavior. -
HUD/message placement. - High-score behavior. - Secret flight code. -
Mobile layout controls.

## Adjustable message banner

Added a dedicated variable:

`MESSAGE_BANNER_Y`

The banner position is expressed as a fraction of screen height.

The current V7.5 value is:

`MESSAGE_BANNER_Y = 0.45`

Increasing it moves temporary bonus/power-up messages lower on the
screen.

## Maximum lives

Maximum lives were increased to:

`MAX_LIVES = 6`

## Desktop keyboard legend

Added a single-line desktop-only shortcut legend near the bottom of the
game.

The legend emphasizes shortcut letters in a larger golden-yellow style
rather than repeating the key separately.

Examples: - **P**ause - **H**ome / End Run - **R**estart

Movement and jump information remain in the same compact legend.

## HUD cleanup

Removed the upper-right eagle graphic.

Removed the redundant top pause icon on desktop, leaving Pause
represented by the keyboard legend.

## Score HUD redesign

The score display was redesigned into a more polished upper-right HUD
card.

The initial decorative coin icon was removed after it interfered
visually with the score text.

The final score card displays: - **SCORE** - Current score. - **BEST** -
Highest saved score.

------------------------------------------------------------------------

# V7.5 --- Current Development Build

V7.5 combines the V7 visual work with gameplay sequencing,
splash-screen, HUD, and mobile usability refinements.

## Force Field / Shield sequencing

Shield and Force Field had sometimes appeared too close together.

Force-field event levels were revised to create a clearer sequence:

**Force Field → minefield → Shield afterward**

On those event levels: - The normal rotating power-up is suppressed
before the minefield. - Force Field is collected first. - The player
crosses the minefield. - A normal Shield can appear afterward.

This makes the two defensive abilities serve different purposes.

## Current special-event structure

### Force Field

-   Temporary minefield protection.
-   Current duration: **7 seconds**.
-   Event repeats periodically once mines are active.

### Shield

-   One-hit protection.
-   Can be saved until needed.

### Flight

-   Temporary flight.
-   Current duration: **9 seconds**.
-   Used with special gaps that normal jumping cannot cross.

### Medical Kit

-   Appears every **3 levels**.
-   Adds one life up to the maximum of **6**.
-   Awards bonus points when already at full lives.

## New splash-screen system

The original splash/instruction artwork was replaced with a more
polished illustrated Rooftop Coins start screen matching the game's
current visual style.

The current splash emphasizes: - Rooftop Coins title. - Rooftop/city
artwork. - Running character and floating coins. - Large **START GAME**
button. - Desktop controls. - Large, recognizable power-up icons.

The later splash revision deliberately: - Removed the version number
from the artwork. - Removed unnecessary lower information rows. -
Reduced instructional clutter. - Kept the power-up guide prominent.

### Responsive splash repair

Earlier V7.5 splash experiments could be partially cropped on desktop or
mobile because the image proportions and viewport sizing did not agree.

The splash sizing logic was revised so the complete artwork can remain
visible and centered across different aspect ratios.

## Mobile portrait HUD repair

Portrait testing revealed overlap between: - Lives. - Coin
information. - Timer. - Level. - Score card.

V7.5 introduced dedicated portrait HUD scaling and positioning so these
elements occupy separate areas.

## Raised mobile R / P / E controls

The mobile action row was raised above the large movement controls.

This prevents: - Restart. - Pause. - End.

from crowding the bottom edge or overlapping the primary controls.

## Bottom fade/fog removal

The old lower-screen fade/fog graphic was removed.

Building and rooftop artwork now remains visible and crisp all the way
to the bottom of the viewport.

## Larger landscape touch controls

Landscape mode previously reduced the main touch buttons.

The latest V7.5 build increases the landscape controls to match the
larger portrait sizing:

-   **Left:** 78 × 78 px
-   **Right:** 78 × 78 px
-   **Jump:** 96 × 96 px

The smaller **R / P / E** action buttons remain compact to preserve
usable landscape screen space.

## Desktop HUD and legend

The current desktop presentation includes: - Lives. - Coin
information. - Timer. - Current level. - SCORE / BEST score card. -
Active power-up information. - Bottom keyboard shortcut legend.

## Current scoring

Current documented scoring includes: - Coin: **100 points** - Power-up
pickup: **200 points** - Perfect Jump: **250 points** - Close Call:
**150 points** - Full-life medical kit: **300 points** - Combo bonus
step: **25 points** - Combo window: **2 seconds**

## Current level/hazard progression

The current game supports up to **30 levels**.

Documented hazard progression: - Obstacles begin: **Level 2** - Mines
begin: **Level 4** - Moving obstacles begin: **Level 6** - Moving mines
begin: **Level 7**

## Current time/life defaults

-   Starting lives: **3**
-   Maximum lives: **6**
-   Starting Level 1 time: **60 seconds**
-   Final countdown: final **10 seconds**
-   Medical kit: every **3 levels**
-   Base level time bonus: **22 seconds**
-   Maximum level time bonus: **38 seconds**
-   Bonus increases every **2 levels**

## Current cosmetic progression

Persistent browser progression remains in place.

Current documented settings: - Character/outfit unlock: every **10
plays** - Background unlock: every **5 plays** - In-run cosmetic
progression: every **2 levels**

## High scores

The game stores up to **5 high scores**.

A qualifying score can prompt for a name of up to **10 characters**.

The highest saved score is displayed as **BEST** in the in-game HUD.

------------------------------------------------------------------------

# Current Controls --- V7.5

## Desktop

-   **A / D** or **Left / Right Arrow** --- Move
-   **W / Up Arrow / Space** --- Jump
-   Jump again while airborne --- Double jump
-   **P** --- Pause / Resume
-   **H** --- Home / End Run
-   **R** --- Restart
-   **67** --- Toggle secret flight mode

## Mobile

-   Large Left / Right buttons --- Move
-   Large Jump button --- Jump / Double jump
-   **P** --- Pause / Resume
-   Hold **R** --- Restart
-   Hold **E** --- End Run
-   **CODE** --- Enter secret flight code

------------------------------------------------------------------------

# Current Design Principles

The original foundation remains:

**Run → jump → collect → survive → advance**

Special events follow:

**Ability → challenge**

Examples: - **Force Field → minefield** - **Flight → otherwise
impossible gap** - **Shield → protection for a later hit** - **Medical
Kit → risk/jump for another life**

The goal is to add replay value and visual polish without making the
basic controls complicated.

------------------------------------------------------------------------

# Project / GitHub History

Rooftop Coins is organized as a GitHub Pages project.

Repository:

`assafavi/rooftop-coins`

Earlier project structure preserved major versions independently,
including V2 Classic, V3 Enhanced, and V4 Super Rooftop.

The current active development line is **Super Rooftop V7.5**.

A custom iPhone Home Screen icon was also created for the project.

------------------------------------------------------------------------

# Current Version

**Super Rooftop V7.5**

Latest documented refinements: - Responsive illustrated splash screen. -
No version number required on splash artwork. - SCORE / BEST HUD. -
Six-life maximum. - Force Field → minefield → Shield event flow. -
Centralized safe settings. - Desktop shortcut legend. - Improved
portrait HUD. - Raised portrait R / P / E buttons. - Bottom fade
removed. - Larger landscape Left / Right / Jump controls.

**Change log updated: September 29, 2026**

Future meaningful milestones should be added to this file so
`CHANGELOG.md` remains the permanent development history of Rooftop
Coins.
