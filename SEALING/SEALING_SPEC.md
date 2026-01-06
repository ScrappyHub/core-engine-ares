# ENGINE SEALING SPEC (CANONICAL)

## Purpose
This engine must emit deterministic, reproducible artifacts that CORE can seal and verify.

## Canonical Output Rules
1. Output MUST be valid UTF-8 JSON.
2. Output MUST be deterministic under identical inputs + parameters + engine version.
3. Output MUST NOT include:
   - user identity
   - governance state (roles, tiers, feature flags)
   - billing/monetization signals
4. Output MUST include:
   - run_id
   - engine_code + engine_version
   - inputs_hash (sha256 of canonical input JSON text)
   - outputs_hash (sha256 of canonical output JSON text)

## Hashing
- Hash algorithm: SHA-256
- Canonicalization: JSON serialized text (CORE defines canonical serializer).
- Engines must not reorder fields nondeterministically.

## What CORE seals
CORE seals:
- ENGINE_MANIFEST.json (definition)
- INPUT_SCHEMA.json / OUTPUT_SCHEMA.json
- Run input payload (RUN_INPUT)
- Run output payload (RUN_OUTPUT)
- Run metadata (RUN_META)

Engines do not modify sealed artifacts after emission.
