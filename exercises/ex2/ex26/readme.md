# Exercise 2.6 - Watch a deployment exception

In this exercise you will see a deployment exception as an example of an alert in *Integration & Exception Monitoring*.

#### Prerequisites:

- You are logged in to the [SAP Cloud ALM tenant](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home) and have navigated to [*Integration & Exception Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=com.sap.crun.imapp.ui#/Home)
- *If you are performing all configurations yourself:* Alerting for *Integration Exceptions* should be activated for that Cloud Integration service you have registered: `CloudIntegration-<tenant_name>_<userID>`
    
    In the *preconfigured Cloud Integration service* in SAP Cloud ALM `CloudIntegration-<tenant_name>` the alerting to integration exceptions is already activated and nothing had to be done.
    
- You have provoked a deployment exception in the Cloud Integration capability of SAP Integration Suite

## Exercise steps

Run through the steps in the given order

1. There are two options to **jump to the alerting section**:

	- *Click* on the *exclamation mark* icon on the left navigation to see all alerts raised for the services and scenarios in scope
	- *Click* on the *number* of Alters mentioned in the footer row of the card. Please use this option.

	<br>![](/exercises/ex2/images/IMExceptOverviewMoveToAlerting.png)
    
	<br>![](/exercises/ex2/images/IMExceptAlerting.png)
	
2. **Filter** for alerts related to integration flows you have deployed

    *Click* on the *filter* icon in the upper light grey row on the right and filter for the *Object Details* **Hallo_World_`<userID>`**

    
    <br>![](/exercises/ex2/images/IMExceptAlertFilter.png)
     
    - In case your are using one of the default pre-configured *Cloud Integration services* the alert name is **Errorneous Integratio Artifact**
    - In case you have added own alert to the *Cloud Integration service* you are managing yourself the alert name should be `userID` **Exceptions**
    

3. See the **Alert Details** via *clicking* on the alert link

	<br>![](/exercises/ex2/images/IMExceptAlertDetails.png)

    
	
## Summary

You've now seen how an alert reaches the embedding alerting in *Integration & Exception Monitoring*.

<br>Continue to - [Exercise 2.7 - Configure the ProcessDirect channels correctly and deploy integration flow successfully](/exercises/ex2/ex27/)
