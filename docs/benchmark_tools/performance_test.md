# performance_test

## Introduction

- [performance_test](https://gitlab.com/ApexAI/performance_test)
- [performance_report](https://gitlab.com/ApexAI/performance_test/-/tree/master/performance_report)
- [Performance Testing in ROS 2](https://drive.google.com/file/d/15nX80RK6aS8abZvQAOnMNUEgh7px9V5S/view)

## Setup

Build `performance_test` following the official instructions:

- https://gitlab.com/ApexAI/performance_test#building-the-performance_test-tool

Clone configuration files repository in the home directory:

```
git clone https://github.com/ros-realtime/performance_test_rt_cfg.git
```

# Run the experiments

```bash
# It takes around 24 minutes
ros2 run performance_report runner \
--log-dir $log_dir \
--test-name experiments \
--configs ~/ros_realtime_benchmarks_config/performance_test/runner/run_compare_all.yaml
```

## Generate the reports

```bash
ros2 run performance_report reporter \
--log-dir $log_dir \
--configs ~/ros_realtime_benchmarks_config/performance_test/reporter/compare_experiment_settings/*.yaml
```
