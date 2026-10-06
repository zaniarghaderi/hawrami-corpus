# Human review checklist — ZB

File: `hac_hawrami-zb.conllu`

Status: **preliminary-silver**

The first conversion is intentionally reviewable rather than silently overconfident. Published morphology is used where available; the UD conversion layer still needs human decisions.

## Corpus-level checks

- [ ] Confirm that all 61 units ZB.1–ZB.61 match the intended published transcription.
- [ ] Review all Persian translations against Hawramî, not only against English.
- [ ] Confirm whether source annotation units should remain UD sentences or whether selected multi-clause units should be split.
- [ ] Finalize the project tokenization policy for clitics and multiword tokens.
- [ ] Resolve all `X` UPOS tokens.
- [ ] Review all automatically mapped UD features.
- [ ] Manually review every dependency tree.
- [ ] Run the official UD validator after the language-specific conventions stabilize.

## Linguistic hot spots

Pay particular attention to:

- direct vs. oblique nominal case;
- gender and number on nominals;
- ezafe/linking morphology;
- demonstratives;
- bound person markers and possessive clitics;
- present vs. past alignment;
- transitive past clauses;
- auxiliary/copula analysis;
- existential `hen`;
- complex adpositions and postpositions;
- compound/complex predicates;
- reported speech;
- coordination and parataxis.

## Provenance checks

Each sentence must retain:

- project ID, e.g. `hwr-rec-zb-045`;
- source unit, e.g. `ZB.45`;
- source corpus/book references;
- audio file ID;
- start/end timestamps;
- English and Persian translations.

## Review rule

When changing an analysis, prefer an attested explanation from the published Hewramî grammar/text corpus. If a decision is genuinely uncertain, document the uncertainty rather than forcing a confident annotation.
