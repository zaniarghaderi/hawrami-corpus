# Universal Dependencies

This directory is reserved for the Hawrami UD annotation layer.

The intended future treebank is provisionally:

`UD_Gurani-Hawrami`

This name should be confirmed with the Universal Dependencies maintainers before treating it as official.

## Rules

- UD data must derive from attested corpus records.
- Keep source sentence IDs traceable.
- Use CoNLL-U.
- Validate files with the official UD validator before release.
- Record language-specific annotation decisions in `docs/annotation-guidelines.md`.

No fabricated example sentences should be committed as corpus data.
