# Data model

## Sentence record

Each sentence should minimally have:

- `sentence_id`: stable unique identifier
- `text_original`: text exactly as collected or published
- `source_id`: link to provenance metadata

Recommended when available:

- `text_normalized`
- `translation_fa`
- `translation_en`
- `speaker_id`
- `region`
- `genre`
- `audio_id`
- `notes`

## Separation of layers

The project distinguishes:

1. **Source layer** — what was actually said or written.
2. **Normalized layer** — optional orthographic normalization.
3. **Translation layer** — Persian and/or English.
4. **Linguistic annotation layer** — lemma, POS, morphology, syntax.
5. **UD export layer** — standardized CoNLL-U representation.

Never overwrite the source layer with normalized text.
