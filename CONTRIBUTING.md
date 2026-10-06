# Contributing

Thank you for helping document Hawrami.

## Before adding data

- Only add material you are allowed to share.
- Record a source for every item.
- Do not publish identifying speaker information without explicit consent.
- Keep attested corpus data separate from illustrative examples.
- Preserve the original wording before applying any normalization.

## Suggested workflow

1. Add or update source metadata in `data/metadata/sources.tsv`.
2. Add speaker metadata, if applicable, in `data/metadata/speakers.tsv`.
3. Add corpus records to `data/corpus/sentences.tsv`.
4. Document any orthographic or annotation decision that is not already covered.
5. Only export to UD after the source record is stable.

## IDs

Use stable identifiers. Suggested patterns:

- Sentence: `HRM-S000001`
- Speaker: `SPK0001`
- Source: `SRC0001`
- Audio: `AUD000001`

Do not recycle identifiers after deletion.

## Pull requests

A contribution should explain:

- what data or documentation changed;
- where the material came from;
- whether consent or licensing considerations apply;
- whether the change affects UD annotation conventions.
