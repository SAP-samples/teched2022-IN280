# Display the deployment exception

In this exercise you will check whether the deployment exception is displayed in *Integration & Exception Monitoring*.

#### Prequisites:

- You are logged in to the [SAP Cloud ALM tenant](https://teched22-cloudalm-003.authentication.eu10.hana.ondemand.com/) and within *Integration & Exception Monitoring*
- Events for *Integration Exceptions* are activated and you have provoked a deployment exception in SAP Integration Suite

## Exercise steps

Run through the steps in the given order

1. *Click* on the *AUtomatic Refresh* icon at the black top row to pull for data from Cloud Integration tenant every *15 sec*.

	SAP Cloud ALM is polling the Cloud Integration tenant for monitoring data every 5 minutes. We want to avoid to wait 5 minutes will reset this right after we have received the event.

	<br>![](/exercises/ex2/images/IMExceptRefresh15sec.png)

2. After receiving the event the number of exceptions and the number of alerts increase. *Reset* the *automatic refresh* to default.

    <br>![](/exercises/ex2/images/IMExceptRefreshReset.png)
 
 	> Improve the screenshot to have 0 messages, 1 exception and 1 alert

3. *Click* on the *Exceptions* link

4. Look over the **Exception page** and afterwards *navigate* to the details page

    <br>![](/exercises/ex2/images/IMExceptPageNavigateToDetails.png)
	
	>
	> Description of the page ncessary ...
	> 

5. *Login* 

    <br>![](/exercises/ex2/images/xxx.png)







X. xxxxxx 

    <br>![](/exercises/ex2/images/xxx.png)


## Summary

You've now copied an existing integration flow, configured and deployed it and provoke an exception error. 

Go back to the main [Exercise 2](../../ex2/) to check whether the deployment exception is displayed in *Integration & Exception Monitoring*.






















