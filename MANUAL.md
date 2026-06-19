# lesson-cc-codex — 코스 매뉴얼 & 전체 목차

> **Claude Code + Codex를 "직접 해보며" 배우는 대화형 실습 스킬.** 비개발자 1인 사업자·실무자용. 이 문서는 코스의 전체 지도입니다(설치 → 목차 → 트랙 → 보안·고급기능 → 도움받기). 빠른 시작만 원하면 [README.md](README.md)를 보세요.

---

## 1. 이 코스는 무엇인가

터미널이 처음이어도 괜찮습니다. 이 스킬을 켜면 Claude(또는 Codex)가 **실습 조교(TA)**가 되어, 명령을 한 단계씩 알려주고 여러분이 직접 입력해 보도록 옆에서 함께합니다. 대신 해주지 않고 **직접 해보게** 안내합니다.

**시나리오** — 여러분은 1인 사업자 **'지우'**입니다. 온라인 강의를 만들어 팔고, 뉴스레터를 보내고, 가끔 컨설팅도 합니다. 기획·글쓰기·고객응대·매출정리를 혼자 다 하죠. 이 코스에서 **Claude Code와 Codex 두 AI 도구를 사업 운영 파트너로** 만들어, 자료 읽기 → 분석 → 보고서/콘텐츠 초안까지 한 사이클을 직접 끝내봅니다.

**이 코스의 목표**는 두 도구 중 무엇이 더 좋은지 가리는 게 아니라, **두 도구로 실제 업무 한 사이클을 끝내보고 "언제 무엇을 쓰면 좋을지" 감을 잡는 것**입니다.

---

## 2. 설치 — 두 플랫폼 모두 지원

이 스킬은 **Claude Code와 Codex 양쪽에서** 똑같이 돌아갑니다.

### Claude Code
**방법 A. 플러그인 (권장)** — Claude Code 대화창에서:
```text
/plugin marketplace add treylom/lesson-cc-codex
/plugin install lesson-cc-codex
```
**방법 B. 직접 클론** — 터미널에서:
```bash
git clone https://github.com/treylom/lesson-cc-codex.git ~/.claude/skills/lesson-cc-codex
```
설치 후 `/lesson-cc-codex cc-01` 로 시작.

### Codex
1. 저장소를 클론합니다:
   ```bash
   git clone https://github.com/treylom/lesson-cc-codex.git
   ```
2. **클론한 폴더에서** Codex를 실행: `codex` (또는 `codex --cd lesson-cc-codex`).
3. 스킬 호출: `$lesson-cc-codex codex-01` (또는 `/skills` 로 목록 확인).
   - 전역 설치를 원하면 `.agents/skills/lesson-cc-codex/` 를 `~/.agents/skills/lesson-cc-codex/` 로 복사.

> **표기 차이 한 줄**: Claude Code = `/lesson-cc-codex`, Codex = `$lesson-cc-codex`. 내용은 같습니다.

---

## 3. 빠른 시작 + 언제든 질문하기

- **시작**: `/lesson-cc-codex cc-01` (CC) 또는 `$lesson-cc-codex cc-01` (Codex). 처음엔 이름·업무·AI 경험을 가볍게 물어본 뒤(거부해도 됨) 바로 첫 실습.
- **이어서**: `/lesson-cc-codex 이어서` → 프로필 기준 다음 레슨 자동 제안.
- **언제든 질문 — `/lesson-help`**: 막히거나 궁금할 때 `/lesson-help <질문>` 으로 자유롭게 물어보세요. 지금 레슨이든, 다른 주제든, Claude Code·Codex 무엇이든 학습 도우미가 답합니다. 예:
  ```text
  /lesson-help cd 가 무슨 뜻이에요?
  /lesson-help codex에서 모델 바꾸는 법 알려줘
  /lesson-help 내 매출 CSV를 분석하려면 어느 레슨부터 보면 돼?
  ```

---

## 4. 전체 목차 — 22개 레슨 (자습 풀버전)

각 레슨 15~50분. 강의(`lecture`)는 클립 순서로, 부록(`appendix`)은 같은 명령으로 자습.

