# Exercise 4.8 - Check alerts in Health Monitoring

Health Monitoring comes with embedded alerting leveraged for various ALM use cases as for *Health Monitoring* or for *Integration & Exception Monitoring*. In this exercise you will check raised alerts in the alerting section of *Health Monitoring*

#### Prerequisites:
- You are in [*Health Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=sap.crun.hmapp.ui)
- :construction_worker: *If you have a self-managed `CloudIntegration-<tenant_name>-<userID>` service*: alerts should be **activated**

## Exercise steps

Run through the exercise steps in the given order

1. *Navigate* to the **Alerting** section using 

    a. either the **Alert** link in the footer of the *SAP Integration Suite** card
    
    <br>![](/exercises/ex4/images/HMOverviewpageMoveToAlerts.png)
    
    b. or the *exclamation mark* icon **(!)** in the left-navigation

    <br>![](/exercises/ex4/images/HMAlerting.png)
    
    >
    > In the *Alerting* page one alert per registered cloud service and since the last data collection is listed. 
    >
    > Every 5 minutes SAP Integration Suite is pulled for monitoring data. Therefore you might have to wait until the next data collection until your activated alert get listed in the alerting section
    >

 

2. **Filter** for alerts **JMS Queue Capacity** with the *filter* icon the right side

    *Enter* `JMS Queue Capacity` in field *Alert Name* and *apply* for the filter
    
    <br>![](/exercises/ex4/images/HMAlertingFilterCapacity.png)
    
     As the resulting list still may be long because of the number of services you have in scope. If this is the case you may have to use the *browser search* to squeeze down the list and see the relevant Cloud Integration service. The service is listed in column *Managed Components*. 
    In real environments this kind of browser search isn't necessary.
    
3. *Click* on the alert **JMS Queue Capacity** 

    <br>![](/exercises/ex4/images/HMAlertingCapacity.png)

    > 
    > Alerts originating from *Health Monitoring* are based on the **rating of the related metric**. In the *Alert Details page* the active alerts since the last data collection are displayed with their properties. An alert is active, if one of the metric’s entries (labels) is in a *Warning* or *Critical* state. All alerts related to the same metric and service instance are aggregated to avoid overwhelming the alert inbox.
    >    
    

    The **alert details page** opens for the *JMS Queue Capacity* alert. In the screenshot the total queue capacity of the tracked Cloud Integration tenant exceeds the max queue capacity. The worst rating has been *Critical* but currently it is *Ok* again.
    
    Under *Rating* you see  again this behavior but also how the rating  has changed over time. You see that the situation regarding total number of messages in JMS queues has been improved. You may also zoom in to figure out, when the status has been changed.

   
4. *Close* the alert  by using the *cross* icon **(X)**

5. *Filter* now for **Expired Certificates** alerts using the *filter* icon in the upper right corner (as done in step 2.)

6. *Click* on the alert for the service `CloudIntegration-TECHED-EU01`
    
    <br>![](/exercises/ex4/images/HMAlertingCertifcates.png)  


    This tenant is prepared in the way that 3 certificates are expired already and another will expire soon
    
    It is worth to mention that for *certificate alerts* you see multiple single alerts, one for each certificate that is not in state *Ok*. As the expiry status may change over time, the *wrost rating* might be *Critical* although in the meanwhile some certificates have been updated and the current state is in *Warning* 
    
7. *Filter* now for all alerts on **JMS Queue Status** 
      
    *Recognize* that different alerts have been raised depending on the queue
    
    - *Click* on one of the alerts with queue `SFSF_EMPLOYEE_ERROR` in column *Object Details*

        <br>![](/exercises/ex4/images/HMAlertingRatingOverTime.png)

        In the description of the single alert you can recognize that the JMS queue has been stopped.
    
    - *Click* on one of the alerts with queue `CX_SRVORDER_ASYNC` in column *Object Details*

        <br>![](/exercises/ex4/images/HMAlertingRatingOverTime.png)

        This queue is in *Warning* state because the resources are getting exhausted.
        

    
## Summary

You've now learned how to check raised alerts in the alerting section of *Health Monitoring*


Congratulation. You have finalized all exercises. Go back to the main page - [IN280 - Central monitoring of integration scenarios using SAP Cloud ALM](../../../README.md)
