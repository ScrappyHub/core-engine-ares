# PHYSICS CAPABILITIES — Canonical V1

Engine Key: **ARES**
Authority: Engine Repo (Binding declaration; enforced by CORE Runtime)

## Purpose
Declare supported physics capability keys and explicit exclusions.

## Required Global Controls
- distance_scale_factor ∈ {0.25, 0.50, 0.75, 1.00} (if geometry-dependent)

## Supported Capabilities
- CAP_MOVING_OBJECT_SPEED
- CAP_DISTANCE_SCALING

## Unit Tagging Rules
All outputs MUST be unit-tagged per core-platform/GOVERNANCE/UNITS_AND_CONVERSIONS.md.

## NOT_SUPPORTED
- CAP_WIND_SPEED
- CAP_RAIN_RATE
- CAP_SNOW_RATE
- CAP_HURRICANE_COUPLING
- CAP_TSUNAMI_WAVE_DYNAMICS
- CAP_MUDSLIDE_FLOW
- CAP_LAYERED_MEDIA_RESPONSE
- CAP_EM_FIELD_COUPLING
- CAP_THERMAL_GRADIENTS
- CAP_STRUCTURAL_FAILURE_SIGNATURES
- CAP_CRYSTAL_RESONANCE
- CAP_SIGNAL_TRANSFORMS
- CAP_FUSION_CORRELATION

## Notes
- Engines emit physics only.
- No classification (missile/vehicle/submarine/etc).
- Inputs delivered by CORE only.
