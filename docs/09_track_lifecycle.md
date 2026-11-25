# Track Lifecycle

A tracked object progresses through the following lifecycle:

TENTATIVE -> CONFIRMED -> LOST -> TERMINATED

## TENTATIVE

A new detection creates a tentative track. The track requires
sufficient observations before becoming confirmed.

## CONFIRMED

A track becomes confirmed after satisfying the configured confirmation
criteria.

## LOST

A confirmed track becomes lost when no matching detection is available.
A lost track may be recovered if a matching detection is found before
the configured deletion timeout.

## TERMINATED

A lost track is terminated when the configured deletion criteria are
satisfied.

Terminated tracks are removed from the active tracked-object list.