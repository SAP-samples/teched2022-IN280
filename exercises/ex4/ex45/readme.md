# Exercise 4.5 - Monitored metrics of Cloud Integration

In this exercise you will understand how to get an **overview of all metrics** that are monitored for a particular Cloud Integration service.

#### Prerequisites:

- You are in the *monitoring page* of all *Cloud Integration services* 

## Exercise steps

Run through the steps in the given order.

1. *Click* on any *Cloud Integration service* `CloudIntegration-TECHED-APJ01` and drill down one level 

    <br>![](/exercises/ex4/images/HMDrillDownToInstance.png)
    
    The **metric overview page** opens
    
    >
    > This **metric overview of a particular service** is the centerpiece of Health Monitoring and offers a quick health overview, in our case the selected *Cloud Integration service*. 
    >
    > The grouping of available metrics is pre-configured and depends on the service type and offered metrics. Cloud Integration offers as of today the status of **JMS queue resources** and the **validity of certificates**. The default thresholds are the same as you know them from the local Cloud Integration monitoring. The blog [Centralized health monitoring of SAP Cloud Integration using SAP Cloud ALM](https://blogs.sap.com/2022/02/07/centralized-health-monitoring-of-sap-cloud-integration-using-sap-cloud-alm/) explains in detail all metrics that are available in Health Monitoring for Cloud Integration.
    >
    > By means of **rating colors** it is easy to track all monitored metrics briefly. Any rating in red or orange attracts attention and likely will be examined more closely.
    > 
    > In the lower section, one can also see also tiles for each JMS queue, titled by their label. They have own metrics and are visualized as separately: *activation status*, *queue status*, and the *number of messages*
    >
    
    <br>![](/exercises/ex4/images/HMMetricOverview.png)
        
    For the selected Cloud Integration service `CloudIntegration-TECHED-APJ01` you see that a certificate is in state *Warning* and soon expiring. And the JMS resources have to be examined. The queue `SFSF_EMPLOYEE_ERROR` has been stopped with 6 messages in the queue. 2 of 10 queues aren't in state *Ok* and it looks like the total queue capacity is getting exhausted.
    
## Summary

Now you understand how to get an **overview on all metrics** that are monitored for a particular Cloud Integration service.

<br>Continue to - [Exercise 4.6 - Details on metric page](/exercises/ex4/ex46/)

