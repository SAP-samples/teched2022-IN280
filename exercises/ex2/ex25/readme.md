# Exercise 2.5 - Display the deployment exception

In this exercise you will examine deployment exceptions in *Integration & Exception Monitoring*

#### Prerequisites:

- You are logged in to the [SAP Cloud ALM tenant](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home) and navigated to [*Integration & Exception Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=com.sap.crun.imapp.ui#/Home)
- You should have provoked a deployment exception of an integration flow in SAP Integration Suite
- *If you are performing configurations yourself:* Events and alerts for *Integration Exceptions* should be activated for that Cloud Integration service you are managing: `CloudIntegration-<tenant_name>_<userID>`


## Exercise steps

Run through the steps in the given order

1. Navigate to the **Exceptions overview page** by using the *Warning* icon in the left-side navigation

	<br>![](/exercises/ex2/images/IMExceptRefresh.png)
	
2. *Optionally* *click* on **Refresh** at the black top row to get your **user interface** updated

	SAP Cloud ALM is **polling** Cloud Integration tenants for monitoring data as default **every 5 minutes**. Therefore it might be that you have to wait until the next data collection. 

	:warning: In the meanwhile you have the possibility to understand how the data collection is working and how to check when the next data collection will happen
	
3. After receiving the event from the deployment exception that you have provoked in [Excercise 2.4](./ex24/readme.md) the number of exceptions and the number of alerts should increase. 

	<br>![](/exercises/ex2/images/IMExceptionsLink.png)
	
4. *Click* on the **Exceptions** link of the *Cloud Integration* service you are monitoring, either one of the six default ones or your self-managed service  `CloudIntegration-<tenant_name>_<userID>` (depending on the services you have in scope)

4. The **exception page** (see screenshot below) is related to a **particular registered service** such as one of the default Cloud Integration services or your owned-managed `CloudIntegration-<tenant_name>_<userID>`
	
	- It displays not only the current exceptions, but also the ones that have had a deployment exception in the past and have been **resolved** in the meanwhile
	- In the first section you get an overview on the number of deployment exception and resolved ones
	- :warning: .....

    <br>![](/exercises/ex2/images/IMExceptPageNavigateToDetails.png)

6. *Click* on the exceptions that you have provoked (artifact name *Hallo World - `UserID`*)

    <br>![](/exercises/ex2/images/IMExceptDetailsHalloUser.png)
	
	Within the **exception details page** you can see the related integration artifact and the deploying user along with the deployment time stamp and the status, whether the exception is resolved or not.

## Summary

You've now seen how an integration exception shows up in SAP Cloud ALM and where to get the details.

<br>Continue to - [Exercise 2.6 - Watch a deployment exception alert](./ex26/readme.md)




















