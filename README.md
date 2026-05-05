# 2026-LLM
2026 하계 연수

## 학습 계획

| 1일차 | 교시 | 주제 | 2일차 | 교시 | 주제 |
| ---- |------|------|---- |------|------|
| 2026.07.28 화 | 1교시 | 수업 소개와 AI 개요 | 2026.07.29 수 | 1교시 | 스킬 개요와 활용 |
| 2026.07.28 화 | 2교시 | LLM과 ChatGPT 개요 | 2026.07.29 수 | 2교시 | 커넥터 개요와 활용 |
| 2026.07.28 화 | 3교시 | ChatGPT와 프롬프트 활용 | 2026.07.29 수 | 3교시 | 확장 프로그램과 코워크 개요 |
| 2026.07.28 화 | 4교시 | Claude 개요 |
| 2026.07.28 화 | 5교시 | Claude 프로젝트 활용 |


```mermaid
gantt
    title AI 강의 일정
    dateFormat YYYY-MM-DD
    axisFormat %m/%d

    section 1일(07.28화)
    1교시 - AI 개요                      :done, a1, 2026-07-28, 8h
    2교시 - LLM 개요                     :done, a2, after a1, 8h
    3교시 - ChatGPT 개요                 :done, a3, after a1, 8h
    4교시 - ChatGPT 활용                 :done, a4, after a2, 8h
    5교시 - Claude 개요                  :done, a5, after a2, 8h

    section 2일(07.29수)
    1교시 - 스킬 개요와 활용             :active, b1, 2026-07-29, 8h
    2교시 - 커넥터 개요와 활용           :active, b2, after b1, 8h
    3교시 - 코워크 개요와 활용           :active, b3, after b1, 8h
```
    
## mermaid 종류

### flowchar
```mermaid
flowchart TD
  A[입력] --> B{조건?}
  B -- Yes --> C[처리]
  B -- No  --> D[종료]
  C --> D
```

### sequenceDiagram
```mermaid
sequenceDiagram
  Client->>Server: POST /login
  Server->>DB: 사용자 조회
  DB-->>Server: 결과
  Server-->>Client: JWT 발급
```

### classDiagram
```mermaid
classDiagram
  Animal <|-- Dog
  Animal <|-- Cat
  class Animal {
    +String name
    +speak() void
  }
  class Dog {
    +fetch() void
  }
```
### erDiagram
```mermaid
erDiagram
  USER ||--o{ ORDER : places
  ORDER ||--|{ ITEM : contains
  USER {
    int id PK
    string email
  }
  ORDER {
    int id PK
    date created
  }
```

### stateDiagram
```mermaid
stateDiagram-v2
  [*] --> Idle
  Idle --> Running : start
  Running --> Paused : pause
  Paused --> Running : resume
  Running --> [*] : stop
```

### ganttChart
```mermaid
gantt
  title 개발 일정
  dateFormat YYYY-MM-DD
  section 설계
    요구분석 :a1,2024-01-01,7d
    설계     :a2,after a1,5d
  section 개발
    구현     :2024-01-13,10d
```

### pieChart
```mermaid
pie title 언어 점유율
  "JavaScript" : 40
  "Python"     : 30
  "TypeScript" : 20
  "기타"        : 10
```

### gitGraph
```mermaid
gitGraph
  commit id:"init"
  branch feature
  checkout feature
  commit id:"feat-A"
  commit id:"feat-B"
  checkout main
  merge feature
  commit id:"release"
```

## 스킬 활용 사례
- [팀 프로젝트 보드](https://claude.site/public/artifacts/610bed12-3584-4ec1-908c-b0dd5431cbe7/embed)
- 입베디스 코드
```HTML
<iframe src="https://claude.site/public/artifacts/610bed12-3584-4ec1-908c-b0dd5431cbe7/embed" title="kanban-board.html" width="100%" height="600" frameborder="0" allow="clipboard-write" allowfullscreen></iframe>
```

## 스킬 생성 프롬프트
- 주식 관련
  ```
  다음처럼 "주식 추천에 관한 스킬"을 요청하려고 해, 먼저 다음 '스킬 요청 문장'을 적절히 수정해 줘 
  목적: 최근 주식 시황을 분석해서 실적이 좋을 섹터를 선정해 수혜가 예상하는 관련 국내 ETF와 주식 종목을 각각 5개 정도 소개해 줘 
  ETF는 과거 실적이 좋으며 수수료가 낮은 것으로 추천해 줘 
  특히 단기(1-3 개월), 중기(6-12개월), 장기(1년이상)로 나누어서 각각 종목 5개씩 설명해줘<img width="2223" height="218" alt="image" 
  ```
  

