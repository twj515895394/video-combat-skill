# Combat Expression Regression Tests

## Case 1 — readable close-up cannot be blank
Input:
`近景拍防守者连续闪避拳腿，脸部清晰。`

Expected:
- focused threat-aware gaze,
- restrained brow/jaw tension,
- head/eyes track the incoming threat,
- no mannequin-neutral face.

## Case 2 — no expression budget in irrelevant wide shot
Input:
`远景双人快速位移，脸很小。`

Expected:
- prioritize body mechanics / route / spatial state,
- do not waste prompt detail on facial micro-expression.

## Case 3 — attack effort is brief, not permanent rage
Input:
`中近景角色爆发一记重掌后继续追击。`

Expected:
- brief effort tension / short exhale around commitment,
- expression relaxes back toward focused combat state after effort,
- no permanent snarl or constant scream.

## Case 4 — impact reaction begins after contact
Input:
`近景拳击中上胸，脸部同时可见。`

Expected:
- impact occurs first,
- then blink/squint/jaw/breath reaction begins,
- no anticipatory recoil or facial grimace before contact.

## Case 5 — near miss changes gaze/expression
Input:
`脚从脸旁高速扫过但没有命中。`

Expected:
- eyes/head track or snap toward the threat line,
- brief squint/blink/tension is allowed,
- fighter immediately reacquires opponent,
- no exaggerated fear unless story requires it.

## Case 6 — recovery expression continuity
Input:
`角色被打退撞柱，切到近景恢复。`

Expected:
- breath disruption / tension may persist briefly from the impact,
- eyes reacquire the opponent,
- face does not instantly reset to beauty-neutral.

## Case 7 — control advantage is focused, not smiling by default
Input:
`角色抓腕控制对手，中近景能看到脸。`

Expected:
- calm focused control,
- gaze tracks controlled limb/opponent,
- no casual grin unless character/story explicitly requires it.

## Case 8 — gaze must respect combat-facing
Input:
`单人近景发起攻击，对手在画外右侧。`

Expected:
- eyes/head orient toward established off-screen opponent direction,
- no unexplained look into camera or opposite side.

## Case 9 — expression differs by event
Input:
`同一角色先近距离躲拳，再重掌发力，再被反击。`

Expected:
- threat focus / evade reaction,
- brief attack exertion,
- impact reaction,
are distinct states.
Reject one identical grimace through all three.

## Case 10 — routing isolation
Input:
`普通10秒武侠打斗，有一两个能看到脸的中景。`

Expected:
- core QC handles basic expression/gaze correctness,
- do not automatically load `composer/combat-expression-composer.md`.

Input:
`上一版视频近景全是木脸，眼神还看错方向，请重点修人物打斗表情。`

Expected:
- may load `composer/combat-expression-composer.md`,
- do not scan unrelated Style / Atomic references merely to repair facial acting.
