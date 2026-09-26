# Body Pose + Tempo Regression Tests

## Case 1 — side kick posture
Input:
“红衣男子右侧踹蓝衣胸口。”

Expected:
- right leg is explicitly the striking leg,
- left leg is support leg,
- support foot pivots enough to free the hip,
- right knee chambers before extension,
- heel is force line,
- torso becomes appropriately side-on without losing opponent awareness,
- recovery/landing is specified.

Reject:
- support foot frozen forward while hip fully rotates,
- support knee hyperextended,
- kick ends with fighter permanently back-facing,
- right leg magically becomes left leg.

## Case 2 — low sweep posture
Input:
“红衣低扫蓝衣支撑脚。”

Expected:
- center lowers first,
- one support leg bears body weight,
- pelvis rotates around support base,
- sweeping leg travels near floor,
- torso counterbalances,
- sweep finishes into a real planted/retracted exit.

Reject:
- both feet airborne,
- upright body with disconnected sweeping leg,
- instant reset to original stance.

## Case 3 — throw posture
Input:
“蓝衣把红衣摔出去。”

Expected:
- exact entry/contact,
- control/grip or body connection,
- off-balance direction,
- attacker's base/hip/leg relationship,
- throw path,
- landing orientation.

Reject:
- receiver floats before contact,
- throw begins from striking distance with no connection,
- attacker has no support base.

## Case 4 — fast two-person wide exchange
Input:
“10秒两人武侠打斗，电影感，正常速度。”

Expected:
- when both fighters are substantially visible, attack-defense-counter remains fast and continuous,
- no one waits motionless for a full opponent technique,
- next action grows from prior contact/miss/recovery,
- master shot is an anchor, not the entire clip.

Reject:
- A attacks, resets; B attacks, resets; repeated turn-taking,
- both fighters remain fully visible and slowly demonstrate one technique each.

## Case 5 — slow emphasis through close shot
Input:
“这一掌要有重量，让观众看清。”

Expected:
- keep surrounding fight at real-time speed,
- use a tighter contact/receiving-point/foot-reaction shot to emphasize the palm,
- do not slow the whole two-person wide exchange.

## Case 6 — attacker-only shot
Input:
“蓝衣突然冲上来出拳。”

Expected:
- valid to show blue dominating frame during acceleration,
- red may appear only as shoulder edge/foreground blur/off-screen established target,
- cut on extension to block/contact/result.

Reject:
- requirement that both full fighters and both faces always remain visible.

## Case 7 — defender-only result shot
Input:
“红衣被一掌打退撞柱。”

Expected:
- valid to cut to red recoil/boot skid/body-to-pillar result while attacker is partial/off-screen,
- attack direction remains spatially inferable,
- result begins only after established contact.

## Case 8 — named Yuen Woo-ping profile
Input:
“袁和平武侠电影风格，两人徒手快速打斗。”

Expected:
- fast complete-body attack-defense bursts,
- defense physically becomes counter,
- selective single-subject and contact/detail shots,
- tempo variation comes from action overlap and shot selection,
- no generic slow master-shot sparring.

## Case 9 — real slow motion explicitly requested
Input:
“最后一下重击用慢动作。”

Expected:
- slow motion limited to the decisive impact or receiving-body reaction unless user explicitly asks for a longer stylized slow-motion exchange,
- prior and following full-body fighting returns to real-time speed.

## Case 10 — routing isolation
Ordinary fast 1v1 should use compact Pose + Impact + Tempo rules from SKILL.md without automatically loading:
- body-pose-composer.md,
- contact-impact-composer.md,
- tempo-shot-composer.md.

Load a detailed Composer leaf only when the user explicitly prioritizes that domain or a previous generation failed in that domain.
