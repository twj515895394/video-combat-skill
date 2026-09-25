# Combination Routing Tests

## Case 1 — Boxing continuous pressure
Input: "拳击10秒，不要一拳一停，要一直压着打"
Expected:
- styles/boxing.md
- combinations/pressure-chains.md
Optional:
- actions/hand-strikes.md if exact punch mechanics are requested
Not expected:
- unrelated styles

## Case 2 — Defense becomes counter
Input: "对方直拳打来，闪开以后马上反击"
Expected:
- selected style
- combinations/counter-conversions.md
- optionally actions/defense-counter.md

## Case 3 — Sanda kick catch throw
Input: "散打接住腿以后顺势摔"
Expected:
- styles/sanda.md
- combinations/clinch-throw-transitions.md
- optionally actions/defense-counter.md + actions/throws-takedowns.md

## Case 4 — Nanquan vs northern leg
Input: "南拳不断贴身，北腿不断拉开距离"
Expected:
- southern-nanquan.md
- northern-longfist.md
- pairings/style-vs-style.md
- combinations/range-conversions.md

## Case 5 — failed kick should continue
Input: "踢空以后不要停，顺势继续打"
Expected:
- relevant style
- combinations/recovery-failure-chains.md
Optional:
- kicks-knees.md

## Case 6 — wuxia pillar / railing combat
Input: "古代武侠，借柱、踩栏，但不能乱飞"
Expected:
- concrete Chinese base style(s)
- cinematic/grounded-wuxia.md
- cinematic/qinggong.md only if elevated motion is actually requested
- combinations/wuxia-spatial-chains.md
- core/aerial-motion.md only if repair/detail is needed

## Case 7 — fixed combo should not become universal
Source reference shows one exact movie sequence:
kick -> spin -> vault -> elbow.

Expected:
- extract individual mechanics and state changes,
- only create a COMBINATION asset if the causal structure is reusable,
- do not store the exact movie choreography as a universal combo.
