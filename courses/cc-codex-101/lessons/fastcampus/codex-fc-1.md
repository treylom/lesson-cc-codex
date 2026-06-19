# codex-fc-1 (강의 클립): Codex 설치와 첫 실행
> 대응 자습 레슨: `/lesson-cc-codex codex-01` · 강의 클립 1.2.4 · 예상 12~15분
> 이 문서 = 강의 촬영·진행용 런시트(이론 짧게 → 터미널 라이브). 깊은 자습은 위 레슨으로.

## 🎬 이 클립 한 줄 목표
Claude Code에서 익힌 설치·로그인·첫 실행 흐름을 Codex에 그대로 옮겨, 지우의 `~/practice-data/creator/` 폴더를 읽히는 데까지 끝낸다.

---

## 🗣️ 이론 (강사 설명 · 2~4분)

- **Codex = OpenAI가 만든 터미널 AI 비서.** Claude Code(Anthropic)와 일하는 방식은 같고 회사·계정·명령 기호 몇 개만 다르다. "같은 종류의 두 브랜드 냉장고" — 쓰는 법은 90% 같다.
- **왜 두 개를 쓰나?** 같은 질문을 두 AI에게 던져 비교하면 "이 일은 이 친구가 낫네"를 직접 느낄 수 있다. 혼자 일하지만 AI 파트너가 둘이 되는 셈.
- **딱 두 가지만 새로 기억하면 된다:** ① 로그인 계정이 ChatGPT 계정 ② `--sandbox read-only`(보기만 하는 안전 모드)라는 개념. 나머지는 Claude Code와 같다.
- **비유 — 샌드박스:** 아이가 정해진 울타리 안에서만 노는 모래놀이판처럼, Codex가 내 폴더를 함부로 건드리지 않도록 범위를 정하는 안전장치다.
- **CC와 Codex 명령 대조표 (화면에 보여주기):**

  | 동작 | Claude Code | Codex |
  |------|-------------|-------|
  | 설치 | `npm install -g @anthropic-ai/claude-code` | `npm install -g @openai/codex` |
  | 로그인 | `claude login` (Anthropic 계정) | `codex login` (ChatGPT 계정) |
  | 첫 실행 | `claude "..."` | `codex "..."` |
  | 버전 확인 | `claude --version` | `codex --version` |

---

## ⌨️ 터미널 라이브 시연 (8~10분)

### STEP 1 — 토대 확인

- **시연:** `node --version`
- **보여줄 것:** `v20.11.0` 처럼 `v` + 숫자가 뜨면 토대 준비 완료. `command not found`가 뜨면 nodejs.org에서 LTS 설치 필요.
- **학습자에게:** "직접 `node --version`을 쳐서 숫자가 뜨는지 확인해 보세요."

---

### STEP 2 — Codex 설치

- **시연:** `npm install -g @openai/codex`
- **보여줄 것:** 설치 진행 메시지가 흐르다가 `added 1 package in 6s` 같은 완료 줄이 뜬다. Claude Code를 깔 때 썼던 `@anthropic-ai/claude-code`와 회사 이름 부분만 다르다는 점을 강조.
- **학습자에게:** "직접 한 줄 입력해 보세요. 완료 메시지가 뜰 때까지 기다리면 됩니다."

---

### STEP 3 — 설치 확인 + 로그인

- **시연:**
  ```
  codex --version
  codex login
  ```
- **보여줄 것:**
  - `codex --version` → 버전 숫자(`codex-cli 0.xx.x`)가 뜨면 성공. 안 뜨면 터미널 창을 껐다 다시 열면 대부분 해결.
  - `codex login` → 브라우저가 자동으로 열리고, 평소 ChatGPT 계정으로 로그인 → 승인 버튼 → 터미널에 완료 안내.
- **학습자에게:** "직접 `codex login`을 쳐서 브라우저에서 ChatGPT 계정으로 승인해 보세요."

---

### STEP 4 — 안전하게 폴더 첫 열기 (read-only)

- **시연:**
  ```
  codex --cd ~/practice-data/creator --sandbox read-only "이 폴더에 어떤 파일이 있는지 둘러보고, 각 파일이 뭔지 한 줄씩 설명해 줘. 나는 비개발자야."
  ```
- **보여줄 것:** Codex가 폴더를 스스로 열어 파일 목록(`course_sales_monthly.csv`, `student_inquiries.csv` 등)을 읽고 각 파일의 용도를 설명해 준다. 복사·붙여넣기 없이 AI가 직접 폴더를 여는 장면 — 이것이 "터미널 AI의 와우 모먼트". `--sandbox read-only`라서 단 한 글자도 고치지 않았다는 점도 강조.
- **학습자에게:** "직접 `~/practice-data/creator` 대신 자기 트랙 폴더를 넣어서 쳐보세요."

---

### STEP 5 — 실제 데이터로 첫 분석

- **시연:**
  ```
  codex --cd ~/practice-data/creator --sandbox read-only "너는 내 온라인 강의 사업의 데이터 분석가야. @course_sales_monthly.csv 를 읽고, 매출이 가장 큰 강의 TOP 3를 CSV의 실제 숫자를 인용해서 표로 정리해 줘. 비개발자도 이해되게."
  ```
- **보여줄 것:** Codex가 CSV의 실제 숫자(예: 187명·1,477만원)를 근거로 든 TOP 3 표를 내준다. 숫자가 붙어야 믿을 수 있는 답이라는 점, "CSV의 실제 값으로 근거를 보여줘"라고 추가 요청하면 더 정확해진다는 점을 설명.
- **학습자에게:** "직접 같은 명령을 쳐보고, Codex가 내 파일의 실제 숫자를 근거로 답하는지 확인해 보세요."

---

## ✅ 마무리 (1분)

오늘 한 것: 토대 확인 → Codex 설치 → 버전 확인 → ChatGPT 계정 로그인 → `--sandbox read-only`로 폴더 안전하게 열기 → 실제 데이터로 첫 분석. Claude Code와 90% 같은 흐름이었다.

더 깊이 파고들고 싶으면 → `/lesson-cc-codex codex-01`에서 파일 만들기·두 도구 비교·트러블슈팅 전체를 볼 수 있다.

다음 클립(1.2.5)에서는 **Codex와 대화하는 도중에 쓰는 명령들** — Codex만의 호출 기호 `$`(스킬 부르기)와 세션 안 슬래시 명령(`/plan`, `/status` 등)을 배운다.

---

## 📌 강사 노트

**자주 막히는 지점 1 — `command not found: codex`**
설치 직후 가장 흔한 일시 현상. 터미널 창을 완전히 닫았다 다시 열면 대부분 해결. "망가진 게 아니라 터미널이 방금 깐 프로그램을 아직 못 찾는 것"이라고 안심시킨다.

**자주 막히는 지점 2 — 로그인 브라우저가 자동으로 안 열림**
터미널에 표시된 주소(URL)를 직접 복사해 브라우저에 붙여넣으면 된다. 로그인이 자꾸 풀린다면 `Ctrl+C`로 껐다가 `codex login` 다시 → 브라우저에서 "승인"까지 클릭하는지 확인.
