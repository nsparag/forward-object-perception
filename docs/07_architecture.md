# FOP-001 Architecture

## High-Level Processing Pipeline

Camera Frame
    ↓
Object Detection
    ↓
Detection Filtering
    ↓
Multi-Object Tracking
    ↓
Track Management
    ↓
Tracked Object List

## Component Responsibilities

### Object Detectio

Responsible for identifying supported road users in the current
camera frame and producing a list of Detection objects.

### Detection Filtering

Responsible for validating and filtering detections before they
are provided to the tracking component.

### Multi-Object Tracking

Responsible for associating current-frame detections with existing
tracks and maintaining object identity across frames.

### Track Management

Responsible for managing the lifecycle of tracks, including:

- Track creation
- Track confirmation
- Temporary track loss
- Track recovery
- Track termination

### Output Publisher

Responsible for converting active tracks into the standard
TrackedObjectList output interface.

### Dataset Adapter

Responsible for converting dataset-specific input into the standard
FOP CameraFrame interface.

For v1.0, a KITTI adapter shall:

- Read KITTI image sequences.
- Preserve frame ordering.
- Generate frame identifiers.
- Provide timing information.
- Convert images into the standard CameraFrame interface.

Dataset-specific logic shall remain outside the core perception feature.