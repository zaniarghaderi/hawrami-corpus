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
3. **Speaker privacy.** Public data should use anonymized speaker IDs unless a speaker explicitly chooses attribution.
4. **Consent first.** Recorded or elicited material should only be published under a documented consent basis.
5. **Source vs. annotation.** The preservation corpus is the primary dataset; UD is a derived annotation layer.
6. **Reproducibility.** Transformations from corpus records to UD files should be scriptable and documented.

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
│       └── README.md
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
- [ ] Add the first attested Hawrami sentences with sources
- [ ] Add Persian and English translations where available
- [ ] Establish lemma and UPOS conventions
- [ ] Establish morphological feature conventions
- [ ] Establish dependency annotation conventions
- [ ] Produce an initial valid CoNLL-U sample
- [ ] Run the official UD validator
- [ ] Contact the UD maintainers about the official treebank repository

For a first UD contribution, quality and consistency are more important than dataset size.

## Data status

The repository is currently in the **bootstrap phase**. Template TSV files contain schemas/headers only until real, sourced material is added.

## License

**Not yet selected.** Before corpus data is published, the maintainers should choose a license compatible with the rights and consent attached to the source material and suitable for the intended UD contribution.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).
