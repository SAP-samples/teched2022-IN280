# Exercise 4.6 - Details on metric page

In this exercise, we will get an understanding how to work with the *metrics page*. You oversee resources of *Cloud Integration* at a glance and exhausted resources get attention quickly.

<br> :heavy_exclamation_mark: **It is not possible to resolve any issue in SAP Cloud ALM. For the issue resolution you have to use SAP Integration Suite!**  

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
   
    In the list you see, that the queue `SFSF_EMPLOYEE_ERROR` has been stopped and therefore rated as *Error*. The queue `CX_SRVORDER_ASYNC` is in state *Warning*

4. *Close* the details page by the *plus* icon **(X)** and *click* on the tab **All Metrics**

   <br>![](/exercises/ex4/images/HMSwitchToAllMetrics.png)   

   In the **All Metrics page** all metrics that are offered by Cloud Integration are listed 

   <br>![](/exercises/ex4/images/HMCIMetrics.png)
   
   >
   > Different metric types exist such as *Quota*, *Status* or *Performance* 
   >
   > Some metrics have only informative character and are not counted during rating calculation (see [Calculation of a service's health rating](/exercises/ex4/ex44))
   >
   
    As the list of metrics might be large the list can be sorted, filtered by a specific metric type or rating, or one can group the metrics by their labels
    
    *The following steps are **optional** and only for your information.* You may jump directly to [Exercise 4.7](/exercises/ex4/ex47/)<br>
    
5. **Filter** for metrics in state *Critical*, *Fatal*, or *Warning*

    <br>![](/exercises/ex4/images/HMMetricsFilterData.png)    
 
6. *Click* on the button **History** of the metric **JMS Queue Capacity**

    <br>![](/exercises/ex4/images/HMMetricClickHistoryCapacity.png)    
    
7. *Use* the **time picker** to find the best time interval in the curve to see when the queues filled up 

    <br>![](/exercises/ex4/images/HMMetricCapacityHistory.png)

    >
    > The graph shows how the metric has evolved in chronological development, to identify trends for the usage of resources, or to analyze when exactly a specific situation has happened. 
    > 
    > It is possible to see the collected data of selected labels for the last 30 days. 
    >

    The queues on this tenant `TECHED-APJ01`have been prepared Nov 15th, 2022, 5:00 - 5:40 pm.  
    

   
   
   
8. **Close** the dialog and **reset the filter** in the *filter dialog*

9. Now **group** the list per certificate **Type** and additional **search** for **certificate** to exclude JMS queues

   <br>![](/exercises/ex4/images/HMMetricsGroupPerCertificateType.png)
   
   You see that the certificate metric *CPI.Certificate.Expiry* has **two different labels**:
   
   - **alias**: certificate name
   - **type**: certificate type (certificate, key pair) 
   
 
    
## Summary

You've understood how to work with Cloud Integration metrics. You can get into the details of each metric and see also the chronological development for trend analysis.

<br>Continue to - [Exercise 4.7 - Activate alerts](/exercises/ex4/ex47/)
