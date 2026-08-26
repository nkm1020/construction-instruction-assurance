# Architecture

## 1. Context sources

- People, roles, crews, and language preferences
- Zones, work packages, schedules, and recent site state
- Drawings, BIM objects, specifications, and revision identifiers
- Materials, equipment, quantities, and safety constraints
- Previous, superseded, corrected, and cancelled instructions

All retrieved context must retain its source and timestamp. Transient site state must expire.

## 2. Canonical instruction

Each instruction should include:

- issuer and intended recipient
- action and object
- quantity or specification
- location or zone
- material and equipment
- start condition and deadline
- source evidence
- superseded instruction
- ambiguity and confidence state
- translation version
- worker read-back or acknowledgement
- completion and exception state

## 3. Decision policy

### Confirmed

Required fields resolve to current attributable sources. Translate and request read-back.

### Clarify

A required referent has multiple plausible candidates, source context is stale, or confidence is below a risk-based threshold. Ask one short targeted question.

### Escalate

The instruction changes safety material, critical sequencing, or an unresolvable conflict. Do not autonomously approve it.

## 4. Interaction flow

Push-to-talk audio -> construction ASR -> terminology normalization -> context retrieval -> reference resolution -> ambiguity policy -> structured instruction -> translation/TTS -> worker read-back -> audit event

## 5. Audit model

Use an append-only version chain. Never overwrite the original utterance. Record who confirmed which interpretation, what source was used, what changed, and whether the worker's response referred to the same instruction version.

## 6. Privacy and safety

- Minimize stored audio and personal data
- Define lawful basis, retention, access, and deletion rules before a pilot
- Separate model suggestions from confirmed site facts
- Require human approval for safety-critical decisions
- Test noisy-site and offline degradation explicitly
