# Exercise 2.9 - Watch the resolved deployment exception

In this exercise you will check the integration flow again now running successfully. This change is visible in the exception page and also in the alerting section of SAP Cloud ALM.

#### Prerequisites:

- You are in [*Integration & Exception Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=com.sap.crun.imapp.ui#/Home)
- You should have corrected the ProcessAdapter channel configuration as outlined in [Exercise 2.7](/exercises/ex2/ex27/)
 - :construction_worker: *If you have a self-managed `CloudIntegration-<tenant_name>-<userID>` service* : Eventing and alerting for *Integration Exceptions* should be activated


## Exercise steps

Run through the steps in the given order

1. *Navigate* to the **Exception page** by clicking on the *warning* icon in the left-side navigation
    
    <br>![](/exercises/ex2/images/IMExceptionsLink.png)
    
2. *Optionally* click on **Refresh** at the black top row to get your user interface updated
	
3. After receiving the event the number of exceptions and the number of alerts should decrease

    :clock1: It can take up to 5 minutes until data collection has been executed


4. *Click* on the **Integration Artifacts Deployments** link of the *Cloud Integration* service you are monitoring, either default or your self-managed `CloudIntegration-<tenant_name>-<userID>` service

    Recognize that you can see that the integration flow has changed it's **exceptions status** from *Error* to **Resolved**. This is visible in the lower list where the icon in the first column has changed to **green**. Also in the upper overview section you see now *resolved exceptions*

    <br>![](/exercises/ex2/images/IMExceptPageSuccessMoveToDetails.png)

5. *Navigate* to the **exception details page** using the *arrow* icon on the right side (see screenshot above) and see the successful message

    <br>![](/exercises/ex2/images/IMExceptDetailsSuccessfulMessage.png)

5. *Click* on the *exclamation mark* icon on the left navigation to navigate to the **alerting section**

#### Now we want to oversee the exception alerts

6. **Filter** for alerts related to integration flows you have deployed

    *Click* on the *filter* icon in the upper light grey row on the right and filter for the *Object Details* **`<userID>`**

    <br>![](/exercises/ex2/images/IMExceptAlertFilter.png)
    
    - In case you are using one of the **default and pre-configured** *Cloud Integration services* the alert name is **<tenant_name> Deployment Exception**
    - :construction_worker: you had created the event name in [Excercise 2.4](/exercises/ex2/ex24/), proposed was **<tenant_name> Deployment Exception `<userID>`**
   
7. See the **Alert Details** via *clicking* on the alert link

    <br>![](/exercises/ex2/images/IMExceptAlertDetailsSuccessfulMessage.png)


## Summary

You've now seen that a resolved integration exception shows up in SAP Cloud ALM as an event and an alert.

<br>Continue to - [Exercise 2.10 - Search for customer header properties](/exercises/ex2/ex210/)
