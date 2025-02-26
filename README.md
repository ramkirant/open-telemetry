# Opentelemetry

OpenTelemetry is an observability framework for cloud-native software. It is a collection of tools, APIs and SDKs which we can use to instrument, generate, collect and export teletry data (metrics, logs and traces) for analysis to understand our software's performance and behavior. 

OpenTelemetry facilitates a way to measure the performance of everything we use in our application remotely. 

OpenTelemetry is a standardization for describing what distributed systems are doing no matter what programming language or computer systems we are using. By standardizing the data, we are not tied to anything and in the long run, it makes easy to move from one analysis tool to another. It will not also not impact the historical data.

## Observability

Observability means how well we can understand what is going on internally in a system based on its outputs. It is hard to see what is going on inside our applications especially when the applications are big and complex. 

### M.E.L.T

M.E.L.T stands for Metrics, Events, Logs and Traces.

Metrics are measurements collected at regular intervals and they must have a timestamp, a name, one or more numeric values and a count of how many events are represented. These include error rate, respone time or output. 

Event is a descrete action happening at any moment in time.

Logs come directly out of our application exporting detailed data and detailed context around an event. 

Traces follow a request from the initial request to the returned output. Traces are very valuable in highlighting inefficiencies, bottlenecks and roadblocks in the user experience. 

## OpenTelemetry Architecture and Components

The architecture of OpenTelemetry consists of several core components, each playing a crucial role in the collection, processing and exporting of telemetry data. 

![image](https://github.com/user-attachments/assets/1fd79499-9224-4895-b4f0-3fdf115a5161)

### APIs

The OpenTelemetry APIs are language specific interfaces that allows us to instrument our code to collect the telemetry data. They are designed to be light weight and efficient with minimal impact on the application performance. 

### SDK

OpenTelemetry SDK is a set of tools that implement the OpenTelemetry APIs. It provides functionality to collect, process and export telemetry data from our services. The SDK includes features like batching, retry, and throttling to ensure efficient data collection. It also inclues a configuration system that allows us to control how the data is collected and exported. 

### Collector

The OpenTelemetry Collector is a service that receive, process and export telemetry data. It provides a unified way to ingest and export data, making it easier to integrate OpenTelemetry with your existing infrastructure. The collector can be deployed as a standalone service or a sidecar, depending on your needs. It is designed to be scalable and reiable, ensuring that your telemetry data is safely and efficiently handled. 

### Receiver

A Receiver is a component that receives telemetry data from your services. Receivers can handle different types of data, including traces, metrics and logs. Receivers are responsible for accepting data, transforming it and passing it on to processors. They are the entry point for data into the OpenTelemetry system. 

### Difference between OpenTelemetry Collector and Receiver

OpenTelemetry Collector is a central hub that receives, processes and exports the data. While Receiver is primarily responsible for the initial ingestion Essentially, receiver is a component of collector which receives the data from various sources. 

### Processor

Processor takes data from Receivers and processes it before sending it to exporters. They can perform a variety of tasks such as batching, filtering and enriching the data. 

### Exporter

Exporter takes the processed data from processors and export it to a backend of your choice. This could be a database, a monitoring service, or any other system where you want to store and analyze your telemetry data. Exporters are designed to be flexible and extensible, allowing us to integrate OpenTelemetry with various banckends and analysis tools. 
