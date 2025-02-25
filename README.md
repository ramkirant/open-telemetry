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
