# Licensing

Status: **layer-specific licensing in progress**

The project does not assume that all corpus layers have the same rights status.

## Current ZB import

The first imported text, ZB (_zaroɫe û bizê_), uses two closely related published resources:

1. Masoud Mohammadirad, _Echoes of the past: Hewramî narratives_ (Language Science Press, 2025), which is published under **CC BY 4.0**.
2. The associated Zenodo archive, _A corpus of Hewramî recordings, time-aligned with transcription and translation_ (DOI `10.5281/zenodo.15419952`), used for source provenance and ELAN/audio timing.

The repository currently redistributes **textual derived data and annotations**, not the supplied WAV recording.

Before redistributing any source audio or additional archive files, verify the rights metadata that applies to that particular source component rather than inferring it from the book license.

## Project-created layers

The following are project-created or project-derived layers and should have their licensing finalized before an upstream/public release policy is declared:

- Persian translations;
- UD UPOS/FEATS conversion;
- dependency annotation;
- project metadata and scripts.

## Rule

For every imported source, record:

1. creator;
2. stable source/DOI;
3. rights status;
4. applicable license;
5. whether the repository stores the original work or only a derived annotation;
6. any attribution requirements.

Do not copy a source license onto another layer unless that license actually applies to that layer.
