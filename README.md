# 2026-LLM
2026 하계 연수

## 학습 계획
```mermaid
gantt
    title AI 강의 일정
    dateFormat YYYY-MM-DD
    axisFormat %m/%d

    section 1일차 (07.28 화)
    1교시: AI 개요                      :done, a1, 2026-07-28, 1d
    2교시: LLM 개요                     :done, a2, 2026-07-28, 1d
    3교시: ChatGPT 개요                 :done, a3, 2026-07-28, 1d
    4교시: ChatGPT 활용                 :done, a4, 2026-07-28, 1d
    5교시: Claude 개요 및 프로젝트 활용 :done, a5, 2026-07-28, 1d

    section 2일차 (07.29 수)
    1교시: 스킬 개요와 활용             :active, b1, 2026-07-29, 2d
    2교시: 커넥터 개요와 활용           :active, b2, 2026-07-29, 2d
    3교시: 코워크 개요와 활용           :active, b3, 2026-07-29, 2d
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
