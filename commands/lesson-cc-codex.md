---
description: "Claude Code + Codex 실습 진행 — /lesson-cc-codex {레슨}"
allowedTools: Read, Write, Bash, Glob, Grep, AskUserQuestion
---

`SKILL.md` 의 lesson-cc-codex 엔진 절차를 따라 실습을 진행한다.

- 인자 = 레슨 id, 또는 `이어서`/`start`(프로필 기준 다음 레슨 자동 제안).
  - **자습(풀버전)**: `cc-01`~`cc-11`, `codex-01`~`codex-11` (총 22)
  - **강의용(클립)**: `cc-fc-1`~`cc-fc-7`, `codex-fc-1`~`codex-fc-6`
- `Read("SKILL.md")` 후 Step 0~3(인자 파싱 → 프로필 → 코스·레슨 로드 → 3-Phase 진행)을 그대로 수행.
- 예: `/lesson-cc-codex cc-01`, `/lesson-cc-codex codex-01`, `/lesson-cc-codex cc-fc-1`, `/lesson-cc-codex 이어서`.

> 막히거나 궁금하면 `/lesson-help <질문>` — 학습 도우미가 자유 Q&A로 답합니다(레슨 진행과는 별개).
> Codex에서는 `$lesson-cc-codex <레슨>` (자세히 = `AGENTS.md` · `MANUAL.md`).
