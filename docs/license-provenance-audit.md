# Bama AI — License & Provenance Audit

> Phase 1.5 — licensing and provenance checkpoint
> Verification date: 2026-09-21

This is a technical provenance audit, not legal advice.

## 1. Kunkado

Status: 🟢 research reuse appears permitted under the published dataset licence.
- Source: https://huggingface.co/datasets/RobotsMali/kunkado
- Licence: CC BY-SA 4.0.
- The dataset card explicitly says users may share and adapt, including commercially, with attribution and ShareAlike obligations.
- Provenance identifies Radio Benkouma, Mousso TV, ORTM and Radio Sahel FM.
- Automatic transcripts were generated and about 40 h were manually corrected.

Bama AI decision: suitable candidate for research and model experiments, subject to attribution, provenance and ShareAlike compliance.

## 2. Jeli-ASR

Status: 🟢 research reuse appears permitted under the published dataset licence.
- Source: https://huggingface.co/datasets/RobotsMali/jeli-asr
- Current published licence: CC BY 4.0.
- Current dataset version: 1.0.1.

Bama AI decision: suitable candidate for research and training experiments. Pin the exact version or commit for reproducibility.

## 3. RobotsMali Soloba ASR model

Status: 🟢 candidate baseline.
- Source: https://huggingface.co/RobotsMali/soloba-ctc-0.6b-v3
- Model licence: CC BY 4.0.
- Model card documents Kunkado and Nyana Eval results.

Bama AI decision: use as an ASR baseline. Model licence and training-data licences remain separate questions.

## 4. Bayelemabaga

Status: 🟢 published dataset licence is clear; 🟡 underlying-source provenance still matters.
- Source: https://huggingface.co/datasets/RobotsMaliAI/bayelemabaga
- Current version shown: 1.0.1.
- Current size: 46,976 aligned lines.
- Published licence: CC BY-SA 4.0.
- It originates from the Corpus Bambara de Référence and 264 text sources.

Bama AI decision: suitable for linguistic research and controlled training experiments under the published licence. Preserve provenance.

## 5. Bambara Reference Corpus (CBR/BRC)

Status: 🟡 permission/licence scope requires further verification before training or redistribution.

The 2013 description identifies the corpus as freely accessible online, with more than one million words and linguistic annotation including tone, POS tags and French glosses. That does not by itself establish blanket permission for every modern redistribution or commercial model-training use.

Bama AI decision: research/inspection only until current access and reuse terms are verified. Do not mirror the corpus into the public repository yet.

## 6. MALIBA-AI Bambara TTS

Status: 🟡 usable for non-commercial research, but not cleared for commercial deployment.
- Source: https://github.com/MALIBA-AI/bambara-tts
- Repository states CC BY-NC-SA 4.0.
- It states non-commercial use, attribution and ShareAlike obligations.
- It also documents consent and anti-impersonation responsibilities.

Bama AI decision: research baseline only unless separate permission is obtained.

## 7. Belebele

Status: 🟢 for evaluation, with licence separation.
- Source: https://github.com/facebookresearch/belebele
- Bambara is included as bam_Latn.
- Project states the benchmark is intended as a test set, not training or validation data.
- Main benchmark licence: CC BY-SA 4.0.
- The assembled training set has different licensing.

Bama AI decision: use as an external evaluation resource. Do not train on the benchmark itself.

## 8. Critical licence rules

1. Dataset licence and model licence are separate.
2. Public access does not automatically mean unrestricted reuse.
3. Benchmark test sets remain isolated from training.
4. CC BY-SA ShareAlike obligations must be tracked.
5. CC BY-NC resources stay in the non-commercial lane unless permission changes.
6. Every resource keeps URL, identifier, version/commit, licence, authors, provenance, access date and checksum when practical.

## 9. Bama AI classification

| Resource | Licence status | Research | Commercial product | Public redistribution |
|---|---|---:|---:|---:|
| Kunkado | CC BY-SA 4.0 | Yes* | Potentially* | Yes* |
| Jeli-ASR | CC BY 4.0 | Yes* | Potentially* | Yes* |
| Soloba v3 | CC BY 4.0 | Yes* | Potentially* | Yes* |
| Bayelemabaga | CC BY-SA 4.0 | Yes* | Potentially* | Yes* |
| CBR/BRC | Scope not fully verified | Research/inspection | Not cleared | Not cleared |
| MALIBA-AI TTS | CC BY-NC-SA 4.0 | Yes* | No, unless authorized | Non-commercial only |
| Belebele benchmark | CC BY-SA 4.0 | Evaluation | Potentially* | Yes* |

* Subject to attribution, provenance, applicable licence terms and upstream restrictions.

## 10. What Bama AI should build itself

Our most important long-term asset should be a new Bamanankan dataset collected by Bama AI with explicit informed consent and an explicit project licence.

For voice data, the collection protocol should define consent, intended AI training use, release scope, commercial/non-commercial permission, withdrawal policy where feasible, metadata minimization, age requirements, recording conditions, transcription rules and orthography/normalization policy.

This gives Bama AI a foundation whose provenance we control instead of relying entirely on inherited corpora.

## 11. Current blockers before Phase 2

1. Verify current CBR/BRC terms.
2. Decide the licence for Bama AI's future first-party dataset.
3. Keep MALIBA-AI TTS research-only unless permission changes.
4. Pin external datasets/models to exact revisions.
5. Create a machine-readable manifest before downloading large resources.
6. Keep benchmark data isolated.
7. Preserve attribution in experiment artifacts.
8. Do not publish a derived mixed dataset until the licence chain is checked.

## 12. Phase 1.5 conclusion

Bama AI can reuse substantial public resources for research, but its long-term foundation should not depend entirely on third-party data.

Therefore we will maintain two data tracks:

### Track A — ecosystem resources
Existing datasets/models for baselines, benchmarking, linguistic study and transfer experiments.

### Track B — Bama AI native data
Our own conversational speech, transcriptions, dialogue pairs, evaluation sets, consented voices and native-speaker preference data.

Track B is the long-term foundation for Bama AI's identity and provenance.

## 13. Next gate

Before Phase 2 model experiments:
1. Create data/manifest.yaml.
2. Record exact versions and licences.
3. Define train/validation/test separation.
4. Define the first reproducible ASR experiment.
5. Download only the minimum required resources.
6. Document the experiment and baseline metrics.

Only after this gate should we begin training or fine-tuning.