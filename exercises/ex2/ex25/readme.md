# Exercise 2.5 - Display the deployment exception

In this exercise you will check whether the deployment exception is displayed in *Integration & Exception Monitoring*.

#### Prerequisites:

- You are logged in to the [SAP Cloud ALM tenant](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home) and navigated to [*Integration & Exception Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=com.sap.crun.imapp.ui#/Home)
- *If you are performing configurations yourself:* Events for *Integration Exceptions* should be activated for that Cloud Integration service you are managing: `CloudIntegration-<tenant_name>_<userID>`
- You should have provoked a deployment exception of an integration flow in SAP Integration Suite

## Exercise steps

Run through the steps in the given order

1. *Optionally* *click* on the *Automatic Refresh* icon at the black top row and change the refresh frequency to every *15 sec*. 
	
	SAP Cloud ALM is polling the Cloud Integration tenant for monitoring data as default every 5 minutes and we want to avoid waiting. 
	
	After receiving the event the number of exceptions and the number of alerts increase in the card of the Cloud Integration service you are watching. *Reset* the *automatic refresh* to *5 Minutes*.

	<br>![](/exercises/ex2/images/IMExceptRefresh15sec.png)

3. *Click* on the *Exceptions* link of your *Cloud Integration* service and familiarize yourself with the **Exception page** 

	<br>![](/exercises/ex2/images/IMExceptionsLink.png)

4. *Navigate* to the details page

    <br>![](/exercises/ex2/images/IMExceptPageNavigateToDetails.png)
	
	>
	> Description of the page necessary ...
	> 

5. Within the *exception details page* you can see that an integration exception shows up. Also the related integration artifact and the responsible user are listed.

    <br>![](/exercises/ex2/images/IMExceptDetailsHalloUser.png)

	>
	> In future there will be the possibility to navigate forward directly to the *Integration Content Monitor* of the responsible Cloud Integration tenant to resolve the deployment exception occurred.
	>


## Summary

You've now seen how an integration exception shows up in SAP Cloud ALM and where to get the details.

<br>Continue to - [Exercise 2.6 - Watch a deployment exception alert](./ex26/readme.md)




















