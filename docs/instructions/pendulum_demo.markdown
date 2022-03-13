# Instructions for pendulum demo real-time benchmark

## Introduction

- [pendulum_control](https://github.com/ros2/demos/tree/galactic/pendulum_control)
- [Real-time programming in ROS 2](https://docs.ros.org/en/rolling/Tutorials/Real-Time-Programming.html)

## Setup

TODO

## Run the demo

Run the pendulum demo with the following settings:
- update period (-u): 1 millisecond
- maximum heap prefault size for dynamic memory (-d): 200 MB
- real-time loop iterations (-i): 60000
- thread priority (-t): 90
- sched policy (-s): SCHED_FIFO

```bash
pendulum_demo -d 200mb -t 90 -s fifo -u 1ms -i 60000 -f pendulum_demo_results
```

See all the options available in the
[rttest](https://github.com/ros2/realtime_support/tree/master/rttest) repository.

## Generate the plots

```bash
rttest_plot pendulum_demo_results
```

## Generate statistics

Use the [analyze.py](https://github.com/ros2/realtime_support/blob/master/rttest/scripts/analyze.py)
script to show the resulting statistics:

```bash
python3 analyze.py | tee pendulum_demo_results_statistics.txt
```
