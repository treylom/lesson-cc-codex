# AGENTS.md — lesson-cc-codex (Codex 안내)

이 저장소는 **Claude Code(CC) + Codex 실습 스킬 `lesson-cc-codex`** 입니다. 비개발자 1인 사업자를 위한 터미널 실습 코스(cc-codex-101, 22 레슨 + 강의용 클립 13).

## Codex에서 쓰는 법
1. 이 저장소를 클론한 폴더에서 Codex를 실행합니다: `codex` (또는 `codex --cd <이 저장소 경로>`).
2. 스킬 호출: **`$lesson-cc-codex <레슨>`** (예: `$lesson-cc-codex codex-01`). `/skills` 로 목록도 볼 수 있습니다.
   - 스킬 정의 = [`.agents/skills/lesson-cc-codex/SKILL.md`](.agents/skills/lesson-cc-codex/SKILL.md)
   - 코스 콘텐츠 = [`courses/cc-codex-101/`](courses/cc-codex-101/)
3. 사용자(user) 전역 설치를 원하면 `.agents/skills/lesson-cc-codex/` 폴더를 `~/.agents/skills/lesson-cc-codex/` 로 복사하세요.

## Claude Code에서 쓰는 법
`/lesson-cc-codex <레슨>` (저장소를 `~/.claude/skills/lesson-cc-codex/` 로 클론하거나 플러그인으로 설치). 자세히 = [README.md](README.md).

## 전체 안내
설치·목차·트랙·보안·고급기능 = [MANUAL.md](MANUAL.md).

> 이 `AGENTS.md` 는 Codex가 스킬을 찾는 데 **필수는 아닙니다** — 스킬은 `.agents/skills/` 에서 자동 발견됩니다. 이 파일은 저장소를 연 사람을 위한 안내입니다.
