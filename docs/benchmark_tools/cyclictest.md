# Cyclictest

## Introduction

Cyclictest is a pure tool used for benchmarking RT systems. The tool measures difference
between a thread's intended wake-up time and the time at which it actually wakes up
in order to provide statistics about the system's latencies.

See: https://wiki.linuxfoundation.org/realtime/documentation/howto/tools/cyclictest/start

In this context, cyclictest is used to measure the RT performance of the system that is then
used to carry out ROS specific benchmarks. In some sense, the generated report provides a
sanity check to verify the system is properly configured. Additionally it sets a baseline
for the performance it is possible to achieve for a simple real-time application running in the system.

## Setup

In Ubuntu install rt-tests:

```
sudo apt install rt-tests
```

Clone configuration files repository in the home directory:

```
git clone https://github.com/ros-realtime/ros_realtime_benchmarks_config
```

## How to run


Run `mklatencyplot` script to run the benchmark and generate the report:

```bash
cd my_experiments
bash ~/ros_realtime_benchmarks_config/cyclictest/mklatencyplot.bash
cp ~/ros_realtime_benchmarks_config/cyclictest/cyclictest_report.md .
```