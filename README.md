[![Simulation](../../actions/workflows/main.yml/badge.svg)](../../actions/workflows/main.yml)

# Lesson 5 - Time series

The goal of this lesson is to familiarize you with how manage time in a GridLAB-D simulation. The specific learning objectives are the following

1. How to specify the timezone.
2. How to specify the start time.
3. How to specify the stop time.

## Clock

To manage time in a simulation, you must use the `clock` directive.  This directive allows three parameters settings:

1. `timezone`: this is used to specify which timezone and daylight saving's time rules are in effect.
2. `starttime`: this is used to specify the date and time at which the simulation starts.
3. `stoptime`: this is used to specify the date and time at which the simulation stop.

The clock is only active when there is an upcoming change in the state of one or more objects in the model. For example, adding weather will always result in changes every hour. As a result the simuation will run forever unless a stop time is specified.  The simulation will always stop at the stop time or if there is not pending state change in an object.

## Tasks

The following tasks are illustrated in [`main.glm`](main.glm):

1. Set the clock to run from January 1, 2020 midnight PST to January 1, 2021 midnight PST (see [`main.glm@7'](main.glm#L7-L12)).
   1. Set `timezone` to `PST+8PDT` (see [`main.glm@9`](main.glm#L9)).
   2. Set `starttime` to `2020-01-01 00:00:00 PST` (see [`main.glm@10`](main.glm#L10)).
   3. Set `stoptime` to `2021-01-01 00:00:00 PST` (see [`main.glm@11`](main.glm#L11)).
2. Get and load weather data for Los Angeles (see [`main.glm@14`](main.glm#L15-18))

# Exercises

1. Change the location to Phoenix, Arizona. (Hint: there is no daylight savings time in Arizona.)

# More Information

* [Clock](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/GLM/Directive&doc=/GLM/Directive/Clock.md)
 * [Weather](https://docs.gridlabd.us/_page.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Subcommand&doc=/Subcommand/Weather.md)

# Next Lesson

* [Lesson 7 - Managing Weather](../../../lesson-7)
