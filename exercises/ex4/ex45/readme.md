# Activate alerts
In this exercise, we will activate the alerting for a particular Cloud Integration service on the level of the metrics

## Exercise steps

Run through the exercise steps in the given order.

First we have to **activate alerts** on metric level

1. Click on the *configuration icon* and select the service you have registered

<br>![](/exercises/ex4/images/HMSelectConfiguration.png)

2. Switch to the *Events* tab if necessary

<br>![](/exercises/ex4/images/HMConfigSwitchToEvents.png)

3. Click on the event *Expired Certificate*

<br>![](/exercises/ex4/images/HMConfigSelectEventCertificate.png)

4. Use the switch button to activate the alert and save the configuration for this event

<br>![](/exercises/ex4/images/HMConfigTurnOnEventCertificate.png)

5. Do same steps *c.* and *d.* for the events *JMS Queue Capacity*, *JMS Queue entries*, *JMS Queue Messages*, *JMS Queue Status* 

After the configuration you see all events activated

<br>![](/exercises/ex4/images/HMConfigActiveAlerts.png)

Keep in mind this configuration is valid for a particular registered service and not for all Cloud Integration services

6. *Close* the configuration and click again on the configuration icon to close the right configuration frame.
   

## Summary

You've now activated alerts for all events of the service your have registered. Alerts will be displayed in the page *Alerting*.

Go back to [Exercise 4](../../ex4/readme.md)





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
