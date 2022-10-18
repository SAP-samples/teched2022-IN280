# Details on how to work with Cloud Integration metrics

In this exercise, we will ...

#### Prequisites:

- You have opened the *metric overview page* of the Cloud Integration service that you registered.
<br>

## Exercise steps

Run through the exercise steps in the given order.

1. *Click* on the tab *All Metrics*

   <br>![](/exercises/ex4/images/HMSwitchToAllMetrics.png)   

   See all metrics that are offered by Cloud Integration such as all *certificate validities* including the remaining days until their expiry. 

   <br>![](/exercises/ex4/images/HMCloudIntegrationMetrics.png)
   
   >
   > *Information*: As default, Cloud Integration tenants are pulled every 5 minutes using the OData APIs.
   > 

2. Filtering, sorting, and group metrics

   As the list of metrics might be large the list can be sorted, filtered by a specific metric type or rating, or one can group the metrics by their labels. In the screenshot below one can see all metrics of type ‘Certificate validity’ grouped by the label ‘type’ (certificate, key pair).
   
   a. Filter for metrics in *Critical*, *Fatal*, or *Warning* state
   
   <br>![](/exercises/ex4/images/HMMetricsFilterData.png)   
   
   Reset the filter again.
   
   b. 
   
   c. Group the list per certificate *Type* and additional search for *certificate* to exclude JMS queues

   <br>![](/exercises/ex4/images/HMMetricsGroupPerCertificateType.png)
   
   The certificate metric *CPI.Certificate.Expiry* has two different labels: ===the *alias* is the certificate name, and *type* is the certificate type ....===Link to docu===

3. Click on the button *History* of the metric ???? 

   The graph shows how the metric has evolved in chronological development, to identify trends for the usage of resources, or to analyze when exactly a specific situation has happened. 

   It is possible to see the collected data of selected labels for the last 30 days. 

   Below you see the obvious behaviors of the certificate validity of all key pairs. Linear lines represent the number of remaining days until expiry. Directly within this popup you may filter on all labels available for the metric (alias and type for Certificate Validity).

   
## Summary

You've now ...

Next we will ....... Continue to - [Exercise 5](../ex5/README.md)





<!--
# Available metrics for Cloud Integration

In this exercise, we will ...

## Exercise steps

Run through the exercise steps in the given order.

#### Prequisites:
The Cloud Integration tenant is already registered. If not please run through exercises [Register a Cloud Integration tenant in LMS](../ex11/).

If not already done, please login to [SAP Cloud ALM tenant](https://teched22-cloudalm-003.authentication.eu10.hana.ondemand.com/).  

1.	Navigate t...

   <br>![](/exercises/ex4/images/CALMLandingHealthMon.png)
   
    >
    > *Important:*
    > Health monitoring do.....
    >

## Summary

You've now ...
After completing these steps you will have created...

Next we will ....... Continue to - [Exercise 5](../ex5/README.md)


2.	Insert this line of code.
```abap
response->set_text( |Hello ABAP World! | ). 
```

-->
