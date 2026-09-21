# Bama AI Roadmap

This roadmap is intentionally staged. We do not jump directly to training a large model.

## Phase 0 — Foundation
**Status: current**

- [x] Create public repository
- [x] Define project vision and principles
- [x] Define initial architecture
- [x] Define dataset governance principles
- [x] Define contribution rules
- [ ] Complete resource audit
- [ ] Define first benchmark tasks

## Phase 1 — Bamanankan resource audit

Research existing Bamanankan text corpora, speech datasets, open models, linguistic resources, orthography, dialectal variation and licensing.

**Deliverable:** documented map of resources, gaps and legal/ethical constraints.

## Phase 2 — Language and data foundation

Build carefully curated datasets covering vocabulary, natural contexts, grammar, conversations, questions, idioms, proverbs, stories, politeness and relevant variants.

**Deliverable:** versioned datasets with provenance and quality controls.

## Phase 3 — First Bamanankan speech recognition

Build or adapt an STT baseline.

**Target:** Bamanankan audio → Bamanankan transcript.

Measure error rates and analyze failures by speaker, environment, vocabulary and linguistic phenomenon.

## Phase 4 — Native language brain

Investigate models capable of processing Bamanankan directly. Compare approaches experimentally rather than assuming one architecture.

## Phase 5 — Bamanankan speech synthesis

Build or adapt a TTS baseline.

**Target:** Bamanankan text → natural Bamanankan speech.

Evaluate pronunciation, intelligibility, rhythm, prosody and speaker diversity.

## Phase 6 — End-to-end voice AI

Combine:

**microphone → STT → language reasoning → TTS → audio**

Measure the complete system, not only individual components.

## Phase 7 — Evaluation, robustness and multimodality

Expand evaluation across accents, speakers, noise, code-switching, long dialogue, cultural context, latency, safety and optional tools/vision.

## Phase 8 — Ecosystem

When the foundations are mature: APIs, developer tools, applications, public benchmarks, community datasets, documentation, publications and partnerships.

## Rule

A phase can evolve or split. We advance when evidence and quality justify it, not simply because a calendar says so.
