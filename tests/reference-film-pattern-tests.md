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

## Case 9 — Full-body two-shot is not default cinematic coverage
Input:
"做影视级双人武侠打斗。"

Expected:
- establish spatial relation with wide/medium-wide only when needed,
- do not keep both full fighters visible for most of the fight,
- after geography is clear, prefer single-subject / partial / contact / control / reaction / result shots,
- do not return to wide after every exchange,
- reject sports-broadcast-style coverage unless explicitly requested.

## Case 10 — State-change cut
Input:
"两人高速拳掌攻防，随后一人突然抓住对方手腕进入控制。"

Expected:
- fast free striking may remain in a continuous wider/medium passage,
- the wrist capture is recognized as a physical relationship state change,
- cut may move to hand/wrist/forearm control detail,
- next shot may show opponent-only off-balance/result,
- do not cut simply because each earlier punch/palm ended.

## Case 11 — Visual Anchor Fighter
Input:
"连续攻击很快，但观众要能一直看清防守者的化解。"

Expected:
- defender may remain mid-ground visual anchor,
- attacker may be fragmented into foreground limbs / frame-edge entries / partial body,
- attack side remains consistent,
- camera does not need to keep both full bodies visible,
- visual anchor may transfer after initiative/state changes.

## Case 12 — Contact relay / no guard reset
Input:
"连续手上攻防，不要一挡就收手再重新摆架。"

Expected:
- contact exit becomes next contact start when style/range permit,
- a guiding hand may remain connected / become frame or control,
- the other hand can receive the next threat while the first contact is resolving,
- no automatic return to neutral guard after every touch,
- no impossible simultaneous unrelated motion.

## Case 13 — Control mechanics insert
Input:
"抓腕转臂这一下要让观众看懂。"

Expected:
- may use SP-26 Control Mechanics Insert,
- frame can contain only hands/wrist/forearm/shoulder edge,
- exact control direction is readable,
- full-body view is not mandatory if broader geography is already known,
- internal full-body balance remains coherent.

## Case 14 — Result-only follow-up
Input:
"已经拍清楚抓腕和带转，下一镜只看对手失衡。"

Expected:
- may use SP-27 Result-Only Follow-up,
- controller may be fully off-screen,
- receiver's rotation/step/fall follows the established cause/vector,
- no redundant return to two-person master shot.

## Case 15 — Decisive mechanic proof
Input:
"复杂动作是不是必须每次都拍全身？"

Expected:
No.
- prove the body region that makes the decisive mechanic understandable,
- kick may need foot/hip/leg proof,
- wrist control may only need hands/wrist/forearm,
- throw usually needs hips/feet/base removal,
- impact result may show only receiver/environment,
- internal Pose Packet remains complete regardless of crop.

## Case 16 — Sports-like coverage failure
Input:
"成片动作挺快，但几乎全程都是两个人完整全身同框，看起来像格斗比赛。"

Expected repair:
- treat this as cinematic coverage/tempo-shot failure even if body speed is fast,
- prefer `composer/tempo-shot-composer.md` or targeted framing patterns rather than adding more martial-art references,
- reduce unnecessary master-shot dependency,
- add single-subject / foreground / control / result information without breaking geography.
