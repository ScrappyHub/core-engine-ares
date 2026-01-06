# ARES — Acoustic Resonance Engine

ARES is a **deterministic acoustic physics engine** within the CORE Engine Family.

ARES computes **acoustic domain truth only**.  
It does not manage users, governance, policy, or publishing.

---

## Engine Role

**Engine Type:** TRUTH_ENGINE  
**Domain:** Acoustics  
**Governance Owner:** CORE Platform  
**Execution Context:** CORE-orchestrated only

ARES produces sealed, reproducible acoustic outputs suitable for scientific,
engineering, and cross-domain fusion analysis.

---

## What ARES Computes

ARES models acoustic wave behavior including:

- wave propagation and attenuation
- boundary reflection and absorption
- standing waves and modal structure
- harmonic resonance and Q-factor estimates
- pressure / velocity fields (as declared by schema)

ARES outputs **measured or computed fields**, never interpretations.

---

## What ARES Does NOT Do

ARES does NOT:

- access sensors or devices directly
- manage identity, permissions, or billing
- infer intent, attribution, or causality
- perform medical, biological, or defense classification
- publish data or make decisions
- call other engines directly
- access networks or external systems

ARES is compute-only.

---

## Determinism & Reproducibility

ARES runs are reproducible given identical:

- geometry and material inputs
- boundary conditions
- excitation definitions
- solver parameters
- engine version

Any non-deterministic behavior must be explicitly declared in the manifest and
is disabled by default.

---

## Outputs & Sealing

ARES emits a **sealed artifact bundle** including:

- canonical input payload
- canonical output payload
- manifest + schema references
- SHA-256 hashes for verification
- domain artifacts (modal maps, spectra, fields)

All outputs are sealed and verified by CORE.

---

## Governance

ARES is permanently bound by CORE governance:

- CORE_CONSTITUTIONAL_STOP_LAYER
- CORE_PLATFORM_CONSTITUTION
- CORE_ENGINE_REGISTRY_AND_VERTICAL_INHERITANCE_LAW
- CORE_ENGINE_REGISTRY_CONTRACT

This repository contains **engine truth only**.

---

## License & Use

ARES is intended for governed execution inside CORE.

Direct, ungoverned use is unsupported.
