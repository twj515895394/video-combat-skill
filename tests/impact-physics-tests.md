# Impact Physics Regression Tests

## Case 1 — vague torso hit must fail
Input choreography:
`Blue counters with a right palm strike to Red's chest.`

Expected:
Fail QC unless expanded with:
- exact receiving point,
- force direction,
- local compression,
- receiver posture/balance consequence,
- attacker contact/recoil/follow-through.

Example acceptable structure:
`Blue's right palm heel drives into Red's upper sternum; the robe dents inward, Red's shoulders recoil and his spine inclines backward, forcing his rear foot to slide one short step to catch his center of mass.`

## Case 2 — weightless block must fail
Input:
`Red cross-blocks Blue's side kick.`

Expected:
Fail QC if no collision mechanics exist.

Acceptable structure must include:
- kick receiving surface on forearms,
- abrupt deceleration,
- guard/torso compression,
- attack-line redirection,
- stance/foot consequence.

## Case 3 — dense action is allowed
Input:
10-second sequence with many connected attacks, checks, kicks and counters.

Expected:
Do not reject merely for high action count.
Pass when:
- actions form continuous kinetic phases,
- major contacts have distinct receiving points/results,
- minor contacts use concise but readable line changes,
- no pose/reset gaps.

## Case 4 — every hit cannot use same reaction
Input:
three solid contacts in one sequence.

Expected:
Reactions should depend on contact geometry:
- sternum hit -> backward shoulder/spine recoil,
- rib hit -> lateral torso fold/rotation,
- low kick -> weight shift/knee/support-leg reaction.

Reject identical generic backward glide after every hit.

## Case 5 — attacker also reacts to contact
Input:
solid palm or kick lands.

Expected:
Attacker limb/body must decelerate, compress into target, recoil, redirect or follow through.
Reject strike passing through receiver with unchanged velocity.

## Case 6 — environment impact
Input:
fighter is driven into wooden pillar.

Expected:
Show:
body arrival -> exact contact -> wood vibration/splinter or dull thud -> torso compression/recoil -> hand/foot recovery state.

Reject pillar damage occurring before contact.

## Case 7 — near miss still changes state
Input:
kick misses ribs by inches.

Expected:
Show at least:
- defender torso/cloth reacting to passing line,
- kicker overextension/retraction/forced landing,
- new stance/range for continuation.

## Case 8 — impact physics vs impact camera
Request:
“打击看着像假的，但不需要特写。”

Expected load:
- `core/contact-impact-physics.md`
Not required:
- `directing/impact-inserts.md`

Request:
“除了打击物理，还要拳打胸口的局部撞击特写。”

Expected:
- physical impact rules apply,
- `directing/impact-inserts.md` may also load if within budget.
