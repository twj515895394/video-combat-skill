---
id: sanda
family: striking-throwing
aliases: [Sanda, Sanshou, 散打, 散手]
primary_range: kicking-punching
secondary_range: catch-throw
stance_bias: mobile balanced
movement_signature: fast entry-exit, kick-punch transitions, kick catches, off-balancing throws
primary_tools: [side kick, round kick, straight punches, hooks, sweeps, catches, throws]
defensive_tools: [step evasion, parry, catch, body turn, off-balance]
grappling_level: standing-throw medium-high
aerial_level: low
ai_generation_risk: medium-high
load_when: user requests Sanda or Chinese sport striking with throws
do_not_load_when: prolonged ground grappling is central
---

# Sanda

## Style DNA
- Striking and standing takedowns connect directly.
- Distance can collapse rapidly after a kick is caught.
- Side kick is visually useful for long-range interruption.
- Throws should emerge from catches/body contact rather than telekinetic flips.
- Footwork is mobile and pragmatic.

## Range Model
Outside: side kick / round kick.
Mid: punches.
Transition: catch kick / body contact.
Close: sweep / trip / throw.
Ground phase is normally not the identity here.

## Action Cards

### SD-SIDE-KICK
Support foot pivots; chambered knee points toward target; heel extends linearly.
Useful for stopping forward motion.
Exit: retract or land forward into hands.

### SD-KICK-CATCH
Defender shifts off direct impact line, secures attacking lower leg against forearm/body.
Catching must follow readable contact.
Result: kicker becomes one-leg balanced and must hop, frame or counter.

### SD-CATCH-SWEEP
From captured leg, defender controls upper body/leg while stepping to remove supporting base.
Result: opponent falls because support is taken, not because arms throw them through space.

### SD-BODY-THROW
Entry requires torso/arm contact and off-balance direction.
Specify attacker's hip/leg position and receiver landing.

## Combination Grammar
- side kick disrupts advance -> hands enter as foot lands.
- opponent round kick -> catch after partial evasion -> supporting leg exposed -> sweep.
- punch pressure -> opponent shells -> level/angle changes into body contact -> throw.
- failed throw -> release/strike exit rather than static wrestling.

## Tactical Failure Conditions
- prolonged clinch without off-balancing stalls style identity,
- long ground sequence belongs to MMA/grappling instead,
- catches without impact-line evasion look physically impossible.

## Camera Proof
Throws require full body and floor visibility. Catch sequence should show kick line before close-up.

## Prompt Vocabulary
heel-driven side kick, kick catch against forearm and ribs, supporting-leg sweep, standing off-balance, short punch-to-throw transition.
