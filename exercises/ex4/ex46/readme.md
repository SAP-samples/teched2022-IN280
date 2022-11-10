# Exercise 4.6 - Details on how to work with Cloud Integration metrics

In this exercise, we will ...

#### Prequisites:

- You have opened the *metric overview page* of a Cloud Integration service

## Exercise steps

Run through the steps in the given order.

1. *Click* on the card *Certificate Validity*

   <br>![](/exercises/ex4/images/HMMetricOverviewCertificateDetails.png)   
   
   A *Details page* opens showing all *Certificate Validity* metrics of the selected Cloud Integration service. By default the metrics are sorted by value and you oversee the certificates at the top that have to be updated most urgently
   
2. *Click* on one *info* icon to see the API result from pulling the Cloud Integration tenant

   <br>![](/exercises/ex4/images/HMMetricCertificateInfo.png)   
   
3. Inspect the queue issue and *click* on the card *JMS Queues Status* and examine which queue caused the rating

   From the left metric overview side you see that a queue is rated as *Critical* or *Fatal*. Also the card *JMS Queue Capacity* shows that the may queue capacity has been reached. 
      
   <br>![](/exercises/ex4/images/HMMetricQueueIssue.png)
   
   From the right metric details you get in the insight, that the queue `SFSF_EMPLOYEE_ERROR` has been stopped

4. *Click* on the tab *All Metrics*

   <br>![](/exercises/ex4/images/HMSwitchToAllMetrics.png)   

   See all metrics that are offered by Cloud Integration such as all *certificate validities* including the remaining days until their expiry. 

   <br>![](/exercises/ex4/images/HMCloudIntegrationMetrics.png)
   
   >
   > *Information*: As default, Cloud Integration tenants are pulled every 5 minutes using an OData APIs.
   > 

    As the list of metrics might be large the list can be sorted, filtered by a specific metric type or rating, or one can group the metrics by their labels

5. *Filter* for metrics in state *Critical*, *Fatal*, or *Warning*

   <br>![](/exercises/ex4/images/HMMetricsFilterData.png)   
   
6. Reset the filter again and *group* the list per certificate *Type* and additional search for *certificate* to exclude JMS queues

   <br>![](/exercises/ex4/images/HMMetricsGroupPerCertificateType.png)
   
   The certificate metric *CPI.Certificate.Expiry* has two different labels: 
   
   - *alias*: certificate name
   - *type*: certificate type (certificate, key pair) 
   
7. Click on the button *History* of the metric *JMS Qeueu Capacity*

   The graph shows how the metric has evolved in chronological development, to identify trends for the usage of resources, or to analyze when exactly a specific situation has happened. 

   It is possible to see the collected data of selected labels for the last 30 days. 

   Below you see the obvious behaviors of the certificate validity of all key pairs. Linear lines represent the number of remaining days until expiry. Directly within this popup you may filter on all labels available for the metric (alias and type for Certificate Validity).

## Summary

You've understood how to work with Cloud Integration metrics.

<br>Continue to - [Exercise 4.7 - Activate alerts](/exercises/ex4/ex47/)
