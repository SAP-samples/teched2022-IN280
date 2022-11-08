# Check alerts in Health Monitoring

In this exercise, we will ...
Health Monitoring comes with embedded alerting leveraged for various ALM use cases as for *Health Monitoring* or for *Integration & Exception Monitoring*.

#### Prerequisites:
- You are logged in to [SAP Cloud ALM](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home) and navigated to the *Health Monitoring* application
- *If you are performing configurations yourself*, your Cloud Integration service in SAP Cloud ALM `CloudIntegration-<tenant_name>_<userID>`  should be connected to the Cloud Integration tenant. If not please run through exercise [Configure the monitoring of Cloud Integration tenant in SAP Cloud ALM](../ex1/readme.md)
-  If you are using the *preconfigured Cloud Integration service* in SAP Cloud ALM `CloudIntegration-<tenant_name>` nothing has to be done

## Exercise steps

Run through the exercise steps in the given order

1. *If you are performing configurations yourself:* in the [Exercise 4.5 - Activate alerts](../ex45/readme.md) you activate events for the Cloud Integration service that you have registered.
      
    If you are using the *preconfigured Cloud Integration service* in SAP Cloud ALM `CloudIntegration-<tenant_name>` the alerting is already activated and nothing has to be done and the step can be skipped.

2. *Navigate* to the *Alerting* section using the *exclamation mark* icon in the left-navigation

    <br>![](/exercises/ex4/images/HMAlerting.png)

    In the *Alerting* page one alert per cloud service since the last data collection is listed.

3. *Click* on on the alert *JMS Queue Capacity* 

    The *alert details page* opens for the selected alert. In the screenshot the total queue capacity of the tracked Cloud Integration tenant exceeds the max queue capacity. .........
    You see the rating, all raised messages (single alerts), operation automation logs, and *ServiceNow* tickets

    <br>![](/exercises/ex4/images/HMAlertingCapacity.png)

4. Click on *Actions* and then on *Processor* and *Assign*

    >
    > A reported alert can be treated as a ticket. Somebody can work on it or hand it over to someone else to collaboratively work on it, add useful comments, or start an operation flow. 
    >
    
    | ==Check how we can do this== |


    Assign a processor who should care for the issue that has occured ....

    <br>![](/exercises/ex4/images/HMAlertingActions.png)

5. In *Notification Management* add email recipient, send invitation for email verification, you have ot give your consent, afterwards assign processor

    Message in your browser shows up: *You are subscribed to SAP Cloud ALM notifications.*

    Back in alert inbox you can assign processor for an alert.

    Save

6. Click on Expired Certificates

    This alert is rated as *Ok*

    <br>![](/exercises/ex4/images/HMAlertingRatingOverTime.png)

    > 
    > Alerts originating from *Health Monitoring* are based on the **rating of the related metric**. In the *Alert Details page* the active alerts since the last data collection are displayed with their properties. Cloud Integration is actively pulled every 5 minutes and therefore you might get alerts in this frequency. An alert is active, if one of the metric’s entries (labels) is in a *Warning* or *Critical* state. All alerts related to the same metric and service instance are aggregated to avoid overwhelming the alert inbox.
    >    

7. You may also send notification to email recipients after activation and adding at least one recipient in the configuration of a service.

8. Operations Flow and ServiceNow


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
