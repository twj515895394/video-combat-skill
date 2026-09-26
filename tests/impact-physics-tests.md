# Impact / Contact Composition Regression Tests

## Case 0 — normal fight must not add an impact leaf by default
Request:
`10秒古代徒手武侠打斗。`

Expected:
- compact mandatory Impact Packet from `SKILL.md` is active,
- no automatic load of `composer/contact-impact-composer.md`,
- no automatic load of `core/contact-impact-physics.md`,
- every important C1-C3 contact still has a receiving point and physical consequence.

Reason:
impact quality is a universal composition rule, not a reason to spend an extra leaf on every fight.

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

## Case 8 — impact-focused generation uses Composer
Request:
`生成10秒拳拳到肉、撞击感很强的徒手打斗，重点是真实承受点和受力。`

Expected load:
- normal selected style/archetype as needed,
- `composer/contact-impact-composer.md` because impact authoring is the central requirement.

Normally not required:
- `core/contact-impact-physics.md`.

## Case 9 — failure diagnosis uses Core Physics
Request:
`这个生成视频打击看着像假的，分析为什么碰到了却没有重量。`

Expected load:
- `core/contact-impact-physics.md` for focused diagnosis,
- relevant original style only if needed.

Do not automatically load Composer unless the user also asks to rewrite/re-author the choreography.

## Case 10 — repair + re-author may choose Composer instead of Core
Request:
`这个视频打得很假，直接帮我重写提示词，让每次关键接触都有重量。`

Expected:
Prefer:
- `composer/contact-impact-composer.md`
for authoring the replacement prompt.

Do not automatically load both Composer and Core Physics.

## Case 11 — impact physics vs impact camera
Request:
`要拳拳到肉，但不需要特写。`

Expected:
- Composer may load because impact authoring is central,
- `directing/impact-inserts.md` is not required.

Request:
`拳拳到肉，而且关键一拳要拍拳打胸口的局部撞击特写。`

Expected:
- physical impact rules apply,
- Composer may load,
- `directing/impact-inserts.md` may also load if within budget.

## Case 12 — Contact classes control description density
Sequence contains:
- light wrist parry,
- hard forearm collision,
- solid palm to sternum,
- signature body-to-pillar impact.

Expected:
- C0 wrist parry stays concise,
- C1 block has collision/deceleration/line change,
- C2 palm has contact + local + structural + support consequences,
- C3 pillar impact gets full force-transfer detail.

Reject writing a full paragraph for every light touch or reducing all contacts to equally vague verbs.
