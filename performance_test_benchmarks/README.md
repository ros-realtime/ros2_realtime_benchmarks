# pendulum test real-time benchmarks

## Introduction

- [performance_test](https://gitlab.com/ApexAI/performance_test)
- [performance_report](https://gitlab.com/ApexAI/performance_test/-/tree/master/performance_report)
- [Performance Testing in ROS 2](https://drive.google.com/file/d/15nX80RK6aS8abZvQAOnMNUEgh7px9V5S/view)

## Setup

Clone configuration files repository:

```
git clone https://github.com/ros-realtime/performance_test_rt_cfg.git
```

## How to run the benchmakrs

```bash
# Takes around 4 minutes
ros2 run performance_report runner \
  --log-dir perf_logs \
  --test-name experiments \
  --configs ~/performance_test_rt_cfg/runner/run_rt_experiment_single.yaml

# Takes around 24 minutes
ros2 run performance_report runner \
  --log-dir perf_logs \
  --test-name experiments \
  --configs ~/performance_test_rt_cfg/runner/run_rt_experiment_batch.yaml
```

# Generate the plots

```bash
ros2 run performance_report plotter \
  --log-dir perf_logs \
  --configs ~/performance_test_rt_cfg/plotter/plot_experiment_single.yaml

ros2 run performance_report plotter \
  --log-dir perf_logs \
  --configs ~/performance_test_rt_cfg/plotter/plot_experiment_batch_prio90.yaml
```

```bash
ros2 run performance_report plotter \
  --log-dir perf_logs \
  --configs ~/performance_test_rt_cfg/plotter/plot_experiment_batch_prio0.yaml
```

## Generate the reports

```bash
ros2 run performance_report reporter \
  --log-dir perf_logs \
  --configs ~/performance_test_rt_cfg/reporter/report_experiment_single.yaml

ros2 run performance_report reporter \
  --log-dir perf_logs \
  --configs ~/performance_test_rt_cfg/reporter/report_experiment_batch_prio90.yaml

ros2 run performance_report reporter \
  --log-dir perf_logs \
  --configs ~/performance_test_rt_cfg/reporter/report_experiment_batch_prio0.yaml
```
