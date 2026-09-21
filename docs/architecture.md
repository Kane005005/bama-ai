# Initial Architecture

## Goal
Build a native Bamanankan voice AI without assuming French must be the internal representation.

## Conceptual pipeline
Bamanankan speech → Speech-to-Text → Bamanankan language layer → reasoning/tools → Bamanankan response → Text-to-Speech → Bamanankan speech.

## STT — The ear
Input: Bamanankan audio. Output: Bamanankan text.

Concerns: transcription accuracy, local vocabulary, accents, noise, code-switching and latency.

## Language layer — The brain
Input: Bamanankan text and context. Output: response and/or tool actions.

We will evaluate multiple strategies. We do not assume today whether this requires fine-tuning an existing multilingual model, continued pretraining, adapters, a dedicated model or another approach.

## TTS — The voice
Input: Bamanankan text. Output: natural Bamanankan speech.

Concerns: intelligibility, pronunciation, rhythm, intonation, pauses, speaker diversity and latency.

## Evaluation layer
Each major component needs independent evaluation before end-to-end integration. Metrics will cover STT, language understanding, TTS naturalness, end-to-end task success, latency and resource use.

## Principle
The architecture is a hypothesis, not a permanent commitment. Experiments may replace components when evidence shows a better approach.