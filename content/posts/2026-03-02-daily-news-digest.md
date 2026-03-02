+++
title = "오늘의 뉴스 브리핑 (2026-03-02): AWS 데이터센터 미사일 피격, Qwen3.5 오픈소스, WebMCP 등장"
date = 2026-03-02

[extra]
categories = ["news", "AI", "infra", "geopolitics"]
+++

오늘 테크 뉴스의 핵심은 하나다. **전쟁이 클라우드를 건드렸다.** 그리고 AI 인프라의 지형도 조용히 바뀌고 있다.

---

## 🔴 AWS UAE 데이터센터, 이란 공습에 피격 — "AZ가 미사일에 불탔습니다"

Techmeme 오늘자 최상단이다. 중동 분쟁 중 이란의 반격으로 **UAE에 위치한 AWS 데이터센터가 피격**됐고, `me-central-1` 리전의 `mec1-az2` 가용 영역(Availability Zone)이 마비됐다.

AWS 공식 발표 원문: *"availability zone mec1-az2 was impacted by objects that struck the data center, creating sparks and fire"*

'미사일'이라는 단어 대신 **"데이터센터에 충돌한 물체(objects)"**라는 표현을 쓴 것이 화제가 됐다. 업계에서는 "군사적 완곡어법의 클라우드 버전"이라는 반응이 쏟아졌다.

쉽게 비유하면, 마치 교통사고 보험사가 "차량이 외부 물체와 비자발적 접촉을 경험했습니다"라고 표현하는 것과 같다.

**이 사건이 중요한 이유:**

데이터센터는 기본적으로 **평화 시대용 건물**이다. 항온항습 시스템과 전력 시스템이 정밀하게 맞물려 돌아가도록 설계됐지, 미사일 방어를 고려해 지은 구조물이 아니다. 업계 전문가 @hotaisle의 말이 핵심을 찌른다: *"냉각/전력 시스템 일부만 파괴해도 건물 전체가 셧다운된다. 이 거대한 건물들은 거대한 타겟이다."*

Vercel 창업자 Guillermo Rauch는 자사 두바이 리전이 해당 AZ에 있었지만, 1차 트래픽 수신 AZ가 무사해 서비스가 유지됐다고 밝혔다. 운 좋게 다른 가용 영역에 있었던 것. The Register는 이 사건을 **"전쟁으로 인한 최초의 가용 영역 장애"**로 기록했다.

앞으로의 질문은 클라우드 설계 자체를 바꿀 수 있다: 중앙화된 대형 데이터센터는 전쟁 지역에서 얼마나 안전한가?

**출처:** [Reuters](https://www.reuters.com/world/middle-east/amazons-cloud-unit-reports-fire-after-objects-hit-uae-data-center-2026-03-01/) · [Bloomberg](https://www.bloomberg.com/news/articles/2026-03-02/amazon-cloud-suffers-outage-after-objects-hit-uae-data-center) · [DatacenterDynamics](https://www.datacenterdynamics.com/en/news/aws-uae-outage-after-objects-struck-the-data-center-cause-fire-amid-iran-attacks/) · [The Register](https://www.theregister.com/2026/03/01/asia_tech_news_roundup/) via [Techmeme](https://techmeme.com)

---

## 🤖 알리바바 Qwen3.5-Medium — 내 컴퓨터에서 Claude Sonnet 4.5 수준을 공짜로

GeekNews 상위 항목이다. 알리바바가 **Qwen3.5 시리즈**를 오픈소스(Apache 2.0 라이선스)로 공개했다.

| 모델 | 파라미터 | 라이선스 |
|------|----------|----------|
| Qwen3.5-Large | 122B | Apache 2.0 |
| Qwen3.5-Medium | 35B | Apache 2.0 |
| Qwen3.5-Small | 27B | Apache 2.0 |

핵심은 **Medium(35B) 모델이 로컬에서 Claude Sonnet 4.5 수준의 성능**을 낸다는 점. Sonnet 4.5는 Anthropic의 유료 API $3/M 토큰 제품이다. 이걸 서버 없이 내 컴퓨터에서 돌릴 수 있게 됐다는 의미다.

비유하면, 스타벅스 시그니처 음료 레시피가 공개돼서 집에서 똑같이 만들 수 있게 된 것과 같다. 단, RTX 3090 이상급 GPU가 있어야 제대로 실행된다는 조건이 따라온다.

OpenAI GPT-5-mini와도 경쟁 가능한 수준이라고 VentureBeat는 평가했다. 중국발 오픈소스 모델이 글로벌 상용 AI의 성능 기준을 빠르게 따라잡고 있다.

**출처:** [VentureBeat](https://venturebeat.com/technology/alibabas-new-open-source-qwen3-5-medium-models-offer-sonnet-4-5-performance) via [GeekNews](https://news.hada.io/topic?id=27111)

---

## 🌐 WebMCP — 브라우저가 AI 에이전트의 손발이 된다

Hacker News에서 오늘 129개 댓글을 달성한 항목이다. Google Chrome이 **WebMCP(Model Context Protocol의 웹 브라우저 구현체)** 얼리 프리뷰를 공개했다.

**MCP(Model Context Protocol)**란 AI 에이전트가 외부 도구·서비스와 표준화된 방식으로 소통하는 프로토콜이다. Anthropic이 처음 제안해 업계가 빠르게 채택하고 있다. WebMCP는 이를 브라우저 네이티브로 지원하겠다는 것.

지금까지 AI 에이전트가 웹브라우저를 제어하려면 별도의 플러그인이나 Playwright 같은 자동화 도구를 사용해야 했다. WebMCP가 표준화되면 AI 에이전트가 **브라우저 내부와 직접 소통**하는 방식으로 바뀐다.

비유하면, 지금까지 AI가 브라우저를 "화면을 보면서 마우스를 움직이는" 방식으로 제어했다면, WebMCP 이후엔 "브라우저 내부 API에 직접 말 거는" 방식이 되는 것이다. 훨씬 빠르고 정확해진다.

**출처:** [Chrome Developers Blog](https://developer.chrome.com/blog/webmcp-epp) via [Hacker News](https://news.ycombinator.com/item?id=47211249)

---

## 🧠 보너스: Anthropic이 무료 AI 강의를 열었다

GeekNews 상위에 올라온 실용 소식. **Anthropic Courses**가 공개됐다. Claude 기본 API 활용부터 Claude Code 개발 워크플로, MCP 서버 구축, Agent Skills 구현까지 개발자 대상 무료 강의다.

Claude를 업무에 써보고 싶은데 어디서 시작해야 할지 모른다면 이게 공식 출발점이다.

**출처:** [GeekNews](https://news.hada.io/topic?id=27118)

---

오늘 주요 소스 직접 읽음: [Techmeme](https://techmeme.com) · [GeekNews](https://news.hada.io) · [Hacker News](https://news.ycombinator.com)
