---
id: qinggong
type: cinematic-layer
aliases: [轻功, qinggong]
requires_base_style: true
ai_generation_risk: high
---

# Qinggong for AI Video

Treat qinggong as controlled cinematic locomotion rather than free flight unless the user explicitly wants fantasy.

## Levels

### QG-1 Grounded
- enhanced running step,
- short vault,
- railing step,
- pillar rebound,
- one-body-length lateral leap.

Best default for AI stability.

### QG-2 Elevated
- two-step wall/pillar run,
- longer roof/railing gap,
- brief aerial kick with clear landing.

Use sparingly.

### QG-3 Fantastical
- extended glide,
- rooftop-to-rooftop flight,
- prolonged air combat.

Only when explicitly requested; higher hallucination risk.

## Mandatory card

For every qinggong beat define:
- support_surface,
- push_off_foot,
- body_orientation,
- trajectory,
- opponent_status,
- landing_foot,
- exit_facing.

## One-airborne-subject default

When Fighter A performs qinggong, Fighter B normally stays grounded:
- pursues,
- tracks,
- attacks landing zone,
- evades,
- cuts off route.

This prevents synchronized hopping.

## Good choreography examples

- defender is pressured toward pillar -> right foot plants on pillar -> lateral rebound clears low sweep -> left foot lands first -> torso reorients opponent.
- attacker retreats onto railing -> left foot compresses on stone -> forward-down leap with kick -> defender stays grounded and angles off -> attacker lands forward.

## Bad language

- flies around him,
- floats over opponent,
- gracefully circles in the air,
- both leap into the sky,
- spins repeatedly while airborne.

## Camera

Show support and landing at least once in a qinggong chain.
Close-up may show foot plant; wide/full-body must prove trajectory.

## Prompt vocabulary

brief qinggong burst, visible push-off, single airborne trajectory, short wall step, lateral pillar rebound, weighted two-foot/one-foot landing, no hovering.
