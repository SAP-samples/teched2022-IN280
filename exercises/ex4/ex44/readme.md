# Exercise 4.4 - Check alerts in Health Monitoring

In this exercise, we will ...
Health Monitoring comes with embedded alerting leveraged for various ALM use cases as for *Health Monitoring* or for *Integration & Exception Monitoring*.

#### Prerequisites:
- You are logged in to [SAP Cloud ALM](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home) and navigated to [*Health Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=sap.crun.hmapp.ui)
- *If you are performing configurations yourself*, your Cloud Integration service in SAP Cloud ALM `CloudIntegration-<tenant_name>_<userID>`  should be connected to the Cloud Integration tenant

## Exercise steps

Run through the exercise steps in the given order

1. *If you are performing configurations yourself:* in the [Exercise 4.5 - Activate alerts](../ex45/readme.md) you activate events for the Cloud Integration service that you have registered
      
    If you are using the *preconfigured Cloud Integration service* in SAP Cloud ALM `CloudIntegration-<tenant_name>` the alerting is already activated and nothing has to be done. The step can be skipped

2. *Navigate* to the *Alerting* section using the *exclamation mark* icon in the left-navigation

    <br>![](/exercises/ex4/images/HMAlerting.png)

    In the *Alerting* page one alert per registered cloud service and since the last data collection is listed. 
    
    >
    > *Note:* for the TechEd session we are not in a real environment. As attendees have registered own Cloud Integration services in SAP Cloud ALM connected you will find the same kind of alerts several times for a particular Cloud Integration tenant.
    >
    > Every 5 minutes SAP Integration Suite is pulled for monitoring data. Therefore you might have to wait until the next data collection until your activated alert get listed in the alerting section
    >

3. Use the *Filter* icon the right side to filter for alerts *JMS Queue Capacity* 

    *Enter* `JMS Queue Capacity` in field *Alert Name* and *apply* for the filter
    
    <br>![](/exercises/ex4/images/HMAlertingFilterCapacity.png)
    
    >
    > As the resulting list may be long you may have to use the browser search to squeeze down the list and see the relevant Cloud Integration service. The service is listed in column *Managed Components*. 
    > In real environments this kind of browser search isn't necessary.
    >

4. *Click* on the alert *JMS Queue Capacity* 

    <br>![](/exercises/ex4/images/HMAlertingCapacity.png)

    The **alert details page** opens for the selected alert. In the screenshot the total queue capacity of the tracked Cloud Integration tenant exceeds the max queue capacity. .........
    Under *Rating* you see how the rating or has changed over time. In case of the metric *JMS Queue Capacity* you see that the situation regarding total number of messages in JMS queues has been improved. You may also loop in to figure out, when the status has been changed.
    
    Under *Messages* you find single alerts. 
    
5. *Click* on the *information* icon (i) of a single alert to get the data pulled from the Cloud Integration capability of SAP Integration Suite


    
    , all raised messages (single alerts), operation automation logs, and *ServiceNow* tickets

    <br>![](/exercises/ex4/images/HMAlertingCapacityInfo.png)

6. *Click* on the *history* icon on the right of a single alert

    <br>![](/exercises/ex4/images/HMAlertingCapacityHistory.png)
    
    You may adapt the time frame to zoom in the history curve for further investigations
    
7. Click on *Actions* and then on *Processor* and *Assign*

    It is not necessary to assign someone

    >
    > A reported alert can be treated as a ticket. Somebody can work on it or hand it over to someone else for collaboration.
    > 
    > It is also possible to add useful comments or to start an operation flow. These actions are not part of the exercise.
    > 
    
    <br>![](/exercises/ex4/images/HMAlertingAssignProcessor.png)
    
8. *Optional*: 

    - [Add your email address to SAP Cloud ALM](/exercises/ex4/ex47/)

        If you want to assign a colleagues to an alert you have to use a verified email address. As the email addresses we are using in this TechEd session `userID@opensapusers.com` are not valid you have to add your email address in the separate *Notification Management* application.

        <br>![](/exercises/ex4/images/HMAlertingActions.png)

    - Afer adding yourself as a new recipient you can assign yourself as a processor for the alert. *Save* the assignment.

        <br>![](/exercises/ex4/images/HMAlertingCapacityAssignProcessor.png)
        
9. *Close* the alert *JMS Queue Capacity* by using the *cross* icon. *Filter* now for all alerts called *Expired Certificates* 

    *Enter* `Expired Certificates` in field *Alert Name* and *apply* for the filter
    
    <br>![](/exercises/ex4/images/HMAlertingCertifcates.png)
    
    
10. *Click* on the alert *Expired Certificate* for the Cloud Integration tenant `CloudIntegration-TECHED-EU01`

    This tenant is prepared this way that 3 certificates are expired already and another will expire soon.
    
    You can see the alert details in *full screen modus* by clicking in the middle on the right side

    <br>![](/exercises/ex4/images/HMAlertingRatingOverTime.png)

    > 
    > Alerts originating from *Health Monitoring* are based on the **rating of the related metric**. In the *Alert Details page* the active alerts since the last data collection are displayed with their properties. Cloud Integration is actively pulled every 5 minutes and therefore you might get alerts in this frequency. An alert is active, if one of the metric’s entries (labels) is in a *Warning* or *Critical* state. All alerts related to the same metric and service instance are aggregated to avoid overwhelming the alert inbox.
    >    

11. *Filter* now for all alerts on *JMS Queue Status* 

    - *Enter* `JMS Queue Status` in field *Alert Name* and *apply* for the filter 

        You can see that you may get several alerts depending on the queue
        
        
    - *Click* on the alert *JMS Queue Status*  for the Cloud Integration tenant `CloudIntegration-TECHED-US01` and the queue `SFSF_EMPLOYEE_ERROR`

        <br>![](/exercises/ex4/images/HMAlertingRatingOverTime.png)

        In the description of the single alert you can recognize that a JMS queue has been stopped.
    
    - *Click* on the alert *JMS Queue Status*  for the Cloud Integration tenant `CloudIntegration-TECHED-US01` and the queue `CX_SRVORDER_ASYNC`

        <br>![](/exercises/ex4/images/HMAlertingRatingOverTime.png)

        This queue is in *Warning* state because the resources are getting exhauted.
        
    >
    > In the local monitoring of Cloud Integration you may be able to resolve the issue
    > 
    
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

   <br>![](/exercises/ex1/images/CALMLandingHealthMon.png)
   
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
