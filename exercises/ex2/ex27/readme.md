# Exercise 2.7 - Configure the ProcessDirect channels correctly and deploy integration flow successfully

In this exercise you will deploy the integration fow successfully by configuring unique and identical ProcessDirect channel IDs

#### Prequisites:

- You are logged in to the SAP Integration Suite tenant and navigated to the integration package **TechEd 2022 IN280**
- You had deployed the incorrect integration flow *Hallo World -* `userID`

## Exercise steps

Run through the steps in the given order

1. *Click* on **Actions** of your integration flow *Hallo World - *`userID`* and then on **Configure**

    <br>![](/exercises/ex2/images/SuiteArtifactsActionsConfigure.png)
    
2. *Set* the fields *consumerChannel* and *producerChannel* to `channel_userID`and the field *userID* to `userID`
    
    **Note: The channel IDs should be unique and identical. Best to use your `userID`**
    
    **Deploy** the integration flow *Hallo World -* `userID`.
    
    <br>![](/exercises/ex2/images/SuiteDesignerConfigureCorrectly.png)
    
    A popup appears to save the configuration. *Save* it.
    
    Another popup appears regarding the deployment, *click* on *Ok*.

3. *Switch* to the **integration content monitor** as done in [exercise 2.3](../../ex2/ex23/) step 8 and **reload** the list of deployed artifacts until the integration flow *Hallo World -* `userID` you have deployed switches from *Starting* to status **Started**

    <br>![](/exercises/ex2/images/SuiteMPLSuccessHallo.png)
    
4. Switch to the **MPL monitor**

    a. Use the *Overview* link of the breadcrumb  in the top row to get back to the *monitor overview page*

    b. *Click* on the first tile *All Integration Flows* of the section *Monitor Message Processing*

5. *Select your message** that should have been exchanged successfully: *Hallo World -  `userID`*

    <br>![](/exercises/ex2/images/SuiteMPLMessageSuccess.png)

    You might have to filter for your artifact  *Hallo World -* `userID` if the list of messages is lenghty 
    
## Summary

You've now configurde the integration flow correclty and deployed it successfully.

<br>Continue to - [Exercise 2.8 - Watch the resolved deployment exception](/exercises/ex2/ex28/)



