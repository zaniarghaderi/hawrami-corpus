# Annotation guidelines

Status: **working draft — ZB first-pass annotation**

These guidelines document the initial conversion of Hewramî source material into a future Universal Dependencies-compatible annotation. They are not final language-specific UD guidelines yet.

## 1. Source unit and project IDs

Source annotation-unit IDs are preserved exactly in metadata, e.g.:

`ZB.1`, `ZB.2`, … `ZB.61`

The corresponding stable project IDs use:

```text
hwr-rec-<text-code>-<three-digit-unit>
```

For the first text:

```text
ZB.1  → hwr-rec-zb-001
ZB.61 → hwr-rec-zb-061
```

This keeps the project ID globally understandable while making the original corpus location recoverable.

## 2. Segmentation

For the first import, the source's numbered annotation units are treated as CoNLL-U sentence units even when one annotation unit contains more than one orthographic sentence or clause.

This is intentional: the Zenodo corpus describes these numbered items as annotation units, usually corresponding to intonation units. Preserving them keeps text/audio/source alignment stable.

Future work may introduce finer syntactic sentence segmentation, but any split must retain the original `ZB.N` provenance.

## 3. Canonical transcription

For ZB:

- audio timing comes from the supplied ELAN file;
- canonical linguistic transcription follows the published glossed edition in _Echoes of the past: Hewramî narratives_;
- the original archive PDF/EAF remains provenance evidence.

The archive itself instructs users to consult the book for the most updated transcription and translation.

No normalized spelling is silently substituted for the source form.

## 4. English and Persian translations

English translation follows the published glossed text.

Persian translation was created for this project from the published Hewramî/English analysis and is marked as project-derived. It must be human-reviewed, especially where the earlier archive PDF and the later published analysis differ.

## 5. Morphological analysis

The ZB source morphology is based on the published interlinear analysis, not generated from surface forms alone.

The first conversion maps clear source categories to UD features where a straightforward mapping exists, including:

- direct / oblique → `Case=Dir` / `Case=Obl`;
- masculine / feminine → `Gender=Masc` / `Gender=Fem`;
- singular / plural → `Number=Sing` / `Number=Plur`;
- definite / indefinite → `Definite=Def` / `Definite=Ind`;
- present / past → `Tense=Pres` / `Tense=Past`;
- indicative / subjunctive / imperative → `Mood=Ind` / `Mood=Sub` / `Mood=Imp`;
- negative → `Polarity=Neg`;
- passive → `Voice=Pass`;
- participle → `VerbForm=Part`.

Not every descriptive category in the Hewramî grammar has yet been assigned a final UD representation.

## 6. Lemmas and UPOS

Where available, lemmas and source word classes are derived from the published Hewramî-English glossary associated with the grammar.

UPOS is mapped from those source classes plus the interlinear gloss. A form remains `X` when the current conversion cannot assign a sufficiently defensible UPOS automatically.

Do not resolve `X` values merely by analogy; review the published grammar and the local construction.

## 7. Clitics and orthographic words

The published interlinear analysis identifies many clitics and bound elements with `=` and morphological boundaries with `-`.

The current first-pass CoNLL-U keeps the **surface orthographic word as FORM** rather than automatically splitting every source clitic into separate syntactic words. The source interlinear gloss is retained in `MISC` as `Gloss=...`.

This is a deliberate temporary policy. Hawramî clitics must be reviewed construction by construction before final UD tokenization / multiword-token rules are adopted.

High-priority clitics include person indexing, possessive/non-canonical clitics, additive particles, postpositional elements, and copular material.

## 8. Dependency annotation

Dependencies in the first ZB conversion are **machine-assisted preliminary parses**. They are not derived directly from the published interlinear gloss and must be manually reviewed.

Review is especially important for:

- Hewramî alignment and past transitive constructions;
- argument indexing and pronominal clitics;
- zero arguments;
- copular predicates;
- existential constructions;
- ezafe/linker structures;
- complex predicates;
- adpositions/postpositions;
- coordination;
- reported speech;
- subordinate clauses;
- source units containing multiple clauses.

Until review is complete, dependency labels should be treated as silver data only.

## 9. Evidence hierarchy

When resolving an annotation question for ZB, use this order:

1. the actual recording / ELAN alignment;
2. the published glossed ZB text in _Echoes of the past_;
3. _A grammar of Hewramî_ and its Hewramî-English glossary;
4. other attested Hewramî corpus examples;
5. comparison with related Iranian languages only as supporting evidence, never as a substitute for Hewramî evidence.

## 10. Review discipline

Every non-obvious convention should eventually document:

1. the decision;
2. linguistic rationale;
3. attested examples;
4. the corresponding UD relation or feature;
5. whether the decision is project-specific or proposed as a general Hewramî UD convention.
