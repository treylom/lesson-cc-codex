# lesson-cc-codex

**Claude Code + Codex를 "직접 해보며" 배우는 대화형 실습 스킬** — 비개발자 1인 사업자·실무자를 위한 터미널 첫걸음부터 실전까지.

터미널이 처음이어도 괜찮습니다. 이 스킬을 켜면 Claude(또는 Codex)가 **실습 조교(TA)**가 되어, 한 단계씩 명령을 알려주고 여러분이 직접 입력해 보도록 옆에서 함께합니다. 대신 해주지 않고, 직접 해보게 안내해요.

---

> ## 🙏 원작 크레딧 (Credits & Inspiration)
>
> 이 코스는 아래 두 공개 입문 가이드의 **아이디어·구성·학습 흐름에서 영감**을 받아 출발했습니다. 길을 먼저 닦아주신 두 분께 깊이 감사드립니다 🙇
>
> | 원작 | 만든 분 | 링크 | 라이선스 |
> |------|---------|------|----------|
> | **CC101 — Claude Code 101** | **fivetaku** | [cc101.axwith.com](https://cc101.axwith.com) · `fivetaku/cc101` | [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) |
> | **Codex 101** | **swhan0329** | [swhan0329.github.io/codex-101](https://swhan0329.github.io/codex-101/) · `swhan0329/codex-101` | — |
>
> 두 가이드의 **문장·예시를 그대로 옮기지 않고**, 비개발자 1인 사업자 실무자용 시나리오로 **전부 새로 썼습니다**(변경됨). 자세한 라이선스·크레딧은 맨 아래 **'기반 / 크레딧'** 절을 참고하세요.

---

## 🚀 빠른 시작 (설치 & 첫 실행)

### 1) 사전 준비
- **Claude Code**가 설치돼 있어야 합니다. (없다면 → https://docs.claude.com/claude-code 설치 후 진행)
- 터미널을 열 수 있으면 충분합니다. 코딩 지식은 필요 없어요.

### 2) 스킬 설치 — 둘 중 편한 방법

**방법 A. 플러그인으로 설치 (권장)** — Claude Code 대화창 안에서:
```text
/plugin marketplace add https://github.com/treylom/tofukyung-plugins.git
/plugin install cc-codex-lessons
```
> 두 줄을 **한 줄씩** 입력하세요(한꺼번에 붙여넣으면 주소가 깨져요). `tofukyung-plugins` 마켓 안에 lesson-cc-codex·knowledge-manager 등 강의 도구가 함께 들어 있어요. 안 되면 `/plugin` 을 쳐서 도움말을 확인하세요.

**방법 B. 직접 클론** — 터미널에서:
```bash
git clone https://github.com/treylom/lesson-cc-codex.git ~/.claude/skills/lesson-cc-codex
```
클론 후 Claude Code를 다시 시작하면 `/lesson-cc-codex` 명령을 쓸 수 있습니다.

**Codex에서도 똑같이 돼요** — 저장소를 클론한 폴더에서 Codex를 실행하고 `$lesson-cc-codex codex-01` 로 호출합니다:
```bash
git clone https://github.com/treylom/lesson-cc-codex.git
cd lesson-cc-codex && codex      # 이 폴더에서 실행
```
> Claude Code = `/lesson-cc-codex`, Codex = `$lesson-cc-codex`. 내용은 같습니다. (자세한 설치·전역 설치 = [MANUAL.md](MANUAL.md))

### 3) 첫 실습 시작
Claude Code 안에서:
```text
/lesson-cc-codex cc-01
```
처음 실행하면 이름·업무·AI 경험을 가볍게 물어본 뒤(거부해도 됨), 바로 첫 실습을 시작합니다.
이어서 하려면 `/lesson-cc-codex 이어서` 를 입력하면 다음 레슨을 자동으로 제안해요.

> 💬 **막히거나 궁금하면 언제든** `/lesson-help <질문>` — 지금 레슨이든 다른 주제든, Claude Code·Codex 무엇이든 학습 도우미가 답합니다. (예: `/lesson-help cd 가 무슨 뜻이에요?`)

---

## 📚 무엇을 배우나요?

**시나리오**: 여러분은 1인 사업자 **'지우'**입니다. 온라인 강의를 만들어 팔고, 뉴스레터를 보내고, 가끔 컨설팅도 합니다. 기획·글쓰기·고객응대·매출정리·리서치를 혼자 다 하죠. 이 코스에서 **Claude Code와 Codex 두 AI 도구를 사업 운영 파트너로** 만들어, 자료 읽기 → 분석 → 보고서/콘텐츠 초안까지 한 사이클을 직접 끝내봅니다.

**4가지 업종 트랙** — 자기 사업과 가까운 걸 골라 같은 실습을 자기 데이터로:
- ✍️ **creator** (기본·권장): 온라인 강의·뉴스레터·블로그·컨설팅
- 🛒 **store**: 스마트스토어·쿠팡 셀러
- 💼 **freelancer**: 디자인·마케팅·개발 외주
- ☕ **local**: 카페·공방·학원

---

## 🗂️ 코스 구성 — 22개 레슨 (각 15~50분)

### Claude Code 트랙 (`/lesson-cc-codex cc-NN`)
| 번호 | 주제 |
|------|------|
| cc-01 | 설치와 첫 실행 (맨바닥 터미널) |
| cc-02 | 에이전트 루프 + 첫 와우 |
| cc-03 | 파일 다루기 + 명령어 |
| cc-04 | 워크플로우 + Plan + 좋은 프롬프트 |
| cc-05 | 나만의 규칙서 CLAUDE.md |
| cc-06 | 세션관리 + 맥락오염 + 비용 |
| cc-07 | GitHub로 저장·공유 (+ 공개 전 보안 점검) |
| cc-08 | 플러그인 + 스킬·슬래시 + codex plugin |
| cc-09 | MCP 외부도구 연결 |
| cc-10 | 서브에이전트 + Hooks + 자동화 |
| cc-11 | 워크스페이스 종합 + 트러블슈팅 + 다음 단계 |

### Codex 트랙 (`/lesson-cc-codex codex-NN`)
| 번호 | 주제 |
|------|------|
| codex-01 | Codex 설치와 첫 실행 |
| codex-02 | CLI 사용법 + 슬래시·단축키 ($스킬 호출) |
| codex-03 | 모델·effort·응답 차이 |
| codex-04 | 여러 환경 — App·IDE·Web/Mobile |
| codex-05 | 승인 + 샌드박스 3모드 |
| codex-06 | AGENTS.md + config.toml |
| codex-07 | MCP 외부도구 연결 |
| codex-08 | 비대화형 자동화 · codex exec · CI/CD |
| codex-09 | 프롬프트 전략 + 고급 활용 |
| codex-10 | 트러블슈팅 · FAQ · 팁 |
| codex-11 | CC ↔ Codex 같은 것·다른 것 (종합 비교) |

> 강의에서는 핵심 클립만 순서대로 진행하고, 나머지는 같은 명령으로 자습할 수 있습니다.

---

## 🎓 패스트캠퍼스 수강생용 — 강의 클립 순서

패스트캠퍼스 강의를 듣는 분은 **아래 강의 클립 순서**대로 따라오면 됩니다. (위 22개 전체 레슨은 복습·심화용 자습 버전이에요.) 강의 클립은 핵심만 압축한 진행표이며, 같은 명령으로 직접 실습할 수 있습니다.

**Claude Code 파트**
| 순서 | 명령 | 클립 |
|------|------|------|
| 1 | `/lesson-cc-codex fc-01` | 설치와 첫 실행 |
| 2 | `/lesson-cc-codex fc-02` | 에이전트 루프 + 첫 와우 |
| 3 | `/lesson-cc-codex fc-03` | 파일 다루기 + 명령어 |
| 4 | `/lesson-cc-codex fc-04` | 워크플로우 + Plan + 좋은 프롬프트 |
| 5 | `/lesson-cc-codex fc-05` | 나만의 규칙서 CLAUDE.md |
| 6 | `/lesson-cc-codex fc-06` | 세션관리 + 맥락오염 + 비용 |
| 7 | `/lesson-cc-codex fc-07` | 플러그인 + 스킬·슬래시 + codex plugin |

**Codex 파트**
| 순서 | 명령 | 클립 |
|------|------|------|
| 1 | `/lesson-cc-codex fc-08` | Codex 설치와 첫 실행 |
| 2 | `/lesson-cc-codex fc-09` | CLI 사용법 + 슬래시·단축키($스킬) |
| 3 | `/lesson-cc-codex fc-10` | 모델·effort·응답 차이 |
| 4 | `/lesson-cc-codex fc-11` | 승인 + 샌드박스 3모드 |
| 5 | `/lesson-cc-codex fc-12` | AGENTS.md + config.toml |
| 6 | `/lesson-cc-codex fc-13` | CC↔Codex 같은 것·다른 것 |

> Codex로 들으면 `/` 대신 `$`(예: `$lesson-cc-codex fc-01`). 막히면 언제든 `/lesson-help <질문>`. 전체 안내는 [MANUAL.md](MANUAL.md).

---

## ✅ 이 코스를 마치면

1. 터미널에서 Claude Code·Codex를 설치·로그인해 첫 응답을 받아낸다.
2. 내 데이터에서 눈에 띄는 패턴을 AI와 함께 찾는다.
3. 나만의 `CLAUDE.md`(규칙서)를 만들고, 보고서/콘텐츠 초안 1개를 완성한다.
4. Codex에서 모델·effort를 바꿔 차이를 보고, **CC ↔ Codex의 공통점·차이점을 한 문장으로** 설명한다.
5. 공개·납품 전 `/security-review`(CC)·`codex review`(Codex)로 **스스로 보안 점검**하는 습관을 익힌다.

---

## 🔒 안전 & 개인정보

- 이 저장소의 실습 데이터(`practice-data/`)는 **전부 가상의 인물·사업체**로 만든 예시입니다. 실제 개인정보가 없습니다.
- 실습 중 만드는 파일은 모두 여러분 컴퓨터 안에만 저장됩니다.
- AI는 비서이자 짝꿍이지 시험 감독이 아니에요 — 실수해도 다시 시키면 됩니다.

---

## 🧩 진행 방식 (요약)

- 모든 설명은 비개발자 눈높이. 전문 용어는 첫 등장 시 쉬운 비유와 함께.
- 한 번에 하나씩만 실행. "완벽함"보다 "직접 해봤다"에 초점.
- 명령어는 알려주되 입력은 여러분이 직접 (환경 설치·에러 진단·강사 시연은 예외).

---

## 📦 구성

```
lesson-cc-codex/
├─ SKILL.md                 # 스킬 엔진(진행 로직)
├─ commands/                # 슬래시 명령 정의
├─ courses/cc-codex-101/
│  ├─ CLAUDE.md             # 코스 컨텍스트
│  ├─ course-structure.json # 모듈 맵
│  ├─ lessons/              # 22개 레슨 (cc-01~11, codex-01~11)
│  ├─ company-context/      # 시나리오·업종 트랙·도구 가이드
│  └─ practice-data/        # 4개 업종 트랙 실습 데이터(가상)
└─ references/              # 교수법·엔진·메모리 스키마
```

---

## 🛠️ 기반 / 크레딧

- **lesson-a / lesson-skill** — "이론 설명 → 실습" 진행 패턴의 대화형 교육 엔진 계보.
- **CC101 by fivetaku (cc101.axwith.com)** — Claude Code 101 한국어 입문 가이드(`fivetaku/cc101`). 라이선스 [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/). 본 코스의 구성·학습 목표에서 **아이디어와 영감**을 받아 비개발자 실무자용으로 재구성했습니다(**변경됨**).
- **Codex 101 by swhan0329** — OpenAI Codex 입문 가이드(`swhan0329/codex-101` · https://swhan0329.github.io/codex-101/). (cc101 또한 codex-101에서 영감을 받아 만들어졌습니다.)
- 위 가이드들의 표현(문장·코드)을 통째로 복붙하지 않고, 학습 목표별로 다시 썼습니다.

## 📄 라이선스

MIT License — Copyright (c) 2026 treylom. 자유롭게 쓰고, 고치고, 나눠 주세요. (전문은 `LICENSE` 참조)

**문의 / 기여**: GitHub Issues · Discussions로 남겨주세요.
