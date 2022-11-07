# Watch the resolved deployment exception

In this exercise you will check the same integration flow with an exception in the past and now running successfully. This change is visible in the exception page and also in the alerting section of SAP Cloud ALM.

#### Prerequisites:

- *If you are performing configurations yourself:* Eventing and alerting for *Integration Exceptions* should be activated for that Cloud Integration service you are managing: `CloudIntegration-<tenant_name>_<userID>`
- You should corrected the ProcessAdapter channel configuration correctly running through [Exercise 2.6](../..ex26/)

## Exercise steps

Run through the steps in the given order

1. *Click* on the *Automatic Refresh* icon at the black top row and change the refresh frequency to every *15 sec*.

	SAP Cloud ALM is polling the Cloud Integration tenant for monitoring data as default every 5 minutes and we want to avoid waiting. 

	After receiving the event the number of exceptions and the number of alerts increase. *Reset* the *automatic refresh* to default.

2. *Navigate* to the **Exception page** by *clicking* on the *Exceptions* link of your *Cloud Integration* service
    
    <br>![](/exercises/ex2/images/IMExceptionsLink.png)
    
3. Recognize that the switch of the *status* icon in the first column meaning that the *message has run successfully*. The deployment exception has been resolved.

    <br>![](/exercises/ex2/images/IMExceptPageSuccessMoveToDetails.png)

4. *Navigate* to the *exception details page* using the *arrow* icon on the right side (see screenshot above) and see the successful message.

    <br>![](/exercises/ex2/images/IMExceptDetailsSuccessfulMessage.png)

5. *Click* on the *exclamation mark* icon on the left navigation to navigate to the **alerting section**

6. In case you have to filter for the alert related to integration flow you have deployed, use the *filter* icon in the light grey row on the right and filter for the *Object Details* **Hallo_World_`<userID>`**

   You will see the alert details, highlighting not only that the exception is resolved but also when. .....
   
   > MARKUS: kindly ask you to add here more info

    <br>![](/exercises/ex2/images/IMExceptAlertDetailsSuccessfulMessage.png)


## Summary

You've now seen that a resolved integration exception shows up in SAP Cloud ALM as an event and an alert.

Congratulation. You have finalized [Exercise 2](/exercises/ex2/ex25).



