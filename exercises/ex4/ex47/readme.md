# Exercise 4.7 - Activate alerts

In this exercise, we will activate the alerting for a particular Cloud Integration service to raise alerts

:warning: This exercise is only necessary if you have a **self-managed *Cloud Integration service***

For all *preconfigured Cloud Integration service* the alerting is already activated and you can jump directly to [Exercise 4.8 - Check alerts in Health Monitoring](/exercises/ex4/ex48/)


#### Prerequisites
- You are in [*Health Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=sap.crun.hmapp.ui)
- Your self-managed `CloudIntegration-<tenant_name>-<userID>` service is in scope

## Exercise steps

Run through the steps in the given order

1. *Click* on the **configuration** icon, *expand* the *Services* tray, and *select* the *Cloud Integration service* `CloudIntegration-<tenant_name>_<userID>` you have registered

    <br>![](/exercises/ex4/images/HMSelectConfiguration.png)

2. *Switch* to the **Events** tab and *click* on the event **Expired Certificate**

    <br>![](/exercises/ex4/images/HMConfigSelectEventCertificate.png)

3. *Change* the *toggle button* from *off* to *on* if not changed automatically. **Save** the activation for this particular **metric related event**

    <br>![](/exercises/ex4/images/HMConfigTurnOnEventCertificate.png)
     
    >
    > *Note:* If you want you can *activate* email notification
    >

4. *Activate* all other events *JMS Queue Capacity*, *JMS Queue entries*, *JMS Queue Messages*, *JMS Queue Status* in the same manner as described in steps 2 and 3

    After the configuration you should see all events activated
    
    <br>![](/exercises/ex4/images/HMConfigActiveAlerts.png)

5. *Close* the configuration and *click* again on the *configuration* icon to close the right configuration frame
   

## Summary

You've now activated alerts of selected metrics for a particular Cloud Integration service. Alerts will be displayed in the *Alerting* section.

<br>Continue to - [Exercise 4.8 - Check alerts in Health Monitoring](/exercises/ex4/ex48/)

