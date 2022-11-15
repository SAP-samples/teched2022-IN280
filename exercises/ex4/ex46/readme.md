# Exercise 4.6 - Details on metric page

In this exercise, we will get an understanding how to work with the *metrics page*. You oversee resources of *Cloud Integration* at a glance and exhausted resources get attention quickly.

#### Prerequisites:

- You have opened the *metric overview page* of a Cloud Integration service

## Exercise steps

Run through the steps in the given order

1. *Click* on the *metric card* **Certificate Validity**

   <br>![](/exercises/ex4/images/HMMetricOverviewCertificateDetails.png)   
   
   A **Details page** opens that is showing all *Certificate Validity* metrics of the selected Cloud Integration service. By default the metrics are sorted by value and you oversee those certificates at the top that have to be updated most urgently
   
2. *Click* on one *info* icon to see the **API result** that has been polled from the *Cloud Integration tenant*

   <br>![](/exercises/ex4/images/HMMetricCertificateInfo.png)   
   
3. Now inspect the queue issue and *click* on the *metric card* **JMS Queues Status** and examine which queues have caused the rating

    <br>![](/exercises/ex4/images/HMMetricQueueIssue.png)
   
    From the left metric overview side you see that queues are .  In the list you see, that the queue `SFSF_EMPLOYEE_ERROR` has been stopped and therefore rated as *Error*. The queue `CX_SRVORDER_ASYNC` is in state *Critical*

4. *Close* the details page by the *plus* icon **(+)** and *click* on the tab **All Metrics**

   <br>![](/exercises/ex4/images/HMSwitchToAllMetrics.png)   

   In the **All Metrics page** all metrics that are offered by Cloud Integration are listed 

   <br>![](/exercises/ex4/images/HMCIMetrics.png)
   
   >
   > Different metric types exist such as *Quota*, *Status* or *Performance* 
   >
   > Some metrics have only informative character and are not counted during rating calculation (see [Calculation of a service's health rating](/exercises/ex4/ex44))
   >
   
    As the list of metrics might be large the list can be sorted, filtered by a specific metric type or rating, or one can group the metrics by their labels
    
    *The following steps are **optional** and only for your information.* You may jump directly to [Exercise 4.7](/exercises/ex4/ex47/)
5. **Filter** for metrics in state *Critical*, *Fatal*, or *Warning*

   <br>![](/exercises/ex4/images/HMMetricsFilterData.png)   
   
6. *Reset* the filter again in the *filter dialog* and **group** the list per certificate **Type** and additional **search** for **certificate** to exclude JMS queues

   <br>![](/exercises/ex4/images/HMMetricsGroupPerCertificateType.png)
   
   You see that the certificate metric *CPI.Certificate.Expiry* has **two different labels**:
   
   - *alias*: certificate name
   - *type*: certificate type (certificate, key pair) 
   
7. Go back to the ... page, select the    service and *click* on the button **History** of the metric **JMS Queue Capacity**

    >
    > The graph shows how the metric has evolved in chronological development, to identify trends for the usage of resources, or to analyze when exactly a specific situation has happened. 
    > 
    > It is possible to see the collected data of selected labels for the last 30 days. 
    >

    <br>![](/exercises/ex4/images/HMMetricCapacityHistory.png)
    
    The queues on this tenant have been prepared Nov 8th, 2022. Therefore you will see a hop that day. *Find* the hop using the *picker*
    
     :heavy_exclamation_mark: **It is not possible to resolve any issue in SAP Cloud ALM. For the issue resolution you have to use SAP Integration Suite!**
    
## Summary

You've understood how to work with Cloud Integration metrics. You can get into the details of each metric and see also the chronological development for trend analysis.

<br>Continue to - [Exercise 4.7 - Activate alerts](/exercises/ex4/ex47/)