### Claude Code 트랙 — `/cc-NN` · `$lesson-cc-codex cc-NN`
| 번호 | 제목 | 구분 |
|------|------|------|
| cc-01 | 설치와 첫 실행 (맨바닥 터미널) | 강의 |
| cc-02 | 에이전트 루프 + 첫 와우 | 강의 |
| cc-03 | 파일 다루기 + 명령어 | 강의 |
| cc-04 | 워크플로우 + Plan + 좋은 프롬프트 | 강의 |
| cc-05 | 나만의 규칙서 CLAUDE.md | 강의 |
| cc-06 | 세션관리 + 맥락오염 + 비용 | 강의 |
| cc-07 | GitHub로 저장·공유 (+ 공개 전 🔒보안 점검) | 부록 |
| cc-08 | 플러그인 + 스킬·슬래시 + codex plugin | 강의 |
| cc-09 | MCP 외부도구 연결 | 부록 |
| cc-10 | 서브에이전트 + Hooks + 자동화 (+ 🚀고급 자율기능) | 부록 |
| cc-11 | 워크스페이스 종합 + 트러블슈팅 + 다음 단계 | 부록 |

### Codex 트랙 — `/codex-NN` · `$lesson-cc-codex codex-NN`
| 번호 | 제목 | 구분 |
|------|------|------|
| codex-01 | Codex 설치와 첫 실행 | 강의 |
| codex-02 | CLI 사용법 + 슬래시·단축키($스킬 호출) | 강의 |
| codex-03 | 모델·effort·응답 차이 (시연) | 강의 |
| codex-04 | 여러 환경 — App·IDE·Web·Mobile | 부록 |
| codex-05 | 승인 + 샌드박스 3모드 (yolo 모드 포함) | 강의 |
| codex-06 | AGENTS.md + config.toml | 강의 |
| codex-07 | MCP 외부도구 연결 | 부록 |
| codex-08 | 비대화형 자동화 · codex exec · CI/CD | 부록 |
| codex-09 | 프롬프트 전략 + 고급 활용 (서브에이전트·이미지·/goal) | 부록 |
| codex-10 | 트러블슈팅 · FAQ · 팁 · 참고 | 부록 |
| codex-11 | CC ↔ Codex 같은 것·다른 것 (종합 비교) | 강의 |

---

## 5. 패스트캠퍼스 강의 클립용 — 13개 런시트 (lecture-trim)

강의 영상 클립에 맞춰 핵심만 압축한 진행표입니다(이론→터미널 시연 흐름). 자습 22레슨의 강의용 버전이며, `lessons/fastcampus/` 에 있습니다.

| 번호 | 제목 |
|------|------|
| cc-fc-1 | 설치와 첫 실행 (맨바닥 터미널) |
| cc-fc-2 | 에이전트 루프 + 첫 와우 |
| cc-fc-3 | 파일 다루기 + 명령어 |
| cc-fc-4 | 워크플로우 + Plan + 좋은 프롬프트 |
| cc-fc-5 | 나만의 규칙서 CLAUDE.md |
| cc-fc-6 | 세션관리 + 맥락오염 + 비용 |
| cc-fc-7 | 플러그인 + 스킬·슬래시 + codex plugin |
| codex-fc-1 | Codex 설치와 첫 실행 |
| codex-fc-2 | CLI 사용법 + 슬래시·단축키($스킬) |
| codex-fc-3 | 모델·effort·응답 차이 |
| codex-fc-4 | 승인 + 샌드박스 3모드 |
| codex-fc-5 | AGENTS.md + config.toml — 규칙서 |
| codex-fc-6 | CC↔Codex 같은 것·다른 것 |

---

## 6. 4가지 업종 트랙

같은 실습을 자기 사업과 가까운 데이터로. 강의 시연 기본 = **creator**.
- ✍️ **creator** (기본·권장): 온라인 강의·뉴스레터·블로그·컨설팅
- 🛒 **store**: 스마트스토어·쿠팡 셀러
- 💼 **freelancer**: 디자인·마케팅·개발 외주
- ☕ **local**: 카페·공방·학원

실습 데이터는 모두 **가상의 인물·사업체**입니다(`practice-data/`). 실제 개인정보 없음.

