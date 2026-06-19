---
description: "Claude Code + Codex 실습 진행 — /lesson-cc-codex {레슨}"
allowedTools: Read, Write, Bash, Glob, Grep, AskUserQuestion
---

`SKILL.md` 의 lesson-cc-codex 엔진 절차를 따라 실습을 진행한다.

- 인자 = 레슨 id (`1-1`·`1-2`·`2-1`·`2-2`) 또는 `이어서`/`start`(프로필 기준 다음 레슨).
- `Read("SKILL.md")` 후 Step 0~3(인자 파싱 → 프로필 → 코스·레슨 로드 → 3-Phase 진행)을 그대로 수행.
- 예: `/lesson-cc-codex 1-1`, `/lesson-cc-codex 2-1`, `/lesson-cc-codex 이어서`.
