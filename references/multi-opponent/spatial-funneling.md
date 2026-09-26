# Multi-Opponent Spatial Funneling

Design the protagonist's route first. Enemies are scheduled around that route.

## Protagonist route first

Before techniques, define a simple route such as:
- lateral across corridor,
- around pillar,
- along table edge,
- through doorway,
- toward stairs,
- between crates,
- around railing.

The route should prevent the protagonist from standing still and fighting every enemy from one spot.

## Funnel principle

Environment should reduce how many enemies can enter the same attack lane at once.

Useful funnel geometry:
- pillar blocks one side,
- table forces detour,
- doorway narrows approach,
- crates split group,
- railing limits flank,
- wall protects one side,
- fallen body creates temporary obstacle.

The environment is not the star. It rewrites human trajectories.

## Spatial roles

Assign each enemy a lane:
- FRONT_LANE
- LEFT_FLANK
- RIGHT_FLANK
- REAR_APPROACH
- EXIT_BLOCK
- OBSTRUCTED

Only lanes with actual access should produce immediate attacks.

## Local compression

A nominal 1-vs-4 scene should repeatedly become local:
- 1-vs-1,
- 1-vs-2,
then reopen as protagonist moves.

This is achieved through geometry and displacement, not enemy politeness.

## Route-changing actions

Good protagonist actions:
- sidestep around pillar,
- move along table edge,
- pass through narrow gap,
- push one enemy into another lane,
- force one enemy into furniture,
- use wall/railing for momentary support,
- move behind obstacle only if camera preserves route.

## Downed / displaced bodies

An enemy who falls or is knocked aside becomes part of space:
- blocks route,
- forces others around,
- narrows attack lane,
- becomes foreground/background spatial anchor.

Do not make downed enemies vanish between shots.

## No prop-play detours

Avoid stopping the protagonist to perform long prop routines unless explicitly requested.

Prefer:
- hand brushes table for balance,
- shoulder glances pillar,
- foot plants briefly on step,
- enemy collides with doorframe,
- protagonist squeezes through gap.

## Spatial QC

At each major beat answer:
- where is protagonist moving?
- which 1-2 opponents currently have a clear lane?
- which opponents are blocked and by what?
- where can the protagonist move next?
- does the environment explain why the whole group cannot attack at once?
