# Routing Isolation Tests

These tests verify that the Agent loads the smallest useful reference set and never follows leaf references transitively.

## Case 1 — simple boxing 1v1
Input:
“10秒拳击对打，A先攻，写实，一镜到底。”

Expected Load Manifest:
- `styles/boxing.md`
- optionally one archetype only if macro engine is not already obvious

Not expected:
- `style-index.md`
- `combinations/*` merely because continuity is required
- `directing/*` merely because output is video
- `core/*`
- `cinematic/*`

Leaf budget: <=4, normally 1-2.

## Case 2 — explicit southern fist vs northern long fist wuxia
Input:
“10秒古代庭院，蓝衣南拳，红衣北腿，红衣先攻，写实武侠。”

Expected:
- `styles/chinese/southern-nanquan.md`
- `styles/chinese/northern-longfist.md`
- optional `pairings/style-vs-style.md` if tactical range conflict is emphasized
- `cinematic/grounded-wuxia.md`

Not expected by default:
- `style-index.md` because exact styles are known
- `qinggong.md` unless actual elevated movement is requested
- generic Hong Kong camera file unless requested
- a Combination file unless a specific transition problem needs it
- Directing files unless cinematography is explicitly emphasized

## Case 3 — explicit qinggong
Input:
“南拳对长拳，庭院武侠，要踩柱和踩栏轻功换位。”

Expected:
- exact base styles
- `cinematic/grounded-wuxia.md`
- `cinematic/qinggong.md`
- optionally one spatial combination OR one directing file if needed

Qinggong is justified because elevated push-off is explicit.

## Case 4 — named Tsui Hark reference
Input:
“参考徐克新派武侠的拍摄感觉，南拳对北腿。”

Expected:
- exact base styles
- `directing/style-profiles/tsui-hark-new-wave-wuxia.md`
- optional `cinematic/grounded-wuxia.md` depending requested movement

Not expected:
- `directing/style-profiles/style-profile-index.md` because the profile is directly mapped
- `cinematic/hong-kong-action-language.md` because the specific profile supersedes generic Hong Kong camera language
- all Directing files

## Case 5 — impact close-up only
Input:
“拳打到胸口的时候要一个拳和胸口的特写。”

Expected:
- relevant base style only if needed
- `directing/impact-inserts.md`

Not expected:
- full `shot-pattern-library.md`
- camera-movement.md
- editing-rhythm.md
- style profiles

## Case 6 — one-vs-three generic
Input:
“10秒，一个人被三个人围攻，不能排队送，要持续压迫和走位。”

Expected:
- `archetypes/outnumbered.md`
- `multi-opponent/multi-opponent-router.md`
- `multi-opponent/active-attacker-scheduling.md`
- `multi-opponent/spatial-funneling.md`
- one base style if specified/needed

Not expected by default:
- all four multi-opponent leaves
- generic framing file
- combination files unless a specific transition issue exists
- style profile unless requested

Leaf budget: <=6.

## Case 7 — one-vs-many camera emphasis
Input:
“一个人打四个，镜头始终围绕主角，下一名敌人从画框边缘进入。”

Expected:
- `archetypes/outnumbered.md`
- `multi-opponent/multi-opponent-router.md`
- `multi-opponent/active-attacker-scheduling.md`
- `multi-opponent/protagonist-centric-directing.md`

Not expected:
- generic `directing/framing-and-subject-selection.md` unless another special framing problem is explicitly requested
- all multi-opponent leaves

## Case 8 — repair back-facing
Input:
“生成后一个人一直背对对手，修这个问题。”

Expected:
- `core/combat-facing.md`
- selected original style only if its stance/turning logic is relevant

Not expected:
- full style index
- all Core files
- Directing library unless camera itself caused the error

Repair leaf budget: <=3.

## Case 9 — repair camera readability
Input:
“动作没问题，但镜头一直挡住落脚和踢腿路线。”

Expected either:
- `core/action-camera.md` for generic readability repair,
OR
- exact relevant Directing file for specific cinematography repair.

Not expected by default:
- core/action-camera + several directing files simultaneously.

## Case 10 — broad Chinese martial arts request
Input:
“做一个中国武术打斗。”

Expected:
- brief clarification if style choice materially changes result,
OR
- `style-index.md` to choose one closest family if user delegates choice.

After selection:
- load one chosen Style leaf.

Not expected:
- several Chinese style leaves “for inspiration”.

## Case 11 — leaf cross-reference trap
Suppose `wuxia-courtyard.md` mentions a useful combination or compatible style profile.

Expected:
- do not follow that mention automatically.
- only files already authorized by the original Load Manifest may be read.
- if new need is discovered, return to root router, revise manifest, enforce budget, then add/swap one file.

## Case 12 — maintenance mode
Input:
“看这个参考视频有没有东西可以补进 reference 库。”

Expected:
- `reference-ingestion-pipeline.md`
- only exact target-local files for dedupe/merge, normally 1-3 leaves.

Allowed:
- broader repository review only if user explicitly asks for full routing/project audit.

Not expected:
- scanning every style/action/directing file for each extracted candidate.
