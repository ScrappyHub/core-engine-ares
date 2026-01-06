# ENGINE GOVERNANCE — TRUTH ENGINE (CANONICAL)

Authority Level: Engine Governance (Binding)  
Applies To: This Engine Repository Only  
Status: ✅ BINDING | ✅ NON-OPTIONAL | ✅ INHERITED LAW  

---

## 1. GOVERNANCE INHERITANCE (ACKNOWLEDGEMENT)

This engine is permanently bound by CORE platform governance.

The following documents define all authority above this engine:

- CORE_CONSTITUTIONAL_STOP_LAYER.md  
- CORE_PLATFORM_CONSTITUTION.md  
- CORE_ENGINE_REGISTRY_AND_VERTICAL_INHERITANCE_LAW.md  
- CORE_ENGINE_REGISTRY_CONTRACT.md  
- CORE_GOVERNANCE_INDEX_CHAIN_OF_AUTHORITY.md  

If any content in this repository conflicts with CORE governance →  
**CORE governance wins immediately.**

This repository does not define platform law.

---

## 2. ENGINE ROLE & LIMITATION

This engine is a **TRUTH_ENGINE**.

It is permitted to:
- compute domain-specific physical truth
- emit deterministic, reproducible outputs
- declare domain-specific schemas and artifacts

It is NOT permitted to:
- manage identity, users, or projects
- evaluate permissions, tiers, or billing
- enforce governance or policy
- publish or distribute outputs independently
- infer intent, attribution, or causality
- call other engines directly
- access network or external systems

---

## 3. EXECUTION MODEL (STRICT)

This engine:
- executes headless
- is orchestrated by CORE only
- receives inputs exclusively from CORE
- emits outputs exclusively to CORE

This engine MUST NOT:
- read raw sensor data directly
- persist data outside the sealed output bundle
- mutate outputs after emission

---

## 4. DETERMINISM & REPRODUCIBILITY

All runs MUST be reproducible under identical:
- inputs
- parameters
- engine version
- solver configuration

If nondeterminism exists:
- it MUST be explicitly declared in ENGINE_MANIFEST.json
- it MUST be logged in RUN_CONDITIONS.json
- it MUST be disabled by default unless a CORE lane explicitly enables it

---

## 5. OUTPUT & SEALING REQUIREMENTS

This engine MUST emit:
- canonical JSON outputs
- deterministic field ordering
- SHA-256 hashes as defined by CORE
- artifact index describing all emitted files

This engine MUST NOT:
- alter sealed artifacts
- emit unindexed files
- emit governance or identity metadata

CORE is responsible for sealing verification and storage.

---

## 6. COUPLING RULES

This engine:
- MUST declare coupling permissions in COUPLING_RULES.json
- MUST NOT directly invoke or import other engines
- MUST accept only CORE-mediated coupling

Violation of coupling rules invalidates the run.

---

## 7. SAFETY & MISUSE CONSTRAINTS

This engine MUST:
- label units and coordinate frames
- expose uncertainty and limits
- avoid interpretation outside its physics domain

This engine MUST NOT:
- issue medical, legal, military, or policy conclusions
- issue operational recommendations
- attribute cause or intent

Interpretation is performed only by governed CORE lenses.

---

## 8. VERSIONING & CHANGE CONTROL

Any change to:
- schemas
- determinism guarantees
- artifacts
- coupling permissions

REQUIRES:
- manifest version increment
- registry update
- Git audit trail

Unregistered changes invalidate execution.

---

## 9. FINAL DECLARATION

This engine produces **domain truth only**.

Meaning, classification, authority, and action
are defined **outside this repository** by CORE.

Once committed, this file is treated as **engine-level law**.
