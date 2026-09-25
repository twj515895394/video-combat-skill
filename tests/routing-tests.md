# Routing Tests

## Case 1 — Boxing only
Input: "10秒拳击近身对打"
Expected:
- boxing.md
- optionally action-camera.md
Not expected:
- muay-thai.md
- sanda.md
- wuxia files

## Case 2 — Southern fist vs northern leg wuxia
Input: "蓝衣南拳，红衣北腿，10秒古代武侠徒手"
Expected:
- southern-nanquan.md
- northern-longfist.md
- pairings/style-vs-style.md
- grounded-wuxia.md
Optional:
- qinggong.md if actual elevated movement is requested
Not expected:
- boxing/mma/wrestling

## Case 3 — Muay Thai clinch
Input: "泰拳肘膝连续压制"
Expected:
- muay-thai.md
Optional:
- core/biomechanics.md for repair
Not expected:
- kickboxing.md merely because kicks exist

## Case 4 — Sanda catch and throw
Input: "散打接腿后摔"
Expected:
- sanda.md
- core/biomechanics.md if detailed throw reliability is needed
Not expected:
- wrestling-grappling.md unless the user asks for deeper grappling mechanics

## Case 5 — Video failure: fighter back-facing
Input: "为什么生成后一人一直背对另一个人"
Expected:
- core/combat-facing.md
- original selected style file if needed
Do not scan all styles.

## Case 6 — Wuxia alone
Input: "做一个武侠打斗"
Expected:
- router identifies missing base movement language
- choose a reasonable broad Chinese base based on user's described action, or use style-index if genuinely ambiguous
- load grounded-wuxia only as cinematic layer
Never treat wuxia as sufficient base mechanics by itself.
