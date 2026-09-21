# Bama AI — Resource Inventory

> Phase 1.5 — Technical resource inventory
>
> Last verified: 2026-09-21
>
> Purpose: maintain a source-backed inventory of Bamanankan/Bambara resources that may be reused, studied, benchmarked, or explicitly excluded from Bama AI.

## Status legend
- 🟢 Confirmed: primary/official source checked and the stated property is supported.
- 🟡 Verify: resource exists, but one or more important properties still require a dedicated check.
- 🔴 Not suitable as-is: exists, but does not match the intended role or has a limitation that prevents direct use.
- ⭐ Strategic: particularly important for the long-term Bama AI objective.

## 1. Kunkado
| Field | Value |
|---|---|
| Status | 🟢 ⭐ |
| Type | Speech / ASR corpus |
| Language | Bambara majority; French code-switching; some other material |
| Size | 161.15 h |
| Segments | 118,925 |
| Reviewed subset | 39.3 h (~25%) |
| License | CC BY-SA 4.0 |
| Primary source | https://huggingface.co/datasets/RobotsMali/kunkado |
| Intended use | Robust ASR and code-switching research |
| Bama AI role | Candidate major ASR resource; study of real-world speech |
| Main limitations | Only a subset is human-reviewed; transcription quality is not uniformly ground truth; it is not a complete conversational dialogue corpus |

The dataset card states 161.15 h, 39.3 h reviewed, 118,925 segments and CC BY-SA 4.0. It explicitly targets fast, informal Bambara and French code-switching.

## 2. Jeli-ASR
| Field | Value |
|---|---|
| Status | 🟢 ⭐ |
| Type | Speech / ASR / translation dataset |
| Language | Bambara + French |
| Size | 32.48 h in the current version |
| Samples | 33,643 |
| Split | 32,180 train / 1,463 test |
| License | CC BY 4.0 |
| Primary source | https://huggingface.co/datasets/RobotsMali/jeli-asr |
| Bama AI role | ASR training/evaluation and speech analysis |
| Main limitations | Dataset is still described as in development; known inconsistent transcriptions, language/spelling issues and inaccurate translations remain |

Current dataset card/version 1.0.1 reports 32.48 h and 33,643 samples. Audio was recorded in Mali with griots; the dataset combines Bambara audio, Bambara transcriptions and French translations.

## 3. bam-asr-early
| Field | Value |
|---|---|
| Status | 🟡 |
| Type | ASR training corpus |
| Composition | Primarily Jeli-ASR + Mali-Pense + ~1 h children's speech collected by RobotsMali |
| Primary source | https://huggingface.co/datasets/RobotsMali/bam-asr-early |
| Bama AI role | Historical/experimental ASR resource |
| Main limitation | Dataset is explicitly not fixed and can change |

Decision: do not use an unpinned mutable version in a reproducible experiment. If used later, record an exact dataset revision.

## 4. Bambara ASR Benchmark
| Field | Value |
|---|---|
| Status | 🟢 ⭐ |
| Type | ASR benchmark |
| Benchmark data | 1 h of studio-recorded Malian constitutional text |
| Annotation | Transcribed/validated by linguists from Mali's DNENF-LN |
| Primary source | https://github.com/MALIBA-AI/bambara-asr-leaderboard |
| Bama AI role | Standard reference benchmark for ASR experiments |
| Main limitation | Formal studio speech; does not represent all real-world conditions such as noisy phone audio, spontaneous conversation or code-switching |

The benchmark is useful for comparable model evaluation, but it must not be treated as a complete measure of real-world Bamanankan speech understanding.

## 5. Bambara Text Normalizer
| Field | Value |
|---|---|
| Status | 🟢 ⭐ |
| Type | Text normalization + ASR evaluation framework |
| License | MIT |
| Primary source | https://github.com/MALIBA-AI/bambara-text-normalization |
| Bama AI role | Normalization layer and fair WER/CER evaluation |
| Key capability | Accounts for valid orthographic variation such as contracted/expanded forms |
| Importance | Prevents orthographic variation from being confused with recognition failure |

Decision: include this in the research inventory as infrastructure, not as training data.

## 6. MALIBA-AI Bambara TTS
| Field | Value |
|---|---|
| Status | 🟢 ⭐ |
| Type | Text-to-speech system |
| Primary source | https://github.com/MALIBA-AI/bambara-tts |
| Current system | Speaker-conditioned Bambara TTS |
| Speakers | 10 speaker identities documented by the project |
| Output | 16 kHz waveform |
| Server | HTTP API + OpenAI-compatible speech endpoint |
| Bama AI role | Candidate baseline for TTS |
| License | CC BY-NC-SA 4.0 according to the repository |
| Main limitation | Non-commercial restriction and model/data provenance constraints must be respected |

Important: the repository describes the TTS as open source, but its stated license is CC BY-NC-SA 4.0. Do not assume MIT/Apache or commercial reuse.

