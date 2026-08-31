# 하네스 엔지니어링 (Harness Engineering)
---

## 이 강의가 답하는 질문

> **AI 코딩 도구가 삽질할 때, 무엇을 고쳐야 하는가?**

답은 "프롬프트를 더 길게 쓰기"가 아니다. 모델을 둘러싼 **하네스(Harness)** — Context · Permission · Verification · Tool · 작업 분리 · Debug · State — 를 시스템으로 설계하는 것이다.

그 위에서 **무엇을 만들지 판단하는 능력**(CodeCraft: 요구사항 → 설계 → 구현 → 검증)과, 작업이 커졌을 때 **여러 실행의 관계를 설계하는 능력**(Graph Engineering)까지가 이 책의 범위다.

> **Claude Code의 성능은 모델 하나로 결정되지 않는다. 모델이 어떤 Context를 보고 · 어떤 Permission으로 · 어떤 Tool을 사용하며 · 어떻게 검증받는지를 설계한 Harness가 크게 좌우한다.**

## 목차

| Part | 장 | 핵심 |
|---|---|---|
| **[1. 기초](01.%20Part%201%20—%20하네스%20엔지니어링의%20기초.md)** | 1. 하네스란 무엇인가 | 하네스 7축 / 증상별 진단표 / 자율성의 목표 |
| | 2. 아키텍처와 코어 루프 | 에이전틱 도구 / 코어 루프 / 4레이어 진단 / Human Decision Authority |
| **[2. Context](02.%20Part%202%20—%20Context%20Harness.md)** | 3. 많이가 아니라 정확하게 | 4분류 / Context Pack / Explore 우선 / Reduction Pipeline / 범위 줄이기 3단계 |
| | 4. 재설계와 세션 위생 | 재설계 4요소 / 요청 템플릿 / 세션 오염 / `/clear`·`/compact` / Append-only |
| | 5. CLAUDE.md | 4계층 / Auto Memory 200줄·25KB / Guidance vs Enforcement |
| **[3. Permission](03.%20Part%203%20—%20Permission%20Harness.md)** | 6. 실패 비용으로 설계하는 권한 | Safe/Ask/Deny / Deny First / Layered Control / Approval Fatigue |
| **[4. Verification·Debug](04.%20Part%204%20—%20Verification%20&%20Debugging%20Harness.md)** | 7. 검증 하네스 | 3단계 검증 / Diff / 반례 / Generation-Evaluation 분리 / Rollback |
| | 8. 디버깅 하네스 | Symptom·Evidence·Verification Path / 5단계 프롬프트 / 환경변수 매트릭스 |
| **[5. Tool](05.%20Part%205%20—%20Tool%20Harness.md)** | 9. 개입 지점과 확장 메커니즘 | Skills / MCP / Hooks / Permissions / Plugins |
| | 10. Skills vs Tool use | 절차 문제와 실행 문제의 구분 |
| **[6. 작업 분리](06.%20Part%206%20—%20작업%20분리와%20병렬%20운영.md)** | 11. Subagent | 컨텍스트 격리 / 역할·권한 분리 |
| | 12. Worktree | 파일 시스템 격리와 머지 |
| | 13. Plan-First·Thinking·Sub-Agent | 언제 무엇을 쓸지 |
| | 14. GitHub Issue-PR 자동화 | 어디까지 자동, 어디부터 사람 |
| **[7. CodeCraft](07.%20Part%207%20—%20CodeCraft.md)** | 15. Code Craft와 5단계 루틴 | Explore→Brainstorm→Plan→Implement→Verify |
| | 16. 기능 요구사항 분석 | Input→Logic→Output / 제약 / 변경 가능성 |
| | 17. 좋은 설계란 무엇인가 | 5원칙 / 골디락스 / 결합도·응집도 |
| | 18. OOD | 책임 → 클래스 / Entity·VO·DTO |
| | 19. SOLID | 수정 범위를 좁히는 기준 |
| | 20. 미니 케이스 | Delivery Fee Calculator에 하네스 적용 |
| **[8. 모델 세대](08.%20Part%208%20—%20모델%20세대별%20운영.md)** | 21. Opus 4.8 | Adaptive Thinking / Dynamic Workflow |
| | 22. Opus 5 | 지울 것 / 장황함 / Scope Creep |
| | 23. Fable 5 | 장기 자율 실행 / Effort Inversion |
| **[9. Graph](09.%20Part%209%20—%20Graph%20Engineering.md)** | 24. 왜 그래프인가 | 루프의 4가지 한계 |
| | 25. Node·Edge·State | Fake Edge / 다이아몬드 / Barrier·Streaming / Checker |
| | 26. 실전 패턴과 운영 | 패턴 7 / State 영속화 / Rulebook / 숨은 비용 |
