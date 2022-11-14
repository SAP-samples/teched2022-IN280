# Exercise 3.5 - Search for a failed message

In this exercise, you will search for a failed message that is part of the integration scenario *ExternalWorkforce* in the *tracking* section of *Integration & Exception Monitoring*

#### Prerequisites:

- You are in [*Integration & Exception Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=com.sap.crun.imapp.ui#/Home) and have the integration scenario *ExternalWorkforce* in scope

## Exercise steps

Run through the steps in the given order.

1. *Click* on the *magnifying glass.* icon in the left-side navigation

2. *Select* the business service *ExternalWorkforce*. 

    All business scenarios in scope are proposed in a drop down list

3. *Enter* the search criteria `1EGT*` or `1EGT0e1kEW2C6kPVvE3GCitCRHyw` and *start* the search

    <br>![](/exercises/ex3/images/IMWorkforceTrackingFailedMessage.png)

    You can already recognize in **tracking result list** that the message has a Java script issue. From the entry it is possible to navigate directly to the *message details page* using the link behind the *message ID* `1EGT0e1kEW2C6kPVvE3GCitCRHyw`. There you get the information regarding the assembled message path with the possibility to navigate further to local monitoring to do the issue resolution in Cloud Integration.

    
    
## Summary

Now you have searched for a failed message that is part of the integration scenario *ExternalWorkforce*

<br>Continue to - [Exercise 3.6 - Check failed message alerts](/exercises/ex3/ex36/)
