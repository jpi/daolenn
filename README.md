# Daolenn -- a modular job scheduler

## Goals

* lean
* predictable


## Design

* multi-process
  * launcher: forks processes
  * dispatcher: consumes events, keeps track of jobs, and tells launcher to launch programs
  * event sources:
    * calendar
    * filesystem
    * ...
* HTTP-like protocol for internal communications (main difference: bidirectional)
