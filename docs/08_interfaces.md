# FOP-001 Interfaces

## Input Interface

### CameraFrame

The Forward Object Perception feature shall receive one camera frame
at a time.

A CameraFrame contains:

- frame_id
- timestamp
- image
- width
- height

The interface shall remain independent of the dataset or camera source.

## Output Interface

### TrackedObject

Each tracked object shall contain:

- track_id
- object_class
- bounding_box
- confidence
- track_state

### TrackedObjectList

For each processed frame, the feature shall publish a TrackedObjectList
containing:

- frame_id
- timestamp
- object_count
- tracked_objects

The output interface shall remain independent of the detector and
tracker implementations.

## Internal Interfaces

### Detection

The Object Detection component shall provide detections to the
tracking component.

Each Detection shall contain:

- object_class
- bounding_box
- confidence

The Detection interface shall remain independent of the specific
object detection algorithm or model.

### TrackState

Each tracked object shall have a track state indicating its current
lifecycle status.

Supported states for v1.0:

- TENTATIVE
- CONFIRMED
- LOST

### ObjectClass

The perception feature shall use an internal object-class definition
that is independent of the dataset and detector implementation.

Supported classes for v1.0:

- CAR
- PEDESTRIAN
- UNKNOWN

### BoundingBox

A 2D bounding box shall be represented in image pixel coordinates as:

- x_min
- y_min
- x_max
- y_max

The coordinate origin shall be the top-left corner of the image.

Bounding boxes passed through FOP internal interfaces shall use this
common representation regardless of the representation used by the
dataset or detection model.