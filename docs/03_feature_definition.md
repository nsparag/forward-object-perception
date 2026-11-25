# Feature Definition

## FOP-001: Forward Object Perception

### Purpose

The Forward Object Perception feature processes sequential images
from a forward-facing vehicle camera to detect relevant road users
and maintain their identities over time.

The feature provides a temporally consistent representation of
tracked road users to downstream ADAS functions.

### Input

Sequential images from a single forward-facing camera together with
frame timing information.

### Output

A list of tracked road users containing information required by
downstream consumers to identify and distinguish objects over time.