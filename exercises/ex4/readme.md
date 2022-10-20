# Exercise 4 - Analyze Cloud Integration resources

In this exercise, we will work with the *Health Monitoring* use case of SAP Cloud ALM and track resources of Cloud Integration as the JMS queues and certificates. 

#### Prequisites:
- You are logged in to the [SAP Cloud ALM tenant](https://teched22-cloudalm-003.authentication.eu10.hana.ondemand.com/).  
- Your Cloud Integration service is already registered. If not please run through exercise [Register a Cloud Integration service in LMS](../ex1/ex11/readme.md).

## Exercise steps

Run through the exercise steps in the given order.

1.	Navigate to section *SAP Cloud ALM for Operation* and click on the card *Health Monitoring*.

      <br>![](/exercises/ex4/images/CALMLandingHealthMon.png)

2. Look over the **Health Monitoring overview page** 

   This central view shows the healthiness of connected services on the level of service types, e.g. all Cloud Integration tenants. It offers a first indicator where crucial changes and adjustments are necessary. 
   
   <br>![](/exercises/ex4/images/HMDrillDownToType.png)

3. Click on the card *SAP Integration Suite (Cloud Integration)* to drill one level down to the **service type monitoring page** 

   The *monitoring page* offers an overview on all registered Cloud Integration services along with number of raised alerts, the tenant health rating, and the information on data quality. If alerts exist for an instance you may jump directly to the embedded alert inbox.

   <br>![](/exercises/ex4/images/HMDrillDownToInstance.png)

   The selected Cloud Integration service has a **health percentage** of 92% and the service is rated as *Critical*.
   
   *Recommended but optional*: [Understand how the health rating of a service is calculated](./ex41/)

4.	Click on the service instance you have created in exercise [Register a Cloud Integration service in LMS](../ex1/ex11/readme.md) and drill one level down to the **metric overview of a Cloud Integration service**

      >
      > This page is the centerpiece of Health Monitoring and offers a quick health overview for a particular service, in our case a Cloud Integration tenant. The grouping of available metrics is pre-configured and depends on the service type and offered metrics. Cloud Integration offers as of today the status of **JMS queue resources** and the **validity of certificates**. The thresholds are the same as you know them from the local Cloud Integration monitoring. The blog [Centralized health monitoring of SAP Cloud Integration using SAP Cloud ALM](https://blogs.sap.com/2022/02/07/centralized-health-monitoring-of-sap-cloud-integration-using-sap-cloud-alm/) explains in detail all metrics that are available for Cloud Integration.
       >  
    
      <br>![](/exercises/ex4/images/HMMetricOverview.png)

      By means of **rating colors** it is easy to track all monitored metrics briefly. Any rating in red or orange attracts attention and likely will be examined more closely.

      For identification purposes of various metrics of the same type **labels** has been introduced: 

      - Each JMS queue has a label 'queue* for its name. 
      - Certificates have the labels *alias* and *type* for the differentiation between a certificate and a key pair.

      In the lower section, one can also see also tiles for each JMS queue, titled with their label. They have their own metrics such as its *activation*, the *status*, and the *number of messages*, therefore they are visualized as separate tiles.

4. Check alerts under **Alerting**

      Health Monitoring comes with embedded alerting leveraged for various ALM use cases as for *Health Monitoring* or for *Integration & Exception Monitoring*. 

      a. Activate alerts

      In the exercise [Activate alerts](../ex45/readme.md) you have to activate all possible events for the Cloud Integration service that you have registered.

      b. Go to ***Alerting*** using the left-navigation

      <br>![](/exercises/ex4/images/HMAlerting.png)

      In the *Alerting* page one alert per cloud service since the last data collection is listed.

      c. Click on on the alert *JMS Queue Capacity* 

      The *alert details page* opens for the selected alert. In the screenshot the total queue capacity of the tracked Cloud Integration tenant exceeds the max queue capacity. .........
      You see the rating, all raised messages (single alerts), operation automation logs, and *ServiceNow* tickets

      <br>![](/exercises/ex4/images/HMAlertingCapacity.png)

      d. Click on *Actions* and then on *Processor* and *Assign*

      >
      > A reported alert can be treated as a ticket. Somebody can work on it or hand it over to someone else to collaboratively work on it, add useful comments, or start an operation flow. 
      >
      | ==Check how we can do this== |


      Assign a processor who should care for the issue that has occured ....

      <br>![](/exercises/ex4/images/HMAlertingActions.png)

      e. In *Notification Management* add email recipient, send invitation for email verification, you have ot give your consent, afterwards assign processor

      Message in your browser shows up: *You are subscribed to SAP Cloud ALM notifications.*

      Back in alert inbox you can assign processor for an alert.

      Save

      f. Click on Expired Certificates

      This alert is rated as *Ok*

      <br>![](/exercises/ex4/images/HMAlertingRatingOverTime.png)

      > 
      > Alerts originating from *Health Monitoring* are based on the **rating of the related metric**. In the *Alert Details page* the active alerts since the last data collection are displayed with their properties. Cloud Integration is actively pulled every 5 minutes and therefore you might get alerts in this frequency. An alert is active, if one of the metric’s entries (labels) is in a *Warning* or *Critical* state. All alerts related to the same metric and service instance are aggregated to avoid overwhelming the alert inbox.
      >    

      g. You may also send notification to email recipients after activation and adding at least one recipient in the configuration of a service.

      h. Operations Flow and ServiceNow

5. Customize thresholds

   a. Edit metric configuration
   
   Set threshold for cloud services, either for all metrics of a cloud service in the clouser service overview or for specific metrics after selecting the correpoind service
   
   With treshold active you can override the metric rating reported by the service by creating custom rules. Seleect the metric you want to configure
   
>
> *Important*: Health monitoring does not offer any tools to update certificates or queues directly. This is only possible in the *keystore monitor* or *manage stores monitor* of Cloud Integration itself. 
>
> With *SAP Cloud ALM* one can get an overview of the health rating of all monitored Cloud Integration services at a glance or even all connected services and systems of your IT landscape. Operation teams benefit from this overview and can concentrate their efforts on the most important tasks and do not have to inspect all local monitoring tools. And they have the possibility to navigate from the health monitoring application to the Cloud Integration monitoring.
>
   
## Summary

You've now seen that Cloud Integration can be pulled for some metrics such as JMS resources and certificates to track them. Alerts and email notifications can be activated. Once a default or custom threshold is reached the activated reaction is triggered. 


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

