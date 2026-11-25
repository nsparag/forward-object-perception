# Benchmark Definition

## Reference Dataset

FOP-001 v1.0 shall use the KITTI Object Tracking Benchmark as the
reference dataset for development and evaluation.

## Evaluation Classes

The initial evaluation shall focus on:

- Car
- Pedestrian

## Primary Tracking Metric

- HOTA (Higher Order Tracking Accuracy)

## Supporting Metrics

The following metrics shall be recorded to understand tracking
performance:

- DetA - Detection Accuracy
- AssA - Association Accuracy
- ID switches
- Fragmentation

## Runtime Metrics

The implementation shall also measure:

- Processing FPS
- Mean processing latency
- P95 processing latency

## Purpose

The benchmark provides a standardized and reproducible method for
measuring FOP-001 and comparing its performance against reference
tracking approaches.