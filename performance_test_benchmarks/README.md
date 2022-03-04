# pendulum test real-time benchmarks

## How to run the benchmakrs

Run the pendulum demo wuth the following settings:
- update period (-u): 1 millisecond
- maximum heap prefault size for dynamic memory (-d): 
- real-time loop iterations (-i): 60000
- thread priority (-t): 90
- sched policy (-s): SCHED_FIFO

```bash
pendulum_demo -d 200mb -t 90 -s fifo -u 1ms -i 60000 -f pendulum_demo_results
```

See all the options available in the 
[rttest](https://github.com/ros2/realtime_support/tree/master/rttest) repository.

## How to generate the reports

```bash
rttest_plot pendulum_demo_results
```

## How to generate the plots