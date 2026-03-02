+++
title = "오늘의 뉴스 브리핑 (2026-03-02): AWS 데이터센터 피격, Anthropic vs 펜타곤, Qwen3.5 공개"
date = 2026-03-02

[extra]
categories = ["news", "AI", "geopolitics"]
+++

# 오늘의 뉴스 브리핑 — 2026년 3월 2일

---

## 🔴 AWS UAE 데이터센터 미사일 피격 — 클라우드 인프라의 새로운 위협

오늘자 Techmeme 최상단을 장식한 뉴스다. 이란의 반격 공격 중 UAE에 위치한 AWS 데이터센터가 피격됐다. AWS 공식 발표는 **"가용 영역 mec1-az2가 데이터센터에 충돌한 물체로 인해 화재가 발생해 영향을 받았다"** — '미사일'이라는 단어를 끝까지 피한 역대급 기업 공식 표현이다.

Vercel의 Guillermo Rauch는 자사 두바이 리전의 1차 AZ(가용 영역)가 피해를 입지 않아 서비스가 유지됐다고 발표했다. The Register는 이를 **"전쟁으로 인한 최초의 가용 영역 장애"**로 기록했다.

업계가 주목하는 본질적인 질문은 이미 나왔다:

- *"데이터센터는 전쟁을 위해 설계되지 않았다. 냉각 시스템만 무력화해도 건물 전체가 셧다운된다"* — 업계 트위터 반응
- *"소버린 AI 인프라가 필요하다"* — 중앙화된 클라우드 의존도에 대한 경고

> 💡 이 사건은 단순한 AWS 장애가 아니다. **AI 시대에 클라우드 인프라가 군사 표적이 될 수 있다**는 최초의 실증 사례다.

**Sources:** [Reuters](https://www.reuters.com/world/middle-east/amazons-cloud-unit-reports-fire-after-objects-hit-uae-data-center-2026-03-01/) · [The Register](https://www.theregister.com/2026/03/01/asia_tech_news_roundup/) · [Techmeme](https://techmeme.com)

---

## 🤖 Anthropic vs 펜타곤 — AI 군사 이용의 레드라인 충돌

이번 주 두 번째 빅 스토리다. The Atlantic이 내막을 상세 보도했다: **펜타곤이 Anthropic에 미국 시민의 지리정보·웹브라우징 데이터 같은 상업 대량 데이터(bulk data) 분석을 허용해달라고 요구했고, Anthropic이 이를 거부하면서 협상이 결렬됐다.**

- Anthropic은 협상 결렬 직후 펜타곤을 상대로 소송 제기를 예고했다.
- OpenAI는 그 날 밤 펜타곤과 프레임워크 계약을 체결했다.
- 아이러니: WSJ 보도에 따르면 **트럼프 행정부가 Anthropic 사용을 금지한 지 몇 시간 뒤** 미군은 이란 공습에 Claude를 실제로 사용했다.
- 이 사건 이후 Claude가 앱스토어 1위로 올라섰다 (Semafor).

Anthropic CEO 다리오 아모데이: *"우리는 미국에 헌신하는 애국적 미국인이지만 레드라인은 지킨다."*

Anthropic이 지킨 레드라인은 **자율무기·시민 대량 감시**였다. OpenAI는 그 선을 넘었다.

**Sources:** [The Atlantic](https://www.theatlantic.com/technology/2026/03/inside-anthropics-killer-robot-dispute-with-the-pentagon/686200/) · [WSJ](https://www.wsj.com/livecoverage/iran-strikes-2026/card/u-s-strikes-in-middle-east-use-anthropic-hours-after-trump-ban-ozNO0iClZpfpL7K7ElJ2) · [Semafor](https://www.semafor.com/article/03/01/2026/claude-attracts-users-on-pentagon-spat) · [Techmeme](https://techmeme.com)

---

## 🧠 Anthropic Courses — 무료 AI 강의 공개 (GeekNews)

Anthropic이 개발자 대상 무료 온라인 강의를 공개했다. Claude 기본 API 활용부터 Claude Code, MCP 서버 구축, Agent Skills까지 커버한다.

**Sources:** [GeekNews](https://news.hada.io/topic?id=27118)

---

## ⚡ 알리바바 Qwen3.5-Medium — 로컬에서 Sonnet 4.5 수준 (GeekNews)

알리바바가 Qwen3.5 시리즈를 오픈소스(Apache 2.0)로 공개했다. 35B, 122B, 27B 모델로 구성되며, 로컬 실행 상태에서 Claude Sonnet 4.5 수준의 성능을 낸다고 벤처비트가 보도했다. GPT-5-mini와도 경쟁 가능한 수준.

**Sources:** [GeekNews](https://news.hada.io/topic?id=27111) · [VentureBeat](https://venturebeat.com/technology/alibabas-new-open-source-qwen3-5-medium-models-offer-sonnet-4-5-performance)

---

## 🔧 WebMCP — 브라우저가 MCP를 직접 지원한다 (Hacker News)

Google Chrome이 WebMCP 얼리 프리뷰를 공개했다. **MCP(Model Context Protocol)**를 브라우저 네이티브로 지원하는 기술로, HN에서 129개의 댓글이 달리며 주목받고 있다. AI 에이전트가 웹브라우저와 더 긴밀하게 통합되는 방향의 중요한 스텝이다.

**Sources:** [Hacker News](https://news.ycombinator.com/item?id=47211249) · [Chrome Dev Blog](https://developer.chrome.com/blog/webmcp-epp)

---

## 💻 에이전틱 엔지니어링 시대의 생존 스킬 9가지 (GeekNews)

Karpathy가 주말 프로젝트를 AI 에이전트에게 완전히 위임한 경험을 바탕으로 정리한 글이 GeekNews에서 화제다. IP, 사용자명, 비밀번호, 목표만 주고 30분 뒤 결과를 확인하는 방식으로 에이전트의 가능성과 한계를 동시에 보여줬다.

**Sources:** [GeekNews](https://news.hada.io/topic?id=27104)

---

**오늘 주요 소스:** [Techmeme](https://techmeme.com) · [GeekNews](https://news.hada.io) · [Hacker News](https://news.ycombinator.com)
