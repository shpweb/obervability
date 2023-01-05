# Observability
## What is Observability?

Observability is the ability to measure a system’s current state based on the data it generates, namely logs, metrics, and traces.


###  Why it matters?

Observability helps cross-functional teams understand and answer specific questions about what’s happening in the systems and objectively measure how well a system is behaving. 

-   Measure  *operational performance*
-   Provide view into the *application health*
-   Measure *business performance*
-   Identify and *diagnose failures* to get to the problem fast.

### How it about more than just Alerting/Monitoring?

Monitoring is mostly functionality to send alerts for issues, that we have *identified*. The assumption that we can predict all the future issues/complications is, unfortunately, misguided.

Modern systems (especially Distributed systems) are highly complex and need a high level of instrumentation; So they can be flexibly explored, to identify the root cause if/when issues occur.

### Pillars of Observability

Logs, metrics, and traces are often known as the three pillars of observability. 

1. Logs
	- Logs are discrete timestamped events with the goal of helping engineers identify problem area(s) during failures.
2. Metrics
	- Metrics provide a near real-time numeric representation of data, about the functions the system is performing as well as its health. 
	- Unlike logging and tracing, metric data tends to be more efficient to transmit and store.
3. Traces
	- Produces the information required to observe series of correlated operations in a distributed system. 
	- Once collected they show the path of an end-to-end transaction.

These are powerful tools that, if understood well and used well, can unlock the ability to build better systems and makes isolating and identifying issues much easier.

### Tools and Patterns

There are a number of modern tools to make systems observable. While identifying and/or creating tools that work for our system, there are a few things to consider.

-   Must be simple to integrate and easy to use
-   It must be possible to aggregate and visualise the data
-   Tools must provide near real-time visibility
-   Must be able to guide users to the problem area with suitable, adequate end-to-end context.

## [Prometheus](prometheus/README.md)  
[Visit [prometheus.io](https://prometheus.io/) for the full documentation, examples and guides.]

**Prometheus**, a Cloud Native Computing Foundation project, is a systems and service monitoring system. It collects metrics from configured targets at given intervals, evaluates rule expressions, displays the results, and can trigger alerts when specified conditions are observed.

***The features that distinguish Prometheus from other metrics and monitoring systems are:***

A multi-dimensional data model (time series defined by metric name and set of key/value dimensions)
PromQL, a powerful and flexible query language to leverage this dimensionality
No dependency on distributed storage; single server nodes are autonomous
An HTTP pull model for time series collection
Pushing time series is supported via an intermediary gateway for batch jobs
Targets are discovered via service discovery or static configuration
Multiple modes of graphing and dashboarding support
Support for hierarchical and horizontal federation

## [Grafana](grafana/README.md)
