# Check alerts in Health Monitoring

In this exercise, we will ...
Health Monitoring comes with embedded alerting leveraged for various ALM use cases as for *Health Monitoring* or for *Integration & Exception Monitoring*.

#### Prerequisites:
- You are logged in to [SAP Cloud ALM](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home) and navigated to [*Health Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=sap.crun.hmapp.ui)
- *If you are performing configurations yourself*, your Cloud Integration service in SAP Cloud ALM `CloudIntegration-<tenant_name>_<userID>`  should be connected to the Cloud Integration tenant
-  If you are using a *preconfigured Cloud Integration service* in SAP Cloud ALM nothing has to be done

## Exercise steps

Run through the exercise steps in the given order

1. *If you are performing configurations yourself:* in the [Exercise 4.5 - Activate alerts](../ex45/readme.md) you activate events for the Cloud Integration service that you have registered.
      
    If you are using the *preconfigured Cloud Integration service* in SAP Cloud ALM `CloudIntegration-<tenant_name>` the alerting is already activated and nothing has to be done. The step can be skipped.

2. *Navigate* to the *Alerting* section using the *exclamation mark* icon in the left-navigation

    <br>![](/exercises/ex4/images/HMAlerting.png)

    In the *Alerting* page one alert per registered cloud service and since the last data collection is listed. 
    
    >
    > *Note:* for the TechEd session we are not in a real environment. As attendees have registered own Cloud Integration services in SAP Cloud ALM connected to a particular real Cloud Integration tenant in SAP Integration Suite you will find same kind of alerts several times.
    >
    > Every 5 minutes SAP Integration Suite is pulled for monitoring data. Therefore you might have to wait until the next data collection yuntil your activated alert get listed in the alerting section
    >

3. *Filter* for alerts *JMS Queue Capacity* 

    *Enter* `Capacity`in field *Alert Name* and *apply* for the filter
    
    >
    > As the resulting list may be long you may have to use the brower search for looking for the relevant Cloud Integration service. The service is listed in column *Managed Components*. 
    > In real environments this kind of browser search isn't necessary.
    >

4. *Click* on on the alert *JMS Queue Capacity* 

    The **alert details page** opens for the selected alert. In the screenshot the total queue capacity of the tracked Cloud Integration tenant exceeds the max queue capacity. .........
    Under *Rating* you see how the rating or has changed over time. In case of the metric *JMS Queue Capacity* you see that the situation regarding total number of messages in JMS queues has been improved. You may also loop in to figure out, when the status has been changed.
    
    Under *Messages* you find single alerts. 
    
5. *Click* on the *information* icon (i) of a single alert to get the data pulled from the Cloud Integration capability of SAP Integration Suite

    <br>![](/exercises/ex4/images/HMAlertingCapacity.png)
    
    , all raised messages (single alerts), operation automation logs, and *ServiceNow* tickets

    <br>![](/exercises/ex4/images/HMAlertingCapacity.png)

6. *Click* on the *history* icon on the right of a single alert

    <br>![](/exercises/ex4/images/HMAlertingCapacity.png)
    
    You may adapt the time frame to zoom in the history curve for further investigations
    
7. Click on *Actions* and then on *Processor* and *Assign*

    >
    > A reported alert can be treated as a ticket. Somebody can work on it or hand it over to someone else to collaboratively work on it, add useful comments, or start an operation flow. 
    >
    
    <br>![](/exercises/ex4/images/HMAlertingCapacity.png)
    
8. *Optional*: [Add your email address to SAP Cloud ALM](/exercises/ex4/ex47/)

    If you want to assign a colleagues to an alert you have to use a verified email address. As the email addresses we are using in this TechEd session `userID@opensapusers.com` are not valid you have to add your email address. This is done in the separate *Notfication Management* application.

    <br>![](/exercises/ex4/images/HMAlertingActions.png)

    Back in alert inbox you can assign a processor for the alert and *save* it

9. Next *filter* for alerts *Expired Certificates* 

    *Enter* `Expired Certificates`in field *Alert Name* and *apply* for the filter
    
10. *Click* on the alert *Expired Certificates*

    This alert is rated as ......

    <br>![](/exercises/ex4/images/HMAlertingRatingOverTime.png)

    > 
    > Alerts originating from *Health Monitoring* are based on the **rating of the related metric**. In the *Alert Details page* the active alerts since the last data collection are displayed with their properties. Cloud Integration is actively pulled every 5 minutes and therefore you might get alerts in this frequency. An alert is active, if one of the metric’s entries (labels) is in a *Warning* or *Critical* state. All alerts related to the same metric and service instance are aggregated to avoid overwhelming the alert inbox.
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
