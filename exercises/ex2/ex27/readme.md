# Exercise 2.7 - Watch a deployment exception alert

In this exercise you will see a deployment exception as an example of an alert in *Integration & Exception Monitoring*.

#### Prerequisites:

- You are in [*Integration & Exception Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=com.sap.crun.imapp.ui#/Home)
- You have provoked a deployment exception in the Cloud Integration capability of SAP Integration Suite
- :construction_worker: *If you have a self-managed `CloudIntegration-<tenant_name>-<userID>` service* : Alerting for *Integration Exceptions* should be activated
    
    In the *preconfigured Cloud Integration service* in SAP Cloud ALM `CloudIntegration-<tenant_name>` the alerting to integration exceptions is already activated and nothing had to be done


## Exercise steps

Run through the steps in the given order

1. There are two options to **jump to the alerting section**:

	- *Click* on the *exclamation mark* icon on the left navigation to see all alerts raised for the services and scenarios in scope
	- *Click* on the *number* of Alters mentioned in the footer row of the card. Please use this option.

	<br>![](/exercises/ex2/images/IMExceptOverviewMoveToAlerting.png)
    
2. **Filter** for alerts related to integration flows you have deployed

    *Click* on the *filter* icon in the upper light grey row on the right and filter for *Object Details* **`<userID>`**

    
    <br>![](/exercises/ex2/images/IMExceptAlertFilter.png)
     
    - In case you are using one of the **default and pre-configured** *Cloud Integration services* the alert name is **<tenant_name> Deployment Exception**
    - :construction_worker: you had created the event name in [Excercise 2.4](/exercises/ex2/ex24/), proposed was **<tenant_name> Deployment Exception `<userID>`**
    

3. See the **Alert Details** via *clicking* on the alert link

	<br>![](/exercises/ex2/images/IMExceptAlertDetails.png)

    
	
## Summary

You've now seen how an alert reaches the embedding alerting in *Integration & Exception Monitoring*.

<br>Continue to - [Exercise 2.8 - Configure the ProcessDirect channels correctly](/exercises/ex2/ex28/)
