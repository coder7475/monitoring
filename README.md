# Grafana Stack Overview

## Grafana Stack Components

1. **Grafana Loki**:

   - A log aggregation system designed for collecting and querying logs.
   - Uses **LogQL** for querying logs, similar to how Prometheus uses PromQL for metrics.

2. **Prometheus**:

   - A metrics monitoring system that collects and stores metrics as time-series data.
   - Uses **PromQL** for querying these metrics.
   - **Mimir** is mentioned as a scalable extension to Prometheus, enabling handling larger datasets.

3. **Tempo**:

   - A distributed tracing backend designed to collect traces of requests as they flow through a system.
   - Useful for understanding performance and identifying bottlenecks in microservices.

4. **Pyroscope**:
   - A continuous profiling platform for monitoring the performance of applications.
   - Helps developers understand how resources are used by different parts of an application.

## Telemetry Signals

Telemetry signals are types of data collected for observability, which include:

1. **Logs**:

   - A chronological record of events that occur while a component is running.
   - Provides a running feed of context about the system's activities and behavior.

2. **Metrics**:

   - Quantitative measurements of various aspects of the system at specific points in time.
   - Helps in understanding the health and performance of the system through aggregation.

3. **Traces**:

   - Logs related to a single transaction or request as it travels through various services.
   - Important for performance monitoring and debugging in distributed systems.

4. **Profiles**:
   - Information regarding the computing power and resources consumed by an application, typically gathered over time to identify inefficiencies.

## Databases for Telemetry Signals

- **Logs**: Handled by Grafana Loki, which allows for log aggregation and querying.
- **Metrics**: Handled by Prometheus and its scalable extension, Mimir, which collects time-series data for performance analysis.

- **Traces**: Managed by Tempo, which focuses on distributed tracing for better observability in microservices.

- **Profiles**: Collected by Pyroscope, which enables profiling to monitor resource usage.

## Instrumentation

Instrumentation refers to the methods used to collect telemetry data from applications, which can be done in several ways:

1. **Source Instrumentation**:

   - **Faro**: For frontend applications.
   - **OpenTelemetry**: A set of APIs and libraries for backend applications to collect telemetry data.

2. **Binary Instrumentation**:

   - **Alloy**: A tool used for instrumentation at the binary level, allowing for deeper insights into application behavior.

3. **External Instrumentation**:
   - **BEYLAF**: An external tool or method for instrumentation.

## Software Testing

- **k6**: A tool used for performance testing, allowing developers to simulate loads and test the scalability of applications.

## Visualization

- **Grafana Dashboard**: A powerful visualization tool that allows users to create dynamic and informative dashboards for monitoring metrics, logs, and traces collected from the various components of the stack.

## Incident Response

- **Oncall**: Refers to practices and systems in place for responding to incidents, typically involving a team that is available to handle alerts and resolve issues.
