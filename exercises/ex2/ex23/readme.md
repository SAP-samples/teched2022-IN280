Deploy faulty integration flow

In this exercise you will copy a prepared integration flow, configure, and deploy it

#### Prequisites:

- You are logged in to the [SAP Cloud ALM tenant](https://teched22-cloudalm-003.authentication.eu10.hana.ondemand.com/) and to the SAP Integration Suite tenant you are assigned to.
- Your Cloud Integration service is already registered. If not please run through exercise [Register a Cloud Integration tenant in LMS](/exercises/ex1/ex11/).

## Exercise steps

Run through the steps in the given order

1. *Login* to *SAP Integration Suite* leveraging user / password retrieved from the Tenant Booker application

    <br>![](/exercises/ex1/images/Login.png)

2. *Move* to the *Integration Designer* 

    The new SAP Integration Suite home page offers a new left-side navigation. *Click* on *Design* and then on *Integration* to get to the integration packages. 
    
    <br>![](/exercises/ex1/images/SuiteMoveDesigner.png)
    
3. *Select* the prepared integration package *TechEd 2022 IN280*

    <br>![](/exercises/ex1/images/SuiteDesignerSelectPackage.png)
    
4. *Switch* to the *Artifacts* tab, *select* *Actions* and then *Copy* to copy the prepared integration flow as your own one

    <br>![](/exercises/ex1/images/SuiteArtifactsActionsCopy.png)
  
5. In the copy dialog *replace* the `userID` in field *Name* of the targeted integration flow with the userID you got from the Tenant Booker application. 

    The new integration flow should be *Hallo World -* `userID` and part of the existing integraion package.

    <br>![](/exercises/ex1/images/SuiteDesignerCopyFlow.png)

6. *Select* *Actions* and then *Configure*

    <br>![](/exercises/ex1/images/SuiteArtifactsActionsConfigure.png)
    
7. *Set* in field *userID* the userID you have got via the Tenant Booker application. 
    
    **Don't** change any the channel fields.
    
    *Deploy* the integration flow. 
    
    <br>![](/exercises/ex1/images/SuiteDesignerConfigureUser.png)
    
    A popup appears to save the configuration. *Save* it.
    
    Another popup appears regarding the deployment, *click* on *Ok*.

8. *Move* to the *Integration Monitor* 

    <br>![](/exercises/ex1/images/SuiteMoveMonitor.png)

9. *Select* the tile *All* in the section *Manage Integration Content* 

    <br>![](/exercises/ex1/images/SuiteMonitorMoveToContent.png)

10. *Reload* the list of deployed artifacts until the integration flow you have deployed switches from *Starting* to status *Error*

    <br>![](/exercises/ex1/images/SuiteMPLConsumer001ExistsAlready.png)

    > Provide argument why it is an Error .....

## Summary

You've now copied an existing integration flow, configured and deployed it and provoke an exception error. 

Go back to the main [Exercise 2](../../ex2/) to check whether the deployment exception is displayed in *Integration & Exception Monitoring*.
