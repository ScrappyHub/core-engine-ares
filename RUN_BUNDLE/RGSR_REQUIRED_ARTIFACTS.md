# RGSR REQUIRED ARTIFACTS (Canonical V1)

RGSR is a fusion engine. It must always emit and preserve upstream provenance.

## Required (in addition to standard RUN_BUNDLE spec)

### Required Provenance Artifact
- `INPUT_ARTIFACT_INDEX.json`

This file must list **all upstream artifacts** used by RGSR for the run, each with:
- engine_code
- artifact_name
- sha256

## Required Output Fields (RUN_OUTPUT.json)
- semantics = CORRELATION_ONLY
- inputs_hash
- outputs_hash
- input_artifact_index (array; same content class as INPUT_ARTIFACT_INDEX.json)

## Prohibitions
RGSR output must not include:
- causal claims
- attribution labels (missile/rocket/submarine intent language)
- identity/governance/billing fields
