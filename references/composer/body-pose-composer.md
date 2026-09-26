# Body Pose / Keyframe Composer Protocol

This is a composition protocol for technically readable martial-arts body posture.

Purpose: prevent AI video from producing a move whose name is correct but whose body posture is anatomically or mechanically wrong.

The compact mandatory version should live in `SKILL.md`. Load this detailed file only when posture accuracy is central, when a complex technique is used, or when a previous generation shows broken limb/body geometry.

## 1. Core principle

A martial-arts technique is not a pose name. It is a sequence of mechanically connected body states.

For any important technique, internally resolve:

`START -> LOAD / CHAMBER -> EXECUTION PATH -> CONTACT / PEAK -> RECOVERY / LANDING -> EXIT`

Not every phase must be written verbosely in the final prompt, but the body states must be physically compatible.

## 2. Mandatory internal Pose Packet

```yaml
pose_packet:
  technique:
  phase:
  lead_side:
  support_base:
  weight_distribution:
  support_foot_orientation:
  free_or_striking_foot:
  knees:
  pelvis_hips:
  torso:
  shoulders:
  elbows:
  hands_guard:
  head_gaze:
  center_of_mass:
  opponent_relation:
  balance_condition:
  next_pose_link:
```

Do not print this YAML unless the user requests technical diagnostics.

## 3. Body-pose invariants

These are cross-style safety/biomechanics constraints. A Style leaf may vary appearance, but should not violate basic anatomy.

### Feet / base
- Every major force-producing action has a readable support base.
- A planted foot cannot rotate independently while the knee remains locked in an incompatible direction.
- Large hip rotation normally requires support-foot pivot, heel release, stance adjustment, or another plausible way to free the hip.
- Feet do not cross accidentally during active striking unless the technique explicitly requires a crossing step.

### Knees
- Knee direction should broadly track the supporting foot / intended load line.
- Avoid inward knee collapse under heavy support unless it is an intentional loss-of-balance state.
- Kicks and level changes must not hyperextend the support knee.

### Pelvis / hips
- Hips transmit force between ground and striking limb.
- Kicks must identify how the pelvis turns, opens, drives forward, or remains square according to technique.
- Throws need a believable hip / center relationship before rotation or lift.

### Torso / spine
- Torso rotation follows the kinetic chain rather than twisting independently of pelvis/feet.
- Lean is allowed only when balanced by support base and technique purpose.
- Avoid extreme spine bending merely to make a kick reach higher.

### Shoulders / arms
- Shoulder position must match the striking path.
- Elbows should remain anatomically connected to shoulder/wrist geometry; avoid impossible backward elbow bends or detached arm arcs.
- The non-striking hand should have a plausible balancing / guarding / controlling role rather than disappearing.

### Head / gaze
- Head/gaze remains opponent-aware unless a technique requires a brief turn.
- Spinning/back techniques need explicit visual reacquisition of the opponent.
- Do not force the chest to face front if the technique mechanically requires side-on hip rotation; preserve head/gaze and attack-line awareness instead.

### Center of mass
- The center of mass must remain over or travel toward a plausible support region.
- One-leg techniques need a clear support leg and compensating torso/hip position.
- Landing/recovery must restore a usable base before the next high-force action.

## 4. Pose description levels

### P0 — simple upper-body action
Examples: short parry, palm guide, light jab.
Minimum:
- stance / facing,
- striking/defending arm path,
- shoulder/torso relation,
- exit guard.

### P1 — standard strike
Examples: straight punch, hook, palm, elbow, front kick.
Minimum:
- support base,
- hip/torso contribution,
- limb path,
- contact posture,
- recovery / exit.

### P2 — complex lower-body / rotational action
Examples: side kick, round kick, low sweep, spinning kick.
Require explicit key poses:
- start,
- chamber/load,
- peak/contact,
- landing/recovery.

### P3 — throw / takedown / aerial action
Require explicit relative-body key poses:
- entry,
- connection / control,
- off-balance / push-off,
- execution peak,
- landing / exit.

## 5. Keyframe authoring format

For a complex action, author internally as:

```text
START POSE
- feet / lead side
- weight
- guard / gaze

LOAD / CHAMBER POSE
- support leg
- knee / hip organization
- torso / shoulder preparation

CONTACT / PEAK POSE
- striking or control surface
- pelvis / torso orientation
- support base
- head / gaze

RECOVERY / LANDING POSE
- where the attacking limb goes
- which foot lands first
- how the center of mass is absorbed

EXIT POSE
- final facing
- final lead/rear foot relation
- balance
- distance
- next available action
```

## 6. Example — rear straight punch

Start:
- rear hand near guard,
- lead side slightly forward,
- knees soft,
- weight balanced enough to drive from rear side.

Execution:
- rear foot / hip / shoulder contribute in sequence,
- fist travels direct path,
- rear shoulder advances,
- lead hand remains guard / counterbalance.

Contact:
- wrist remains aligned behind striking surface,
- torso is rotated but not over-twisted,
- rear heel may release/pivot depending style.

Exit:
- hand retracts or becomes frame,
- hips/feet remain usable for next action.

## 7. Example — side kick

Start:
- opponent at kicking range,
- support foot ready to pivot,
- attacking leg free.

Chamber:
- attacking knee rises and folds toward target line,
- support foot turns enough to free the hip,
- pelvis becomes more side-on,
- torso counterbalances without collapsing.

Peak/contact:
- heel is primary line of force,
- support leg remains stable and not hyperextended,
- hip drives through heel line,
- head/gaze remains aware of opponent,
- hands stay in plausible guard/balance position.

Recovery:
- kicking knee refolds before full retraction OR the foot lands deliberately according to choreography.

Exit:
- torso and feet reorient to a usable fighting relationship.

## 8. Example — low sweep

Start:
- center lowers first,
- support leg carries body weight.

Execution:
- pelvis rotates around support base,
- sweeping leg extends near the floor,
- torso counterbalances rotation,
- head remains aware of opponent.

Peak:
- sweeping leg passes through the opponent's support-foot line.

Exit:
- sweeping leg completes the arc and either plants or retracts into a stable base.
- Do not magically return to original stance.

## 9. Example — forearm check

Start:
- defender remains balanced and opponent-facing.

Contact posture:
- forearm meets the incoming limb with elbow slightly flexed rather than locked,
- shoulder stays structurally connected to torso,
- opposite hand remains available,
- feet absorb / redirect force according to direction.

Exit:
- checking arm finishes on a line that can frame, parry, trap, or recover.

## 10. Style-specific variation

The Pose Composer defines biomechanical invariants, not one universal martial-art form.

Style reference may modify:
- stance width,
- torso angle,
- guard height,
- chamber height,
- degree of hip turn,
- weight bias,
- preferred recovery.

If style-specific technical certainty is not available, use a conservative mechanically plausible choreography model and do not claim lineage-level authenticity.

## 11. Prompt compression

Do not dump every joint description into the final prompt.

For simple actions:
- state only the pose features needed to avoid ambiguity.

For complex/high-risk actions:
- explicitly include support foot, chamber/load, hip/torso orientation, striking limb path, landing/recovery.

## 12. AI failure modes

Reject / repair:
- kick with no support leg,
- support foot facing forward while hips rotate unrealistically through a full side/round kick,
- knee collapsing inward under load,
- torso twisting opposite the pelvis with no mechanical reason,
- striking arm detached from shoulder rotation,
- non-striking hand disappearing / duplicated,
- spinning action ending permanently back-facing,
- kick leg changing sides mid-action,
- sweep with both feet airborne,
- throw occurring before grip / off-balance / body positioning,
- landing directly into another power move with no base recovery.
