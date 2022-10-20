# Activate alerts for deployement exceptions for integration artifacts

In this exercise, you will activate the alerting for a particular Cloud Integration service to get an alert once a deployment exception happens

###
Prerequisites:
......

## Exercise steps

Run through the exercise steps in the given order.

First we have to **activate alerts** on metric level

1. Click on the *configuration icon* and *select* the *Cloud Integration* service you have registered

<br>![](/exercises/ex2/images/IMExceptSelectConfiguration.png)

2. *Click* on the service link or the arrow on the right side and navigate to the details of the **service configuration**

<br>![](/exercises/ex2/images/IMExceptConfigSelectService.png)

During setting up the service for the *Cloud Integration* tenant *Landscape Management Service* we have selected several use cases. These two use cases are displayed here as *monitoring categories*:
- *SAP Integration Suite Messages* for *Integration Monitoring*
- *Integration Artifact Deployements* for *Exception Monitoring*

If there are several endpoints available you may switch between them.

The *data collection* toogle should be switched on to collect the data from the *Cloud Integration* tenant.

3. *Click* on the arrow on the right side of the *Integration Artifact Deployments*

<br>![](/exercises/ex2/images/IMExceptSelectUsecase.png)

4. 




5. 
6. 
7. 
8. 
9. Use the switch button to activate the alert and save the configuration for this event

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
