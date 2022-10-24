# Watch the resolved deployment exception

In this exercise you will check the same integration flow with an exception in the past and now running successfully. This change is visible in the exception page and also in the alerting section of SAP Cloud ALM.

#### Prerequisites:

- Events for *Integration Exceptions* are activated and you have provoked a deployment exception in SAP Integration Suite
- You have corrected the ProcessAdapter channel configueration correctly runnding through [Exercise 2.6](../..ex26/)

## Exercise steps

Run through the steps in the given order

1. *Click* on the *Automatic Refresh* icon at the black top row and change the resresh frequency to every *15 sec*.

	SAP Cloud ALM is polling the Cloud Integration tenant for monitoring data as default every 5 minutes and we want to avoid waiting. 

	<br>![](/exercises/ex2/images/IMExceptRefresh15sec.png)

    After receiving the event the number of exceptions and the number of alerts increase. *Reset* the *automatic refresh* to default.



2. *Click* on the *Exceptions* link of your *Cloud Integration* service

    <br>![](/exercises/ex2/images/IMExceptPageSuccessMoveToDetails.png)
  
    You see that the *status* icon in the first column and the corresponding comments mention that the message run successful now.

4. *Navigate* to the *exception details page* using the *arrow* icon on the right side (see screenshot above) and see the successful message.

    <br>![](/exercises/ex2/images/IMExceptDetailsSuccessfulMessage.png)

5. *Click* on the *exclamation mark* icon on the left navigation to navigate to the *alerting* section

    Again here you can see that this message run successfully

    <br>![](/exercises/ex2/images/IMExceptAlertDetailsSuccessfulMessage.png)


## Summary

You've now seen that a resolved integration exception shows up in SAP Cloud ALM as an event and an alert.

Congratulation. You have finalized [Exercise 2](/exercises/ex2/ex25).



