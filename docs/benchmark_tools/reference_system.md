# Reference system

## Introduction

The reference_system package was developed to provide the fundamental building blocks to create complex systems that then can be used to evaluate features or performance in a standardized and repeatable way.

It is specially useful to compare the performance of different ROS executors.

See:

- Repository: [https://github.com/ros-realtime/reference-system](https://github.com/ros-realtime/reference-system)
- Docs: [https://ros-realtime.github.io/reference-system/main/](https://ros-realtime.github.io/reference-system/main/)
- [Introduction to the reference system](https://www.youtube.com/watch?v=76pzSsLjVFo&feature=youtu.be)

## Setup

TODO

## Run the demo and generate the report

We run the benchmark for the rclcpp single threaded executor with and without priority:

```bash
python3 $(ros2 pkg prefix --share autoware_reference_system)/scripts/benchmark.py 120 autoware_default_singlethreaded,autoware_default_prioritized
```