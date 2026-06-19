# memory-schema — 수강생 프로필 (lesson-cc-codex)

> 저장 위치: `.lesson-memory/{이름}-cc-codex-101.json` (수강생 작업 폴더 기준). SKILL.md Step 1 에서 생성·로드.

## 필수 필드 (매 세션)
```json
{
  "name": "김신입",
  "course_id": "cc-codex-101",
  "ai_level": "beginner",
  "created_at": "2026-06-18",
  "updated_at": "2026-06-18"
}
```
- `ai_level` ∈ `beginner | intermediate | advanced`.

## 선택 추적 필드 (세션 간 누적)
```json
{
  "company_role": "제조업 / 운영기획 실무",
  "completed_lessons": ["1-1", "1-2"],
  "struggles": ["터미널 명령", "git 개념"],
  "strengths": ["프롬프트에 배경 잘 줌", "빠른 이해"],
  "preferences": {
    "pace": "slow | normal | fast",
    "examples": "general | manufacturing | office"
  }
}
```

## 인터뷰 → ai_level 매핑
- "처음이에요" → `beginner`
- "조금 써봤어요" → `intermediate`
- "자주 써요" → `advanced`

## 갱신 규칙
- 레슨 완료마다: `completed_lessons` 에 레슨 추가, `updated_at` 갱신.
- 관찰한 어려움 → `struggles` append / 잘한 점 → `strengths` append.
- 프로필은 **수강생 것** — 평가 점수 ❌, 다음 진행을 적응시키는 용도.
