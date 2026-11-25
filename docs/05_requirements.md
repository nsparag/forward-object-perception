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

### FOP-FR-004: Track Identity Persistence

The Forward Object Perception feature shall maintain the same track
identifier for a road user across consecutive frames while that road
user remains successfully tracked.

### FOP-FR-005: Temporary Track Loss

The Forward Object Perception feature shall support temporary loss
of object detections without immediately terminating the corresponding
track.

The duration for which a track may remain without an associated
detection shall be configurable.

### FOP-FR-006: Track Termination

The Forward Object Perception feature shall terminate a track when
the configured track deletion criteria are satisfied.

A terminated track shall no longer be included in the published list
of active tracked road users.

### FOP-FR-007: Tracked Object Output

The Forward Object Perception feature shall publish a tracked-object
list for each successfully processed camera frame.

Each tracked object shall contain at least:

- Track identifier
- Object class
- 2D bounding box
- Confidence
- Track state

The published object list shall be associated with the corresponding
input frame and timestamp.

## Performance Requirements

### FOP-PR-001: Processing Throughput

The Forward Object Perception feature shall target an average
processing throughput of at least 25 frames per second on the
defined reference hardware.

The achieved throughput shall be measured and reported during
performance verification.