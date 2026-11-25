# ADR-001: Implementation Language

## Status

Accepted

## Decision

Python will be used as the initial implementation language for
FOP-001 v1.0.

## Rationale

Python is selected for the initial implementation because it provides:

- Strong computer-vision and machine-learning ecosystem.
- Easy integration with PyTorch and OpenCV.
- Rapid development of perception algorithms.
- Good support for KITTI evaluation tooling.
- Straightforward profiling and experimentation.

## Consequences

Python will be used for the v1.0 reference implementation.

Performance-critical components may later be optimized or migrated
to C++ if profiling demonstrates the need.