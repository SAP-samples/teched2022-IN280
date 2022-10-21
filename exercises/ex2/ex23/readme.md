# Deploy a faulty integration flow

In this exercise you will copy a prepared integration flow, configure, deploy it, and provoke a deployment exception.

#### Prequisites:

- You are logged in to the SAP Integration Suite tenant you are assigned to.
- Your Cloud Integration service is already registered. If not please run through exercise [Register a Cloud Integration tenant in LMS](/exercises/ex1/ex11/).

## Exercise steps

Run through the steps in the given order

1. *Login* to *SAP Integration Suite* leveraging user / password retrieved from the Tenant Booker application

    <br>![](/exercises/ex2/images/Login.png)

2. *Move* to the *Integration Designer* 

    The new SAP Integration Suite home page offers a new left-side navigation. *Click* on *Design* and then on *Integration* to get to the integration packages. 
    
    <br>![](/exercises/ex2/images/SuiteMoveDesigner.png)
    
3. *Select* the prepared integration package *TechEd 2022 IN280*

    <br>![](/exercises/ex2/images/SuiteDesignerSelectPackage.png)
    
4. *Switch* to the *Artifacts* tab, *select* the button *Actions* and then *click* on *Copy* to copy the prepared integration flow

    <br>![](/exercises/ex2/images/SuiteArtifactsActionsCopy.png)
  
5. In the copy dialog *replace* the `userID` in field *Name* with the userID you got from the Tenant Booker application. 

    The new integration flow should be named *Hallo World -* `userID` and be part of the existing integration package.

    <br>![](/exercises/ex2/images/SuiteDesignerCopyFlow.png)

6. *Click* on *Actions* of your integration flow and then on *Configure*

    <br>![](/exercises/ex2/images/SuiteArtifactsActionsConfigure.png)
    
7. *Set* in field *userID* the userID you have got via the Tenant Booker application. 
    
    **Don't change any the channel fields to provoke a deployment error**.
    
    *Deploy* the integration flow *Hallo World -* `userID`.
    
    <br>![](/exercises/ex2/images/SuiteDesignerConfigureUser.png)
    
    A popup appears to save the configuration. *Save* it.
    
    Another popup appears regarding the deployment, *click* on *Ok*.

8. *Move* to the *Integration Monitor* 

    <br>![](/exercises/ex2/images/SuiteMoveMonitor.png)

9. *Select* the tile *All* in the section *Manage Integration Content* 

    <br>![](/exercises/ex2/images/SuiteMonitorMoveToContent.png)

10. *Reload* the list of deployed artifacts until the integration flow *Hallo World -* `userID` you have deployed switches from *Starting* to status *Error*

    <br>![](/exercises/ex2/images/SuiteMPLConsumer001ExistsAlready.png)

    > Provide argument why it is an Error .....

## Summary

You've now copied an existing integration flow, configured and deployed it and provoke an exception error. 

Go back to the main [Exercise 2](../../ex2/) to check whether the deployment exception is displayed in *Integration & Exception Monitoring*.
