# Exercise 4 - Analyze exhausted resources

In this exercise, we will create track resources of the Cloud Integration tenant as the JMS queues and certificates. 

#### Prequisites:
- You are logged in to the [SAP Cloud ALM tenant](https://teched22-cloudalm-003.authentication.eu10.hana.ondemand.com/).  
- The Cloud Integration tenant is already registered. If not please run through exercise [Register a Cloud Integration tenant in LMS](../ex1/ex11/readme.md).

## Exercise steps

Run through the exercise steps in the given order.

1.	Navigate to section *SAP Cloud ALM for Operation* and click on the card *Health Monitoring*.

   <br>![](/exercises/ex4/images/CALMLandingHealthMon.png)

2. Look over the **Health Monitoring overview page** 

   This central view shows the healthiness of connected services on the level of service types, e.g. all Cloud Integration tenants. It offers a first indicator where crucial changes and adjustments are necessary. 
   
   <br>![](/exercises/ex4/images/HMDrillDownToType.png)

3. Click on the card *SAP Integration Suite (Cloud Integration)* to drill one level down to the **service type monitoring page** 

      a. Perceive the service type monitoring page
      
      It offers an overview on all connected Cloud Integration tenants along with number of raised alerts, the tenant health rating, and the information on data quality. If alerts exist for an instance you may jump directly to the embedded alert inbox.
      
      <br>![](/exercises/ex4/images/HMDrillDownToInstance.png)

      b. *Recommended but optional*: [Understand metric ratings](./ex41/)
      
      The selected Cloud Integration tenant has a service health percentage of 92% and the service is rated as *Critical*.

4.	Click on the service instance you have created in exercise [Register a Cloud Integration tenant in LMS](../ex1/ex11/readme.md) and drill one level down to the **metric overview of a Cloud Integration tenant**

      
      This page is the centerpiece of Health Monitoring and offers a quick health overview for a particular tenant, in our case a Cloud Integration tenant. The grouping of available metrics is pre-configured and depends on the service type and offered metrics. Cloud Integration offers as of today the status of **JMS queue resources** and the **validity of certificates**. The thresholds are the same as you know them from the local Cloud Integration monitoring. The blog [Centralized health monitoring of SAP Cloud Integration using SAP Cloud ALM](https://blogs.sap.com/2022/02/07/centralized-health-monitoring-of-sap-cloud-integration-using-sap-cloud-alm/) explains in detail all metrics that are available for Cloud Integration.
       
      <br>![](/exercises/ex4/images/HMMetricOverview.png)
      
      By means of **rating colors** it is easy to track all monitored metrics briefly. Any rating in red on the page attracts attention and should be examined more closely.
      
      For identification purposes of various metrics of the same type **labels** has been introduced: 
      
      - Each JMS queue has a label 'queue* for its name. 
      - Certificates have the labels *alias* and *type* for the differentiation between a certificate and a key pair.
      
      In the lower section, one can also see also tiles for each JMS queue, titled with their label. They have their own metrics such as its *activation*, the *status*, and the *number of messages*, therefore they are visualized as separate tiles.

      a. Click on the tab *All Metrics*

      See all metrics that are offered by Cloud Integration such as all *certificate validities* including the remaining days until their expiry. 
      
      >
      > *Information*: As default, Cloud Integration tenants are pulled every 5 minutes using the OData APIs.
      > 

      b. Filtering and sorting possibilities
      
      As the list of metrics might be large the list can be sorted, filtered by a specific metric type or rating, or one can group the metrics by their labels. In the screenshot below one can see all metrics of type ‘Certificate validity’ grouped by the label ‘type’ (certificate, key pair).

      c. Click on the icon .... to open the *history graph* for a particular metric

      The graph shows how the metrics have evolved, to identify trends for the usage of resources, or to analyze when exactly a specific situation has happened. 
      
      It is possible to see the collected data of selected labels for the last 30 days. 
      
      Below you see the obvious behaviors of the certificate validity of all key pairs. Linear lines represent the number of remaining days until expiry. Directly within this popup you may filter on all labels available for the metric (alias and type for Certificate Validity).

>
>
> *Important*: Health monitoring does not offer any tools to update certificates or queues directly. This is only possible in the *keystore monitor* or *manage stores monitor* of Cloud Integration itself. 
>
> With *SAP Cloud ALM* one can get an overview of the health rating of all monitored Cloud Integration services at a glance or even all connected services and systems of your IT landscape. Operation teams benefit from this overview and can concentrate their efforts on the most important tasks and do not have to inspect all local monitoring tools. And they have the possibility to navigate from the health monitoring application to the Cloud Integration monitoring.
>
>

9. Alerts

      >
      > Health Monitoring comes with embedded alerting leveraged for various ALM use cases. A reported alert can be treated as a ticket. Somebody can work on it or hand it over to someone else to collaboratively work on it, add useful comments, or start an operation flow.
      >

   a) Activate alerts on metric level in configuration page
   
10. Customize thresholds


   
## Summary

You've now ...

Next we will ....... Continue to - [Exercise 5](../ex5/README.md)

<!--
## Exercise 2.1 Sub Exercise 1 Description

After completing these steps you will have created...

1. Click here.
<br>![](/exercises/ex2/images/02_01_0010.png)

2.	Insert this line of code.
```abap
response->set_text( |Hello ABAP World! | ). 
```

## Exercise 2.2 Sub Exercise 2 Description

After completing these steps you will have...

1.	Enter this code.
```abap
DATA(lt_params) = request->get_form_fields(  ).
READ TABLE lt_params REFERENCE INTO DATA(lr_params) WITH KEY name = 'cmd'.
  IF sy-subrc = 0.
    response->set_status( i_code = 200
                     i_reason = 'Everything is fine').
    RETURN.
  ENDIF.

```
-->

