# Metrics collection
Read full article [here](https://www.datadoghq.com/blog/monitoring-101-collecting-data/)

Metrics collection is a process to capture values related to the condition and performance of your system on a specific point of time, for example the number of request since the last 1 minute and the number of currently logged in users.

## Metrics are usually collected once per second, one per minute, or at another regular interval to monitor a system over time.

There are 3 kinds of metrics to be collected :
## Work metrics
Work metrics indicate the top-level health of your system by measuring its useful output. When considering your work metrics, it’s often helpful to break them down into four subtypes:
1. **Throughput** 
Is the amount of work the system is doing per unit time. Throughput is usually recorded as an absolute number.
2. **Success** 
Metrics represent the percentage of work that was executed successfully.
3. **Error** 
Metrics capture the number of erroneous results, usually expressed as a rate of errors per unit time or normalized by the throughput to yield errors per unit of work. Error metrics are often captured separately from success metrics when there are several potential sources of error, some of which are more serious or actionable than others.
4. **Performance**
Metrics quantify how efficiently a component is doing its work. The most common performance metric is latency, which represents the time required to complete a unit of work. Latency can be expressed as an average or as a percentile, such as “99% of requests returned within 0.1s”.

## Resource metrics
Most components of your software infrastructure serve as a resource to other systems. Some resources are low-level—for instance, a server’s resources include such physical components as CPU, memory, disks, and network interfaces. But a higher-level component, such as a database or a geolocation microservice, can also be considered a resource if another system requires that component to produce work.

Resource metrics can help you reconstruct a detailed picture of a system’s state, making them especially valuable for investigation and diagnosis of problems. For each resource in your system, try to collect metrics that cover four key areas:
1. **Utilization**
Is the percentage of time that the resource is busy, or the percentage of the resource’s capacity that is in use.
2. **Saturation** 
Is a measure of the amount of requested work that the resource cannot yet service, often queued.
3. **Errors**
Represent internal errors that may not be observable in the work the resource produces.
4. **Availability**
Represents the percentage of time that the resource responded to requests. This metric is only well-defined for resources that can be actively and regularly checked for availability.

## Events
In addition to metrics, which are collected more or less continuously, some monitoring systems can also capture events: discrete, infrequent occurrences that can provide crucial context for understanding what changed in your system’s behavior. Some examples:

1. **Changes**: Internal code releases, builds, and build failures
2. **Alerts**: Internally generated alerts or third-party notifications
3. **Scaling events**: Adding or subtracting hosts