---

## 7. 🔒 보안 점검 — 공개·공유 전에 (cc-07)

비개발자가 가장 실수하기 쉬운 것: 비밀번호·API 키·고객정보가 든 파일을 GitHub에 올리는 것. 두 도구 모두 **올리기 전 자동 점검 기능**이 있습니다.
- **Claude Code**: `/security-review` — 변경사항을 보안 관점으로 훑어 위험을 짚어줌.
- **Codex**: `codex review --uncommitted` — 아직 저장 안 한 변경을 점검, 하드코딩된 키를 `[P1]`로 검출. (전용 플러그인 `codex-security` 도 있음.)
- **습관**: 무엇을 공유·공개하든 그 직전에 한 번. (실습 = cc-07)

---

## 8. 🚀 고급 자율 기능 (선택 — "이런 게 있구나")

목표만 주면 더 알아서 해주는 기능들. **자율로 움직이니 멈추는 법(`Esc`)부터** 익히고, 작은 일로 연습하세요.

### Claude Code (cc-10 보너스)
- **`/goal <조건>`** — 목표(끝나는 조건)를 주면 그때까지 스스로 진행. `/goal` 조회, `/goal clear` 취소.
- **`/effort ultracode`** — effort(공들이는 정도)를 최고로. 깊이 생각 + 필요시 보조 일꾼 자동 동원. 느리고 비싸니 중요한 일에만.
- **`/workflows`** — 여러 보조 일꾼이 동시에 돌 때 진행 상황판(대시보드).

### Codex (codex-09)
- **서브에이전트** — 자연어로 "여러 관점으로 하나씩 띄워서 표로 정리해줘".
- **이미지 생성** — `$imagegen` 또는 자연어(썸네일·삽화). 기본 그림 생성은 별도 키 불요.
- **`/goal <조건>`** — 목표 모드(`pause`/`resume`/`clear`).
- **yolo 모드** — 승인을 건너뛰는 빠른 모드(codex-05). 격리된 안전한 환경에서만 권장.

---

## 9. 두 플랫폼 표기 비교 (한눈에)

| | Claude Code | Codex |
|--|-------------|-------|
| 스킬 호출 | `/lesson-cc-codex` | `$lesson-cc-codex` |
| 규칙서 | `CLAUDE.md` | `AGENTS.md` |
| 비대화형 실행 | `claude -p "..."` | `codex exec "..."` |
| 보안 점검 | `/security-review` | `codex review --uncommitted` |
| 목표 모드 | `/goal` | `/goal` |
> CC를 익히면 Codex는 약 90%가 그대로 전이됩니다(codex-11에서 직접 확인).

---

## 10. 폴더 구조

```
lesson-cc-codex/
├─ SKILL.md                 # Claude Code 스킬 엔진
├─ AGENTS.md                # Codex 안내(사람용)
├─ MANUAL.md                # 이 문서
├─ README.md                # 빠른 시작
├─ .agents/skills/lesson-cc-codex/SKILL.md   # Codex 스킬 엔진
├─ commands/                # 슬래시 명령(/lesson-cc-codex, /lesson-help)
├─ courses/cc-codex-101/
│  ├─ CLAUDE.md             # 코스 컨텍스트
│  ├─ course-structure.json # 모듈 맵
│  ├─ lessons/              # 22개 레슨 + fastcampus/ 강의용 13
│  ├─ company-context/      # 시나리오·업종 트랙·도구 가이드
│  └─ practice-data/        # 4개 업종 실습 데이터(가상)
└─ references/              # 교수법·엔진·메모리 스키마
```

---

## 11. 크레딧 · 라이선스

- **lesson-a / lesson-skill** — "이론 설명 → 실습" 대화형 교육 엔진 계보.
- 코스 콘텐츠 = 공개 가이드(Claude Code 101 = fivetaku/cc101 · Codex 101 = swhan0329/codex-101)를 비개발자 실무자용으로 **재구성**(통째 복붙 아님).
- Codex 명령·동작은 실제 Codex(0.140.0) 실측 검증 기준.
- **MIT License** — Copyright (c) 2026 treylom. 자유롭게 쓰고 고치고 나눠 주세요.
