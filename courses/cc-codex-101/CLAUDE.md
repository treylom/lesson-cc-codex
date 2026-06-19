# cc-codex-101 코스 컨텍스트

> **이 파일은?** 코스 엔진이 읽는 짧은 운영 컨텍스트입니다. 풍부한 시나리오·업종 트랙·도구 치트시트는 `company-context/` 4문서가 정본이며, 이 파일은 그 요약 + 모듈 맵입니다.
> - 시나리오 전문: [`company-context/SCENARIO.md`](./company-context/SCENARIO.md)
> - 4 업종 트랙: [`company-context/BUSINESS-TRACKS.md`](./company-context/BUSINESS-TRACKS.md)
> - 도구 치트시트: [`company-context/TOOL-GUIDE-CC.md`](./company-context/TOOL-GUIDE-CC.md) · [`company-context/TOOL-GUIDE-CODEX.md`](./company-context/TOOL-GUIDE-CODEX.md)

## 학습 시나리오
당신은 **1인 사업자 '지우'**다. 온라인 강의를 만들어 팔고, 뉴스레터를 보내고, 가끔 컨설팅도 한다. 직원은 없다 — 기획·글쓰기·고객응대·매출정리·리서치를 **혼자 다 한다.** 늘 시간에 쫓긴다. 그래서 **Claude Code(CC)와 Codex 두 AI 도구를 내 사업의 운영 파트너로** 만들기로 한다. 이 코스의 목표는 둘 중 무엇이 더 좋은지 가리는 게 아니라, **두 도구로 실제 사업 한 사이클(자료 읽기 → 분석 → 보고서/콘텐츠 초안)을 직접 끝내보고, 언제 무엇을 쓰면 좋을지 감을 잡는 것**이다. (전체 서사 = `company-context/SCENARIO.md`)

## 현재 미션
1. 두 도구를 내 컴퓨터에 들인다 — 맨바닥 터미널에서 CC·Codex 설치·로그인·첫 실행.
2. `practice-data/<업종>/` 의 매출·고객·콘텐츠 자료를 AI에게 읽히고 패턴을 함께 찾는다.
3. 좋은 요청·Plan·**나만의 규칙서 `CLAUDE.md`**로 AI가 내 방식대로 일하게 만들고, 보고서/콘텐츠 초안을 뽑는다.
4. Codex에서 **모델·effort**를 바꿔 응답 차이를 보고, **CC 안 codex plugin**으로 둘을 같이 쓰며 "같은 것·다른 것"을 한 문장으로 말한다.

## 4 업종 트랙 (자가선택)
실습 데이터·예시는 4개 업종으로 준비됨. 자기 사업과 가까운 트랙을 골라 같은 실습을 자기 데이터로. 강의 영상·시연 = **creator(콘텐츠·지식)** 기본.
- ✍️ **creator** (기본·권장): 온라인 강의·뉴스레터·블로그·컨설팅 — `practice-data/creator/`
- 🛒 **store**: 스마트스토어·쿠팡 셀러 — `practice-data/store/`
- 💼 **freelancer**: 디자인·마케팅·개발 외주 — `practice-data/freelancer/`
- ☕ **local**: 카페·공방·학원 — `practice-data/local/`

## 성공 기준
- 터미널에서 CC·Codex를 설치·로그인해 첫 응답을 받아낸다.
- 자기 트랙 데이터(예: `creator/course_sales_monthly.csv`)에서 눈에 띄는 패턴 2개 이상을 AI와 함께 찾는다.
- 글 자료(예: `creator/student_inquiries.csv`)에서 반복되는 이슈를 정리한다.
- 나만의 `CLAUDE.md` 규칙서를 한 개 만들고, AI와 함께 보고서/콘텐츠 초안 1개를 완성한다.
- Codex에서 모델·effort를 바꿔 응답 차이를 보고, CC↔Codex 의 공통점·차이점을 스스로 1문장으로 요약한다.

## 학습자 프로필
- 비개발자 또는 개발 경험 거의 없는 1인 사업자.
- 터미널·명령어가 낯설고 살짝 무서울 수 있음. (→ 괜찮음. 망가지지 않음. 코스가 안전하게 안내.)
- 엑셀·메신저·문서 작성은 익숙함.
- 목표 = "코드를 잘 짜는 사람"이 아니라 "**AI와 함께 실무를 끝내는 사람**".

