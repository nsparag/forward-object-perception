# Feature Scope

## FOP-001: Forward Object Perception

### In Scope

The feature is responsible for:

- Receiving sequential images from a single forward-facing camera.
- Detecting supported road users in each frame.
- Tracking multiple road users across consecutive frames.
- Assigning and maintaining an identity for each tracked object.
- Managing creation, update, temporary loss, and termination of tracks.
- Publishing the current list of tracked road users.

### Out of Scope

The following capabilities are not part of FOP-001 v1.0:

- 3D object detection.
- Distance estimation.
- Lane detection.
- Traffic sign or traffic light detection.
- Trajectory prediction.
- Time-to-collision estimation.
- Collision warning.
- Sensor fusion.
- Vehicle control or actuation.