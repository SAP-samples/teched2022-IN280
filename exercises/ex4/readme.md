# Exercise 4 - Analyze Cloud Integration resources

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

   It offers an overview on all connected Cloud Integration tenants along with number of raised alerts, the tenant health rating, and the information on data quality. If alerts exist for an instance you may jump directly to the embedded alert inbox.

   <br>![](/exercises/ex4/images/HMDrillDownToInstance.png)

   The selected Cloud Integration tenant has a service health percentage of 92% and the service is rated as *Critical*.
   
   *Recommended but optional*: [Understand how a tenant's health rating is calculated](./ex41/)

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

9. [Activate alerts](ex45/readme.md)

   Health Monitoring comes with embedded alerting leveraged for various ALM use cases as for Health Monitoring or for Integration & Exception Monitoring. 
   
   A reported alert can be treated as a ticket. Somebody can work on it or hand it over to someone else to collaboratively work on it, add useful comments, or start an operation flow.
   
   In the linked exercise you activate all metrics for the Cloud Integration service you have registered.
   
10. Check alerts in **alert inbox**

   a. Go to the alert inbox using the left-navigation

   <br>![](/exercises/ex4/images/HMAlerting.png)
   
   There is one entry per metric and cloud service is listed.
      
   b. Click on on the alert *JMS Queue Capacity* 
   
   The alert details page opens for the selected metric. The total queue capacity of the tracked Cloud Integration tenant tends to get exceeded the max queue capacity. .........
   You see the rating, all raised messages (single alerts), operation automation logs, and servicenow tickets
   
   PICTURE with CPI API result
   
   c. Click on *Actions* and then on *Processor* and *Assign*
   
   Several actions are possible on alerts. We assign a processor who should care for the issue that has occured.
   
   <br>![](/exercises/ex4/images/HMAlertingActions.png)
   
   d. In *Notification Management* add email recipient, send invitation for email verification, you have ot give your consent, afterwards assign processor
   
   Message in your browser shows up: *You are subscribed to SAP Cloud ALM notifications.*
   
   Back in alert inbox you can assign processor for an alert.
   
   Save
   
   e. Click on Expired Certificates
   
   This alert is rated as *Ok*
   
   <br>![](/exercises/ex4/images/HMAlertingRatingOverTime.png)
   
   > 
   > Alerts originating from *Health Monitoring* are based on the **rating of the related metric**. In the *Alert Details page* the active alerts since the last data collection are displayed with their properties. Cloud Integration is actively pulled every 5 minutes and therefore you might get alerts in this frequency. An alert is active, if one of the metric’s entries (labels) is in a *Warning* or *Critical* state. All alerts related to the same metric and service instance are aggregated to avoid overwhelming the alert inbox.
   >

   f. You may also send notification to email recipients after activation and adding at least one recipient in the configuration of a service.
   
   g. Operations Flow and ServiceNow

12. Customize thresholds

   a. Edit metric configuration
   
   Set threshold for cloud services, either for all metrics of a cloud service in the clouser service overview or for specific metrics after selecting the correpoind service
   
   With treshold active you can override the metric rating reported by the service by creating custom rules. Seleect the metric you want to configure
   
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

