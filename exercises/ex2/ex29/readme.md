# Exercise 2.9 - Search for customer header properties

In this exercise, you will search single messages based on a specific business context attribute, your *userID*. Searches are performed in the *tracking section* of *Integration & Exception Monitoring*. From the resulting messages it is possible to navigate forward to the SAP Integration Suite monitoring 

#### Prerequisites:

- You are in [*Integration & Exception Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=com.sap.crun.imapp.ui#/Home) and have the Cloud Integration service in scope where you had deployed the integration flow successfully.

## Exercise steps

Run through the steps in the given order.

1. *Click* on the *magnifying glass* icon in the left-side navigation

    > You can search attributes that are exposed by the service to SAP Cloud ALM. For Cloud Integration these are:
    > - **Technical properties** such as *message ID, correlation ID* (relates integration flows that belong to one execution)
    > - **Artifact details** such as *name* and *ID*, also *package name* and *ID*
    > - **Business and payload related content** if added to the MPL during runtime
    >    - *Sender ID, Receiver ID, custom status, application message ID* and *type*, set by means of a content modifier step
    >    - **Custom header properties** (name value pair) containing business or payload-related information to be set by means of scripts
    >

2. *Enter* your `userID` as a criteria and *start* the search

    The prepared integration flow *Hallo World - `userID`* adds your `userID` to the custom header properties via Groovy script
        
    <br>![](/exercises/ex2/images/IMExceptTrackingMoveToDetails.png)

    In the result list you see all the messages that have been transferred along with the corresponding SAP Integration Suite tenant and the transfer time stamp 
    
    The search in SAP Cloud ALM is executed cross all services
       
3. *Click on an entry* and navigate to the **single message details page**
    
    Here you get information regarding the assembled message path with the possibility to jump to local monitoring in Cloud Integration to react on an issue

4. Within the *Status Details* section *click* on **Local monitoring**

    <br>![](/exercises/ex2/images/IMExceptTrackingMessageDetailsLocalMonitoring.png)

5. You have been navigated forward to the local *MPL monitoring* of SAP Integration Suite

    <br>![](/exercises/ex2/images/IMExceptTrackingMessageInMPL.png)

    From the *monitoring page* you have any possibility such as to navigate to the *integration designer* to do changes on the integration flow
    
## Summary

Now you have searched for messages based on a specific business context attributes available with the custom header properties and you have navigated forward to the SAP Integration Suite monitoring 

<br>Congratulation. You have finalized Exercise 2. Continue to [Exercise 2](/exercises/ex3/)
