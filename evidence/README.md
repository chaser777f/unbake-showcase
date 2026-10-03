# About this evidence

This folder contains a manually curated, sanitized summary of existing Unbake experiment records, inspected on October 3, 2026. It is not raw benchmark output and it is not a new execution or an independent reproduction performed for this showcase.

The source-artifact names and SHA-256 hashes in `results.json` identify the local records used to prepare the summary. Those originals are not included in this public repository. Hashes support artifact identity; without the originals and executable, they do not independently prove the results.

## Retained information

- Compiler/toolset identity, experiment counts, match outcomes, and selection limits.
- Two function-body hashes for recorded exact offline matches.
- Source-artifact identities and hashes, with project-relative names only.
- The difference between answer-key validation, model results, offline investigation, known-case replay, and fresh evaluation.

## Omitted information

Machine-specific paths, account details, executable payloads, target byte arrays, source implementations, generated candidates, address-binding maps, provider prompts/replies, and third-party source are not included. No credentials or account connection is required to read this showcase.

## Interpreting the checks

The ItemAdd review independently applied relocations relative to the match comparator, while still using the project's COFF reader. The BeginDragDropTarget review went further: it used separate standard-library COFF parsing and manual relocation encoding, with `pefile` reading target bytes. Both comparisons covered the recorded function body under its recorded compiler and bindings.

The historical test count is reported from the saved coverage review. Tests were not rerun while preparing this repository. No new model calls or compiler invocations were made for the showcase.
