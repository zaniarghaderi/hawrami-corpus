# Hawrami Corpus

An open, community-oriented corpus project for documenting and preserving **Hawrami / Hewramî** and for developing linguistic resources that can support a future **Universal Dependencies (UD)** treebank.

## Goals

This repository is intended to become the canonical source for:

- carefully sourced Hawrami text;
- Persian and English translations where available;
- linguistic and source metadata;
- optional audio-linked transcriptions;
- orthographic and annotation documentation;
- reproducible exports to Universal Dependencies / CoNLL-U.

The UD-facing target is a Hawrami treebank under **Gurani (ISO 639-3: `hac`)**, provisionally referred to as **UD_Gurani-Hawrami**. The official UD repository name remains subject to confirmation by the Universal Dependencies maintainers.

## Principles

1. **No invented corpus data.** Documentation examples must be clearly marked and must never be mixed with attested corpus records.
2. **Traceability.** Every corpus sentence should have a stable ID and a documented source.
3. **Speaker privacy.** Public data should use anonymized speaker IDs unless a source already publishes attribution or a speaker explicitly chooses attribution.
4. **Consent and rights first.** Recorded or elicited material should only be redistributed when its rights and publication basis are documented.
5. **Source vs. annotation.** The preservation corpus is the primary dataset; UD is a derived annotation layer.
6. **Reproducibility.** Transformations from corpus records to UD files should be scriptable and documented.
7. **Human review.** Automatically assisted linguistic annotation is explicitly marked and is not treated as gold data until reviewed.

## Current dataset

The first imported text is:

- **ZB — _zaroɫe û bizê_ (“The baby and the goat”)**
- Source corpus: Masoud Mohammadirad, _A corpus of Hewramî recordings, time-aligned with transcription and translation_ (Zenodo DOI: `10.5281/zenodo.15419952`)
- Published linguistic source: Masoud Mohammadirad, _Echoes of the past: Hewramî narratives_ (Language Science Press, 2025; DOI: `10.5281/zenodo.17140764`)
- Source units: **ZB.1–ZB.61**
- Project sentence IDs: **`hwr-rec-zb-001`–`hwr-rec-zb-061`**
- Audio alignment: preserved from the supplied ELAN file `ZB-001-speaker4.eaf`
- English translations and interlinear morphology: based on the published glossed text
- Persian translations: project translations, currently awaiting human review
- UD layer: **preliminary / silver**, awaiting manual linguistic review

The source archive itself recommends consulting the book for the most up-to-date transcription and translation. Consequently, the repository uses the published glossed edition as the canonical linguistic transcription for ZB while retaining audio offsets from the ELAN annotation.

### Annotation status

`data/ud/hac_hawrami-zb.conllu` contains a first CoNLL-U conversion of all 61 ZB annotation units.

The source morphology is not guessed: it is derived from Mohammadirad's published interlinear morpheme segmentation and glosses, cross-checked with the Hewramî glossary. Mapping that analysis to UD UPOS/FEATS and especially the dependency trees is, however, a **machine-assisted preliminary conversion**. It must be reviewed by a competent human annotator before being considered a gold UD treebank.

## Repository structure

```text
hawrami-corpus/
├── README.md
├── CONTRIBUTING.md
├── data/
│   ├── README.md
│   ├── corpus/
│   │   └── sentences.tsv
│   ├── metadata/
│   │   ├── speakers.tsv
│   │   └── sources.tsv
│   ├── audio/
│   │   └── README.md
│   └── ud/
│       ├── README.md
│       ├── REVIEW.md
│       └── hac_hawrami-zb.conllu
├── docs/
│   ├── annotation-guidelines.md
│   ├── data-model.md
│   ├── ethics-and-consent.md
│   ├── licensing.md
│   └── orthography.md
└── scripts/
    └── README.md
```

## Milestone 0 — UD bootstrap

- [ ] Agree on project orthography and normalization policy
- [ ] Agree on corpus/data license
- [x] Add the first attested Hawrami text with source provenance
- [x] Add Persian and English translations for the first text
- [ ] Finalize lemma and UPOS conventions
- [ ] Finalize morphological feature conventions
- [ ] Finalize dependency annotation conventions
- [x] Produce an initial structurally well-formed CoNLL-U draft
- [ ] Complete human review of the first text
- [ ] Pass the official UD validator under the final language/treebank configuration
- [ ] Contact the UD maintainers about the official treebank repository

For a first UD contribution, quality and consistency are more important than dataset size.

## Data status

The repository has moved from an empty bootstrap template to its **first real-text review phase**. ZB contains 61 source annotation units. The corpus TSV and the CoNLL-U layer are populated, but the UD conversion is deliberately labeled preliminary until manual review is complete.

## Licensing

Licensing is tracked per source/layer rather than assumed globally.

The published _Echoes of the past: Hewramî narratives_ is CC BY 4.0. Rights for source recordings and other archive components should be checked against the relevant source record before redistributing those files. This repository currently references the audio alignment but does **not** redistribute the uploaded WAV recording.

See `docs/licensing.md` and `data/metadata/sources.tsv`.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).