## 7. MALIBA-AI TTS inference server
| Field | Value |
|---|---|
| Status | 🟢 |
| Type | TTS serving infrastructure |
| Primary source | https://github.com/MALIBA-AI/bambara-tts/blob/main/server/README.md |
| Architecture | Qwen2.5-0.5B fine-tuned language model + BiCodec vocoder |
| Serving | llama.cpp + gateway |
| API | HTTP and OpenAI-compatible endpoint |
| Bama AI role | Possible local TTS experiment/integration baseline |
| Main limitation | Performance depends on GPU; license restrictions of the underlying model/data remain relevant |

This is infrastructure, not evidence that the resulting voice is already sufficiently natural for Bama AI.

## 8. MALIBA-AI Framework
| Field | Value |
|---|---|
| Status | 🟢 ⭐ |
| Type | Unified Malian-language AI SDK |
| Primary source | https://github.com/MALIBA-AI/maliba-framework |
| Capabilities documented | Speech recognition, TTS, machine translation, text generation, embeddings |
| Bama AI role | Existing ecosystem to benchmark/reuse and study |
| Main limitation | A unified SDK is not equivalent to a native Bamanankan conversational brain |

The current documentation lists Bambara models for multiple tasks. This makes it a useful integration/reference point for Bama AI experiments.

## 9. Bayelemabaga
| Field | Value |
|---|---|
| Status | 🟢 ⭐ |
| Type | Bambara–French parallel corpus |
| Size | ~47,000 sentence pairs |
| Source | Bambara Reference Corpus and related sources |
| Primary publication | NAACL 2025 |
| Bama AI role | Linguistic knowledge, vocabulary, structure, supervised experiments and evaluation |
| Main limitation | Primarily written bilingual data; it is not a spontaneous speech/conversation corpus |

Primary publication: https://aclanthology.org/2025.naacl-long.602/

The corpus should not be treated as the central training resource for a native conversational voice model.

## 10. Bambara Reference Corpus (CBR)
| Field | Value |
|---|---|
| Status | 🟡 ⭐ |
| Type | Linguistic reference corpus |
| Primary research source | Valentin Vydrin / LLACAN / INALCO |
| Historical availability | Corpus Bambara de Référence placed online in 2012 |
| Bama AI role | Linguistic analysis, vocabulary, grammar, orthography and corpus research |
| Main limitation | Access and reuse conditions must be checked for each current component before training use |

The published description confirms the CBR as a major Bambara corpus and describes tooling built around Manding-specific characteristics.

Do not assume that all CBR material is freely reusable for model training until current access/licensing terms are verified.

## 11. Belebele — bam_Latn
| Field | Value |
|---|---|
| Status | 🟢 |
| Type | Multilingual reading-comprehension benchmark |
| Bambara variant | bam_Latn |
| Size | 900 questions per language variant |
| Primary source | https://github.com/facebookresearch/belebele |
| Bama AI role | Written-language comprehension evaluation |
| Main limitation | Benchmark/test resource, not conversational training data |

Belebele explicitly describes itself as a test set and lists Bambara (bam_Latn) among its language variants. Its repository includes the applicable dataset license files.

## 12. Resource categories for Bama AI

### Speech / ASR
- Kunkado — priority
- Jeli-ASR — priority
- bam-asr-early — experimental/historical
- Bambara ASR Benchmark — evaluation

### TTS
- MALIBA-AI Bambara TTS — priority baseline
- MALIBA-AI TTS server — deployment/reference infrastructure

### Language / NLP
- Bayelemabaga — priority corpus
- CBR — strategic linguistic resource
- Belebele — evaluation

### Infrastructure
- Bambara Text Normalizer — priority
- MALIBA-AI Framework — ecosystem/reference

## 13. Current gap map

The inventory does NOT yet establish the existence of a single resource that provides all of:
1. spontaneous multi-turn Bamanankan conversations;
2. high-quality human transcripts;
3. speaker metadata and consent suitable for research;
4. natural code-switching annotation;
5. enough diversity of age, gender, accent and environment;
6. explicit conversational intent/context;
7. high-quality Bamanankan responses;
8. evaluation of native conversational understanding;
9. natural expressive TTS targets.

This gap is a research hypothesis to investigate further, not a claim that no such private or unpublished resource exists.

## 14. Immediate decisions

1. Do not download and mix everything blindly.
2. Pin exact versions/revisions before experiments.
3. Record license and provenance for every resource.
4. Separate training, validation, test and benchmark data.
5. Never use benchmark test data as training data.
6. Keep written bilingual corpora separate from speech corpora.
7. Treat orthographic normalization as a first-class component.
8. Evaluate ASR on both formal and real-world speech.
9. Keep the native-Bamanankan objective distinct from machine translation.
10. Before Phase 2, perform a dedicated license/provenance audit for every resource we intend to redistribute or train on.

## 15. Phase 2 preparation

The next technical step is not yet full model training.

First create a reproducible resource manifest containing:
- exact source URL;
- dataset/model identifier;
- revision/version;
- download/access status;
- license;
- provenance;
- size;
- language/script;
- intended task;
- known quality problems;
- permitted use;
- checksum where practical;
- Bama AI decision: reuse / benchmark / inspect / exclude.

Only after this manifest is validated should Phase 2 experiments begin.
