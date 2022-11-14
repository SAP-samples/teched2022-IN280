# Exercise 2.5 - Deploy a misconfigured integration flow

In this exercise you will copy a prepared integration flow, configure, deploy it, and provoke a deployment exception.

#### Prerequisites:

- :construction_worker: *If you are performing configurations yourself*: alerting should be activated for your `CloudIntegration-<tenant_name>_<userID>` service

## Exercise steps

Run through the steps in the given order

1. **Login** to *SAP Integration Suite* 

    Use the information from the  [Tenant Booker application](/exercises/ex0/ex02/)
    
    - first link to access the SAP Integration Suite tenant 
    - user / password
    
    <br>![](/exercises/ex2/images/Login.png)
    
  
    <br>![](/exercises/ex2/images/SuiteLoginInfo.png) 

2. *Move* to the **Integration Designer** 

    The new SAP Integration Suite home page offers a new left-side navigation. *Click* on *Design* and then on *Integration* to get to the integration packages. 
    
    <br>![](/exercises/ex2/images/SuiteMoveDesigner.png)
    
3. *Select* the prepared integration package ***TechEd 2022 IN280***

    <br>![](/exercises/ex2/images/SuiteDesignerSelectPackage.png)
    
4. *Switch* to the ***Artifacts*** tab, *select* the button ***Actions*** and then *click* on ***Copy*** to copy the prepared integration flow.
    
    **Note:** **Please don't use the original integration flow!** You will use your own one *Hallo World -* `userID` throughout all exercises and you have to *configure* it only. Edit is not necesssary.

    <br>![](/exercises/ex2/images/SuiteArtifactsActionsCopy.png)
  
5. In the **copy dialog** *replace* in field *Name* the *_copy*  by `- <userID>` with the userID you got from the [Tenant Booker appl](/exercises/ex0/ex02/)

    The new integration flow should be named *Hallo World -* `<userID>` and be part of the existing integration package.

    <br>![](/exercises/ex2/images/SuiteDesignerCopyFlow.png)

6. *Click* on ***Actions*** of your integration flow and then on ***Configure***

    <br>![](/exercises/ex2/images/SuiteArtifactsActionsConfigure.png)
    
7. *Move* to the tab **More** and *set* in field ***userID*** your userID 
    
    **Important: Don't change any other channel fields as we want to provoke a deployment error**.
    
    ***Deploy*** the integration flow *Hallo World -* `userID`.
    
    <br>![](/exercises/ex2/images/SuiteDesignerConfigureUser.png)
    
    A popup appears to save the configuration. *Save* it.
    
    Another popup appears regarding the deployment, *click* on *Ok*.

8. *Move* to the **Integration Monitor** 

    <br>![](/exercises/ex2/images/SuiteMoveMonitor.png)

9. *Select* the first tile in section ***Manage Integration Content***

    <br>![](/exercises/ex2/images/SuiteMonitorMoveToContent.png)

10. ***Reload*** the list of deployed artifacts until the integration flow *Hallo World -* `userID` you have deployed switches from *Starting* status to status ***Error***

    <br>![](/exercises/ex2/images/SuiteMPLConsumer001ExistsAlready.png)

    >
    > Note: The deployment exception *Multiple consumers not supported: consumer channel_001 already exists* shows up because there is in parallel another integration flow running using the same ProcessDirect channel ID. 
    > 

## Summary

You've now copied an existing integration flow, configured and deployed it, and with that provoked an exception error. 

<br>Continue to - [Exercise 2.6 - Display the deployment exception](/exercises/ex2/ex26/readme.md)



















