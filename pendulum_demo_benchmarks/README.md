# pendulum demo

## Introduction

- [pendulum_control](https://github.com/ros2/demos/tree/galactic/pendulum_control)
- [Real-time programming in ROS 2](https://docs.ros.org/en/rolling/Tutorials/Real-Time-Programming.html)

## How to run the demo

Run the pendulum demo wuth the following settings:
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

## How to generate the plots

```bash
rttest_plot pendulum_demo_results
```
