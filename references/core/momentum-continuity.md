# Momentum Continuity

Use when generated combat feels turn-based, poses between attacks, or resets after every move.

## Zero Idle engine

Every beat follows:

`threat -> response -> changed state -> continuation`

Changed state can be:
- range,
- angle,
- height,
- balance,
- trapped limb,
- clinch,
- wall contact,
- landing,
- overrotation,
- shell posture,
- failed shot position.

## Momentum conversion patterns

### Miss -> continuation
A missed kick lands forward, creating a new stance rather than retracting to reset.

### Parry -> entry
A parried straight punch leaves the attacking shoulder extended; defender uses the opened line to step in.

### Impact -> pursuit
Receiver stumbles backward; attacker follows the backward movement rather than waiting.

### Wall contact -> rebound
A shoulder/back touches wall; compressed posture becomes push-off or clinch frame.

### Landing -> next action
Knees absorb landing; the loaded leg immediately drives the next step or strike.

### Failed takedown -> clinch
Shot stalls; head/arm/body contact becomes over-under or body-lock position instead of separation.

## Initiative changes

Initiative should flip for a reason:
- overcommitment,
- trapped limb,
- failed kick,
- off-balance landing,
- angle loss,
- wall/obstacle,
- caught kick,
- failed shot,
- broken posture.

Do not alternate offense simply for fairness.

## 10-second density

Prefer 3 kinetic phases:
- opening pressure,
- conversion / spatial change,
- escalation / counter-conversion.

The sequence can contain multiple action nodes, but each should inherit the previous state.
