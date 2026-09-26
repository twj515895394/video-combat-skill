# Reference-Film Pattern Tests

These tests validate reusable mechanisms extracted from supplied fight-film references. They test abstractions, not scene copying.

## Case 1 — Foreground limb barrage
Input:
"攻击者连续腿攻，但不要一直双人全身同框。"

Expected:
- may use SP-24 Foreground Limb Barrage,
- defender remains readable in mid-ground,
- attacker's leg/foot can dominate foreground while attacker is partial/off-screen,
- attack direction remains spatially consistent,
- no unexplained extra limbs,
- relation shot only re-establishes after meaningful spatial change.

## Case 2 — Body-evasion-first Tai Chi defense
Input:
"太极式连续化解快速腿攻，不要硬挡。"

Expected:
- torso/head clears attack line before or while contact occurs,
- feet/hips preserve a usable base,
- hand/forearm contact guides rather than stops the limb,
- attacker retains momentum and must overstep/overrotate/recover,
- no slow-motion decorative push-hands,
- no supernatural displacement.

## Case 3 — Borrowed-momentum redirection
Input:
"对方高速冲过来，防守者借力改变方向把他带偏。"

Expected:
- original attacker momentum is described,
- defender clears or changes angle,
- exact guiding contact is described,
- vector changes rather than force disappearing,
- attacker's center of mass/support fails to match new line,
- result is overstep/rotation/displacement/recovery,
- a light touch alone cannot cause huge knockback.

## Case 4 — Long shot can remain fast
Input:
"连续3秒不切镜，但动作必须很快。"

Expected:
- continuous high-density action is allowed,
- multiple attack-defense nodes occur without neutral reset,
- one fighter may become partial/off-screen during parts of the shot,
- camera does not slow choreography merely because shot duration is long.

## Case 5 — Information-driven cut
Input:
"什么时候应该从大全景切到特写？"

Expected:
Cut only when information changes, e.g.:
- spatial relation -> threat,
- threat -> contact,
- contact -> result,
- full-body route -> exact foot/hand mechanics,
- body action -> environment consequence.

Do not cut because a fixed second count elapsed or every technique ended.

## Case 6 — Asymmetric shot duration
Input:
"10秒动作片不要平均分成5个2秒镜头。"

Expected:
- shot lengths may differ substantially,
- a 2.5-4s continuous fight exchange can coexist with 0.3-0.8s inserts,
- short shot does not automatically mean fast body motion,
- long shot does not automatically mean slow body motion.

## Case 7 — Pose correctness vs camera visibility
Input:
"镜头只拍上半身和前景踢腿，还要保证腿法正确。"

Expected:
- internal Pose Packet still resolves support foot, knee, hip, torso, recovery,
- the camera does not need to show every biomechanical component simultaneously,
- hidden mechanics remain physically coherent across shots,
- filmmaking is not turned into an instructional full-body demonstration.

## Case 8 — No scene copying
Input:
"参考某个提供的电影打斗片段。"

Expected:
- extract reusable mechanics/directing principles,
- do not reproduce the exact shot order or exact choreography,
- route principles into existing Style / Composer / Directing assets when possible,
- only create a new asset when the mechanism is genuinely reusable and not already represented.
