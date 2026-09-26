# Multi-Opponent Routing & QC Tests

## Case 1 — simple 1v3
Input:
"一个人打三个，10秒，徒手，不能像排队送人头。"

Expected:
- archetypes/outnumbered.md
- multi-opponent/multi-opponent-router.md
- active-attacker-scheduling.md
- spatial-funneling.md if environment exists
- protagonist-centric-directing.md if cinematic camera is requested

QC:
- usually 1 active attacker,
- at most 2 brief overlapping attackers,
- remaining enemies have active states.

## Case 2 — enemy B enters before A finishes
Input:
"主角刚闪开A，B马上从侧面打进来。"

Expected:
- active-attacker-scheduling.md
- handoff occurs during A recovery rather than after reset.

## Case 3 — environment compresses 1v4
Input:
"主角在有柱子和桌子的酒楼被4个人围攻。"

Expected:
- outnumbered.md
- spatial-funneling.md
- environment-driven archetype only if environment is the primary scene engine; otherwise keep outnumbered as primary
- environment makes local 1v1 / 1v2 lanes.

## Case 4 — supporting enemies partially visible
Input:
"不要所有敌人一直完整同框，要有从画面边缘和柱子后进来的。"

Expected:
- protagonist-centric-directing.md
- current attacker readable,
- next attacker may appear as partial limb/shoulder/half-body.

## Case 5 — recovering enemy returns
Input:
"被打退的人过几秒还能重新回来。"

Expected:
- recovery-reentry-and-sound.md
- enemy must reenter from plausible prior side/route,
- no teleporting behind protagonist.

## Case 6 — protagonist gets hit
Input:
"主角不要无伤，要被打中一次但动作继续。"

Expected:
- protagonist damage changes balance/position,
- next threat exploits or reacts to that changed state,
- no instant reset.

## Case 7 — off-screen threat sound
Input:
"下一名敌人还没完全入镜，但先听到跑步声。"

Expected:
- recovery-reentry-and-sound.md
- sound direction must match plausible entry route,
- visual reveal follows spatially consistent path.

## Case 8 — invalid synchronized rush
Input:
"四个人同时从四面扑上去。"

If user explicitly requires it:
- choreograph lane separation very carefully,
- otherwise prefer staggered overlap for AI stability.

QC should flag body-merging risk and unreadable simultaneous active attackers.

## Case 9 — 10-second flow
Input:
"10秒一打三，持续有压力。"

Expected macro flow:
- 0-3s first attack + next attacker begins entry,
- 3-6s route/funnel change + target handoff,
- 6-10s renewed overlap / reentry / breakout.

Time bands are guidance, not rigid checkpoints.

## Case 10 — not every enemy defeated
Input:
"不用把三个人都打倒。"

Expected:
- enemies may be staggered, displaced, blocked or recovering,
- downed/displaced bodies remain spatial conditions.
