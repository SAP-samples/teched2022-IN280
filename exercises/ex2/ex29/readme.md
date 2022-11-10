# Exercise 2.9 - Search for customer header properties

In this exercise, you will search for your *userID* in the *tracking section* of *Integration & Exception Monitoring* and navigate forward to the SAP Integration Suite monitoring 

#### Prerequisites:

- You are in [*Integration & Exception Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=com.sap.crun.imapp.ui#/Home) and have the Cloud Integration service in scope where you had deployed the integration flow successfully.

## Exercise steps

Run through the steps in the given order.

1. *Click* on the *magnifying glass* icon in the left-side navigation

2. *Enter* your `userID` as a search criteria and *start* the search

    <br>![](/exercises/ex2/images/IMExceptTrackingMoveToDetails.png)

    In the result list you see all the messages that have been transferred along with the corresponding SAP Integration Suite tenant and the transfer time stamp 
    
3. *Click* on an entry and you will be navigated to the *message details page*
    
    Here you get information regarding the assembled message path with the possibility to navigate further to local monitoring to do the issue resolution in Cloud Integration.

4. Within the *Status Details* section *click* on *Local Monitoring*

    <br>![](/exercises/ex2/images/IMExceptTrackingMessageDetailsLocalMonitoring.png)

5. You have been navigated forward to the local *MPL monitoring* of SAP Integration Suite

    <br>![](/exercises/ex2/images/IMExceptTrackingMessageInMPL.png)

    Within the integration flow we have used Groovy scripts that added properties to the header and can be searched in SAP Cloud ALM
    
    From the monitoring page you have the possibility to navigate to the *integration designer* to do changes on the integration flow
    
## Summary

Now you have searched for a message using a custom header property and navigated from search forward to the SAP Integration Suite monitoring 

<br>Continue to - [Exercise 3.6 - Watch alerts that have been raised for failed messages](/exercises/ex3/ex36/)
