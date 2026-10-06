# Universal Dependencies

This directory contains the Hawrami UD annotation layer.

The intended future official treebank is provisionally:

`UD_Gurani-Hawrami`

This name should be confirmed with the Universal Dependencies maintainers before treating it as official.

## Current file

### `hac_hawrami-zb.conllu`

First text:

- Text code: `ZB`
- Title: _zaroɫe û bizê_ (“The baby and the goat”)
- Source units: `ZB.1`–`ZB.61`
- Project IDs: `hwr-rec-zb-001`–`hwr-rec-zb-061`
- Source archive: DOI `10.5281/zenodo.15419952`
- Published glossed source: _Echoes of the past: Hewramî narratives_ (Mohammadirad 2025)
- Status: **preliminary-silver**
- Human review: **required**

Each CoNLL-U sentence includes the original source unit ID, project ID, Hawrami text, English translation, Persian project translation, audio filename, and millisecond-derived start/end offsets.

## What is source-derived vs. project-derived?

**Source-derived / published:**

- ZB segmentation and identifiers;
- canonical Hawrami transcription;
- English translation;
- interlinear morpheme segmentation and morphological glosses;
- audio alignment from the ELAN source.

**Project-derived:**

- Persian translations;
- mapping from the published analysis to UD UPOS and FEATS;
- lemmas where not directly recoverable from the published glossary;
- dependency trees.

The project-derived linguistic layer is a first-pass conversion intended for human correction, not a claim of gold-standard annotation.

## Review priorities

See [REVIEW.md](REVIEW.md). In particular, review:

1. all tokens currently tagged `X`;
2. clitic and multiword-token treatment;
3. ezafe / linker analysis;
4. postpositions and complex adpositions;
5. copular and existential constructions;
6. past transitive / alignment-sensitive clauses;
7. person indexing and pronominal clitics;
8. coordination and clause boundaries;
9. dependency heads and relations.

## Rules

- UD data must derive from attested corpus records.
- Keep source sentence IDs traceable.
- Use CoNLL-U.
- Do not silently alter the source transcription.
- Record language-specific annotation decisions in `docs/annotation-guidelines.md`.
- Validate files with the official UD validator before proposing an upstream release.

No fabricated example sentences should be committed as corpus data.
