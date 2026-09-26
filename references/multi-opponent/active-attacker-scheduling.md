# Active Attacker Scheduling

The purpose of this file is to prevent turn-based one-vs-many choreography.

## Attack-right overlap

The next attacker should often begin entering before the current attacker has fully exited.

Good pattern:
- Enemy A attacks.
- Protagonist evades/redirects A and is still moving from that response.
- Enemy B begins entering during A's recoil/recovery.
- Protagonist changes target because B creates the new immediate threat.

Bad pattern:
- A attacks.
- A fully stops.
- protagonist resets.
- B walks in and attacks.

## Default active budget

At any instant:
- 1 ACTIVE_ATTACKER is safest,
- 2 ACTIVE_ATTACKERS may overlap briefly,
- 3+ simultaneous full attacks are usually unstable for short AI video unless explicitly choreographed and spatially separated.

## Overlap types

### AS-01 Resolve-to-Entry Handoff
A's attack is blocked/missed/redirected.
Before A fully recovers, B enters from a new lane.

### AS-02 Impact-to-Secondary Threat
Protagonist hits A and A recoils.
B uses the protagonist's follow-through/recovery moment to enter.

### AS-03 Evasion-to-Cutoff
Protagonist evades A by moving laterally.
B, already approaching from the new side, becomes immediate threat.

### AS-04 Grab-to-Interruption
A briefly grabs/frames protagonist.
Before the interaction becomes static, B's approach forces protagonist to break/redirect A and move.

### AS-05 Displaced Enemy -> Reentry Later
A is shoved/knocked behind obstacle or out of immediate lane.
A becomes RECOVERING / TEMPORARILY_DISPLACED rather than permanently eliminated.
A may reenter several beats later from a physically plausible route.

## Supporting attacker behavior

Non-active opponents should visibly do useful things:
- close distance,
- circle toward exit,
- recover from prior hit,
- step around furniture,
- appear at frame edge,
- reach but not yet make full contact,
- block escape route,
- become partially occluded.

They should not freeze in a waiting pose.

## Initiative pressure

The protagonist should rarely have time to pursue one enemy for a long finish.
A new threat often forces target switch.

This is the core of cinematic one-vs-many pressure.

## Breathing beat

A very short beat may occur for:
- stumble recovery,
- one sharp breath,
- head/eye snap toward next threat,
- quick spatial read,
- hand catching wall/table.

This is not an idle reset. It must directly reveal or enable the next threat.

## AI failure modes

- enemies politely queue with visible waiting,
- every enemy mirrors the same attack,
- all enemies rush at once and merge bodies,
- protagonist magically switches target without head/body reorientation,
- defeated enemy disappears without spatial reason,
- recovered enemy reappears from impossible direction.
