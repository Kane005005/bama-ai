# Dataset Strategy

Bama AI treats data as a core research asset.

## Dataset families

### Language data

Words and concepts, sentences, dialogue turns, questions and answers, grammar examples, idioms, proverbs, stories, instructions and everyday conversations.

### Speech data

Where legally and ethically appropriate, usable samples should have:

- audio;
- exact transcript;
- language/variant information;
- minimum necessary speaker metadata;
- recording conditions;
- provenance;
- consent/license information;
- dataset version.

### Evaluation data

Evaluation sets must be separated from training data and represent real use cases, including difficult examples.

## Data quality

Priorities:

- accurate transcription;
- natural language;
- speaker diversity;
- balanced domains;
- clear provenance;
- consistent metadata;
- duplicate detection;
- quality review.

## Data lifecycle

**Collect → verify → normalize → annotate → validate → version → evaluate → document**

Raw data should not be silently modified. Processing steps must be reproducible.

## Consent

Voice recordings are personal data. We will not collect or publish someone's voice for model training without an appropriate basis and informed consent.

Contributors should know what is recorded, why it is collected, how it may be used, whether it is publicly redistributed, whether commercial use is possible, and how withdrawal is handled where applicable.

## Licensing

Every dataset or external source must have documented licensing/provenance before inclusion.

A permissive code license does not automatically make datasets or recorded voices permissively licensed.

## Directory policy

- data/raw/: original files; do not commit sensitive/private material.
- data/processed/: derived data that is safe and permitted to store.
- data/metadata/: schemas, manifests and documentation.

Large datasets may live outside GitHub. The repository should contain manifests, documentation, checksums and download instructions when appropriate.