## 코스 진행 원칙
- 모든 설명은 비개발자 눈높이로. 전문 용어는 첫 등장 시 쉬운 비유와 함께.
- 한 번에 하나씩만 실행. 완벽함보다 "직접 해봤다"에 초점.
- AI는 비서이자 짝꿍이지 시험 감독이 아니다 — 실수해도 다시 시키면 된다.
- ⚠️ **실습은 이미 배운 범위만.** 아직 안 배운(미리 세팅된) 에이전트/기능으로 건너뛰지 않는다.

## 실습 데이터 설명
- 4 업종 트랙 폴더 각각에 매출·고객·콘텐츠 자료(CSV+노트) + `README.md`(데이터 의미·실습 팁) 수록.
- 예) `creator/course_sales_monthly.csv`(강의별 월매출), `creator/student_inquiries.csv`(수강생 문의), `creator/newsletter_stats.csv`(뉴스레터 성과), `creator/content_plan.md`·`research_memo.md`·`consulting_schedule.md`.
- 자기 업종 트랙의 `README.md`를 먼저 읽고 시작.

## 모듈 구성 (넘버링 커맨드 = `/cc-NN` · `/codex-NN`)
> 강의 클립은 번호 순서로 진행. 덱에 "지금 `/cc-03` 입력" 콜아웃. 부록도 같은 커맨드로 self-study. 전체 맵·커버 섹션 = `course-structure.json`.

**Claude Code 트랙 (cc101 21섹션 완전커버, 11모듈)**
- 강의: cc-01 설치·첫실행 / cc-02 에이전트 루프·첫와우 / cc-03 파일·명령어 / cc-04 워크플로우·Plan·프롬프트 / cc-05 CLAUDE.md 규칙서 / cc-06 세션·맥락오염·비용 / cc-08 플러그인·스킬·**codex plugin**
- 부록: cc-07 GitHub / cc-09 MCP / cc-10 서브에이전트·Hooks·자동화 / cc-11 워크스페이스·트러블슈팅·다음단계

**Codex 트랙 (codex101 21섹션 1:1, 11모듈 — 실제 0.140.0 실측 검증)**
- 강의: codex-01 설치·첫실행 / codex-02 CLI·슬래시($스킬) / codex-03 모델·effort·응답차이 / codex-05 승인·샌드박스 / codex-06 AGENTS.md·config.toml / codex-11 CC↔Codex 종합비교
- 부록: codex-04 여러 환경(App·IDE·Web) / codex-07 MCP / codex-08 비대화형·codex exec·CI/CD / codex-09 프롬프트·고급 / codex-10 트러블슈팅·FAQ·팁

## 코스의 마지막 장면
지우는 (1) 데이터를 AI에게 읽히고 질문하고, (2) Claude Code로 보고서/콘텐츠 초안을 만들고, (3) Codex를 설치·조절(effort·모델)해 같은 일을 해보고, (4) **CC 안에서 codex plugin으로 둘을 같이 쓰며** "두 도구는 뼈대가 같고 제품·모델·세부 기능만 다르다"를 스스로 설명할 수 있게 된다. 이 코스(=커리큘럼 1단계)의 목적은 "도구를 안다"가 아니라 **"두 AI 도구로 내 사업의 실무를 한 사이클 끝낸다"** 이다.

> **이건 시작이다 (전 커리큘럼 3단계 여정 — SCENARIO.md §2.5)**: 여기서 만든 규칙서·파일·감각이 → **2단계 '사업 두뇌' LLM Wiki**(Part 2~4: 옵시디언 토대·knowledge-manager 자동정리·`/search`·GraphRAG, 지금 `practice-data/`가 씨앗) → **3단계 AI 에이전트 팀**(Part 5~6: `soul.md` 봇 페르소나·Discord/Slack 봇팀) → 배포(Part 7) 로 그대로 자란다. 지우의 "혼자 다 한다"가 단계마다 "AI와 함께 한다"로 바뀐다.
