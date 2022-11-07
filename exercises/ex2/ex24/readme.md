# Display the deployment exception

In this exercise you will check whether the deployment exception is displayed in *Integration & Exception Monitoring*.

#### Prerequisites:

- You are logged in to the [SAP Cloud ALM tenant](https://teched22-cloudalm-003.authentication.eu10.hana.ondemand.com/) and navigated to *Integration & Exception Monitoring*
- Events for *Integration Exceptions* are activated and you have provoked a deployment exception in SAP Integration Suite

## Exercise steps

Run through the steps in the given order

1. *Optionally* *click* on the *Automatic Refresh* icon at the black top row and change the refresh frequency to every *15 sec*. 
	
	SAP Cloud ALM is polling the Cloud Integration tenant for monitoring data as default every 5 minutes and we want to avoid waiting. 
	
	After receiving the event the number of exceptions and the number of alerts increase in the card of the Cloud Integration service you are watching. *Reset* the *automatic refresh* to default.

	<br>![](/exercises/ex2/images/IMExceptRefresh15sec.png)

3. *Click* on the *Exceptions* link of your *Cloud Integration* service and familiarize yourself with the **Exception page** 

4. *Navigate* to the details page

    <br>![](/exercises/ex2/images/IMExceptPageNavigateToDetails.png)
	
	>
	> Description of the page necessary ...
	> 

5. Within the *exception details page* you can see that an integration exception shows up. Also the related integration artifact and the responsible user are listed.

    <br>![](/exercises/ex2/images/IMExceptDetailsHalloUser.png)




## Summary

You've now seen how an integration exception shows up in SAP Cloud ALM and where to get the details.

Continue with the next exercise [Exercise 2](/exercises/ex2/ex25) to watch the same exception in the altering section of SAP Cloud ALM.






















