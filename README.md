# lesson-cc-codex

Claude Code + Codex 대화형 학습 스킬 (interactive lesson engine)

## 개요

`/lesson-cc-codex`는 Claude Code와 Codex를 처음 배우는 **비개발자 실무자** 대상의 인터랙티브 학습 스킬입니다. 이론 설명 후 실습을 1:1로 진행하는 조교(TA) 역할을 하며, 수강생 프로필을 기반으로 학습을 적응형으로 진행합니다.

- **학습 형식**: 4가지 모듈 (Claude Code 2개 + Codex 2개)
- **대상**: 패스트캠퍼스 온라인 강의 수강생 및 개인 학습자
- **특징**: 수강생이 직접 명령을 입력하고 실행하도록 가이드 (대신 해주지 않음)

## 설치

### Claude Code 내장 스킬
```bash
/lesson-cc-codex 1-1   # Claude Code 첫 실습 시작
```

또는 프로필 기반으로 다음 레슨 자동 제안:
```bash
/lesson-cc-codex 이어서
```

### Git 저장소에서 직접 설치
```bash
git clone https://github.com/treylom/lesson-cc-codex.git
# 또는 Codex CLI 플러그인으로 설치
/plugin install github:treylom/lesson-cc-codex
```

## 코스 구조

**cc-codex-101** 코스 (4개 레슨, 각 15~20분)

| 모듈 | 레슨 ID | 제목 | 주제 |
|------|---------|------|------|
| 1 (Claude Code) | 1-1 | Claude Code 첫 실습 | 터미널에서 Claude 기본 명령 및 응답 방식 |
| | 1-2 | Claude Code 파일 다루기 | 파일 읽기, 쓰기, 수정하기 |
| 2 (Codex) | 2-1 | Codex 첫 실습 | Codex와 Claude Code의 차이 체험 |
| | 2-2 | Codex 심화 + 도구 비교 | 도구 선택 및 실무 활용 |

## 사용 방법

```bash
# 레슨 1-1 시작
/lesson-cc-codex 1-1

# 다음 완료 레슨부터 자동 시작
/lesson-cc-codex 이어서

# 특정 레슨으로 점프
/lesson-cc-codex 2-1
```

### 주요 기능

- **수강생 인터뷰**: 첫 실습 시 이름·회사·AI 경험 수준 수집 → `.lesson-memory/` 저장
- **진행 추적**: 완료한 레슨 기록 → 프로필 자동 업데이트
- **에러 처리**: 막히면 트러블슈팅 체크리스트 제공
- **숙련도 적응**: beginner/intermediate/advanced 레벨별 설명 깊이 조정

## 레슨 구성

각 레슨은 **3 Phase**로 진행:

1. **Phase 1 Opening** — 인사 → 학습 목표 설명 → 준비 상태 확인
2. **Phase 2 Progress** — 단계별 명령 제시 → 수강생이 직접 입력 → 결과 확인 → 트러블슈팅
3. **Phase 3 Closing** — 요약 → 저장/커밋 → 다음 레슨 예고 → 프로필 갱신

## 출처 / Attribution

이 스킬은 다음 오픈소스 및 공개 자료를 기반으로 합니다.

### 레슨 엔진
- **treylom/lesson-skill** — 대화형 교육 스킬 기본 아키텍처
- **treylom/lesson-a** — "이론 설명 → 실습" 진행 패턴 (성우하이텍 커스텀)

### Claude Code 레슨 콘텐츠
- **CC101-Guide** (fivetaku/cc101) — 21개 섹션 공식 가이드, 정본 경로 `AI_Second_Brain/020-Library/Research/Claude-Code-Guides/CC101-Guide/`
  - 권리: fivetaku (원저자) / 허가: CC BY-SA 3.0 하에 참고 및 재작곡
  - 재작곡 방식: 통째복붙 금지, 필요한 분·학습 목표별로 재구성

### Codex 레슨 콘텐츠
- **swhan0329/codex-101** — https://swhan0329.github.io/codex-101
  - Codex 실습 및 Claude Code와의 비교 패턴 참고

## 라이선스

MIT License — Copyright (c) 2026 treylom

자유로운 사용, 수정, 배포 가능합니다. (라이선스 전문은 LICENSE 파일 참조)

## 기여 및 피드백

- **문제 보고**: GitHub Issues
- **개선 제안**: GitHub Discussions 또는 Pull Requests

---

**마지막 업데이트**: 2026-06-19
**유지보수**: treylom (코난 봇 스킬 담당자)
