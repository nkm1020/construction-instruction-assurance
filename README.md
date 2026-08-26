# Construction Instruction Assurance

> A context-aware multilingual workflow for making informal construction instruction changes understandable, confirmable, and auditable across multilingual crews.

## 한국어 요약

외국인 근로자가 많은 건설현장에서 작업 중간에 바뀌는 지시를 단순 번역하는 것이 아니라 작업자, 위치, 공종, 도면/BIM, 자재, 장비, 이전 지시와 연결해 해석하고, 모호하면 재질문하며, 작업자의 이해 확인과 변경 이력을 남기는 B2B 에이전트 구상입니다.

## Problem

A phrase can be linguistically translated but operationally unsafe or wrong if the referent, location, quantity, revision, or superseded instruction is unclear. Attendance or a signature proves receipt, not comprehension. Generic translation and task-management products do not by themselves create an evidence chain for mid-shift instruction changes.

## Initial wedge

- One specialty trade, initially rebar or formwork
- One site and one multilingual crew
- Push-to-talk interaction
- A small number of language pairs
- Informal mid-shift changes rather than formal morning TBM translation

## Workflow

1. Capture the supervisor's spoken instruction
2. Resolve people, zone, work package, drawing/BIM object, material, equipment, and recent instruction context
3. Display confirmed facts separately from AI-restored candidates
4. Ask a short targeted clarification when ambiguity is material
5. Produce a canonical structured instruction and translation
6. Obtain worker read-back or explicit understanding confirmation
7. Preserve original, correction, cancellation, confirmation, and completion lineage

## Product boundary

This is an instruction-assurance layer, not a replacement construction-management platform, autonomous safety approver, or generic interpreter. Safety-critical changes always require human reconfirmation.

## Current status

Problem definition, evidence review, and pilot specification. No accident-reduction or labor-supply effect is claimed.

## Documents

- [ARCHITECTURE.md](ARCHITECTURE.md)
- [ROADMAP.md](ROADMAP.md)
- [EVALUATION.md](EVALUATION.md)
