# Exercise 4.8 - Check alerts in Health Monitoring

Health Monitoring comes with embedded alerting leveraged for various ALM use cases as for *Health Monitoring* or for *Integration & Exception Monitoring*. In this exercise you will check raised alerts in the alerting section of *Health Monitoring*

#### Prerequisites:
- You are in [*Health Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=sap.crun.hmapp.ui)
- :construction_worker: *If you have a self-managed `CloudIntegration-<tenant_name>-<userID>` service*: alerts should be **activated**

## Exercise steps

Run through the exercise steps in the given order

1. *Navigate* to the *Alerting* section using the *exclamation mark* icon in the left-navigation

    <br>![](/exercises/ex4/images/HMAlerting.png)
    
    >
    > In the *Alerting* page one alert per registered cloud service and since the last data collection is listed. 
    >
    > Every 5 minutes SAP Integration Suite is pulled for monitoring data. Therefore you might have to wait until the next data collection until your activated alert get listed in the alerting section
    >
:exclamation_mark:  :heavy_exclamation_mark:
*Note:* for the TechEd session we are not in a real environment. As attendees have registered additional *Cloud Integration services* all connected to the same *Cloud Integration tenant* you will find the same kind of alerts several times
    

2. If you have several services in your scope, use the *Filter* icon the right side to filter for alerts *JMS Queue Capacity* 

    *Enter* `JMS Queue Capacity` in field *Alert Name* and *apply* for the filter
    
    <br>![](/exercises/ex4/images/HMAlertingFilterCapacity.png)
    
    >
    > As the resulting list still may be long because of the number of services you have in scope you may have to use the browser search to squeeze down the list and see the relevant Cloud Integration service. The service is listed in column *Managed Components*. 
    > In real environments this kind of browser search isn't necessary.
    >

3. *Click* on the alert *JMS Queue Capacity* 

    <br>![](/exercises/ex4/images/HMAlertingCapacity.png)

    The **alert details page** opens for the selected alert. In the screenshot the total queue capacity of the tracked Cloud Integration tenant exceeds the max queue capacity. The worst rating has been *Critical* but currently it is *Ok* again.
    Under *Rating* you see  again this behavior but also how the rating  has changed over time. You see that the situation regarding total number of messages in JMS queues has been improved. You may also zoom in to figure out, when the status has been changed.
    
    Under *Messages* you find single alerts. 
    
4. *Click* on the *information* icon (i) of a single alert to get the data pulled from the Cloud Integration capability of SAP Integration Suite
    
    , all raised messages (single alerts), operation automation logs, and *ServiceNow* tickets

    <br>![](/exercises/ex4/images/HMAlertingCapacityInfo.png)

5. *Click* on the *history* icon on the right of a single alert

    <br>![](/exercises/ex4/images/HMAlertingCapacityHistory.png)
    
    You may adapt the time frame to zoom in the history curve for further investigations
    
6. Click on *Actions* and then on *Processor* and *Assign*

    It is not necessary to assign someone

    >
    > A reported alert can be treated as a ticket. Somebody can work on it or hand it over to someone else for collaboration.
    > 
    > It is also possible to add useful comments or to start an operation flow. These actions are not part of the exercise.
    > 
    
    <br>![](/exercises/ex4/images/HMAlertingAssignProcessor.png)
    
7. *Optional*: If you have added your email address to SAP Cloud ALM in [Exercise 2.3](/exercises/ex2/ex23/) you may assign yourself as a processor for the alert. 

    <br>![](/exercises/ex4/images/HMAlertingCapacityAssignProcessor.png)

    *Save* the assignment.
        
8. *Close* the alert *JMS Queue Capacity* by using the *cross* icon. *Filter* now for all alerts called *Expired Certificates* 

    *Enter* `Expired Certificates` in field *Alert Name* and *apply* for the filter
    
    <br>![](/exercises/ex4/images/HMAlertingCertifcates.png)
    
    
9. *Click* on the alert *Expired Certificate* for the Cloud Integration tenant `CloudIntegration-TECHED-EU01`

    This tenant is prepared this way that 3 certificates are expired already and another will expire soon.
    
    You can see the alert details in *full screen modus* by clicking in the middle on the right side

    <br>![](/exercises/ex4/images/HMAlertingRatingOverTime.png)

    > 
    > Alerts originating from *Health Monitoring* are based on the **rating of the related metric**. In the *Alert Details page* the active alerts since the last data collection are displayed with their properties. Cloud Integration is actively pulled every 5 minutes and therefore you might get alerts in this frequency. An alert is active, if one of the metric’s entries (labels) is in a *Warning* or *Critical* state. All alerts related to the same metric and service instance are aggregated to avoid overwhelming the alert inbox.
    >    

10. *Filter* now for all alerts on *JMS Queue Status* 

    - *Enter* `JMS Queue Status` in field *Alert Name* and *apply* for the filter 

        You can see that you may get several alerts depending on the queue
        
        
    - *Click* on the alert *JMS Queue Status*  for the Cloud Integration tenant `CloudIntegration-TECHED-US01` and the queue `SFSF_EMPLOYEE_ERROR`

        <br>![](/exercises/ex4/images/HMAlertingRatingOverTime.png)

        In the description of the single alert you can recognize that a JMS queue has been stopped.
    
    - *Click* on the alert *JMS Queue Status*  for the Cloud Integration tenant `CloudIntegration-TECHED-US01` and the queue `CX_SRVORDER_ASYNC`

        <br>![](/exercises/ex4/images/HMAlertingRatingOverTime.png)

        This queue is in *Warning* state because the resources are getting exhausted.
        
    >
    > In the local monitoring of Cloud Integration you may be able to resolve the issue
    > 
    
## Summary

You've now learned how to work with the alerts in the alerting section. 

Congratulation. You have finalized all exercises. Go back to the main page - [IN280 - Central monitoring of integration scenarios using SAP Cloud ALM](../../../)
