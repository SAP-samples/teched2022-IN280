# Activate alerts
In this exercise, we will activate the alerting for a particular Cloud Integration service.
*This exercise is only necessary if you want to perform all configuration in SAP Cloud ALM yourself.*

#### Prerequisites
- You are logged in to [SAP Cloud ALM](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home) and navigated to [*Health Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=sap.crun.hmapp.ui)
- The Cloud Integration service `CloudIntegration-<tenant_name>_<userID>` you are managing is in scope

## Exercise steps

Run through the  steps in the given order.

1. Click on the *configuration* icon, *expand* the *Services* section, and *select* the Cloud Integration service `CloudIntegration-<tenant_name>_<userID>` you have registered

    <br>![](/exercises/ex4/images/HMSelectConfiguration.png)

2. Switch to the *Events* tab and *Click* on the event *Expired Certificate*

    <br>![](/exercises/ex4/images/HMConfigSelectEventCertificate.png)

3. Use the *switch button* to activate the alert and *save* the configuration for this particular **metric related event**

    <br>![](/exercises/ex4/images/HMConfigTurnOnEventCertificate.png)
     
    >
    > *Note:* The activation of email notification, starting of an operation flow, and creating a ServiceNow ticket is out of scope of the TechEd session IN280
    > 

4. *Activate* all other events *JMS Queue Capacity*, *JMS Queue entries*, *JMS Queue Messages*, *JMS Queue Status* in the same matter as described in steps 2 and 3

    After the configuration you see all events activated
    
    <br>![](/exercises/ex4/images/HMConfigActiveAlerts.png)

    Keep in mind this configuration is valid only for the selected Cloud Integration service

5. *Close* the configuration and click again on the configuration icon to close the right configuration frame
   

## Summary

You've now activated alerts for events to selected metrics of a particular Cloud Integraion service. These alerts will be displayed in the *Alerting* section.

Go back to [Exercise 4](../../ex4/readme.md)


