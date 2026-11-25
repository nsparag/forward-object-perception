# Requirements

## Functional Requirements

### FOP-FR-001: Camera Frame Processing

The Forward Object Perception feature shall process sequential image
frames from a single forward-facing camera in chronological order.

### FOP-FR-002: Object Detection

The Forward Object Perception feature shall detect supported road-user
classes within each processed camera frame.

For v1.0, the supported road-user classes are:

- Car
- Pedestrian

### FOP-FR-003: Multi-Object Tracking

The Forward Object Perception feature shall track multiple detected
road users across consecutive camera frames.

Each tracked road user shall be assigned a track identifier that
enables the same object to be distinguished from other tracked objects.