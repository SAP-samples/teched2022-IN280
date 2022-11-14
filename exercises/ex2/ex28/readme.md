# Exercise 2.8 - Configure the ProcessDirect channels correctly

In this exercise you will deploy the integration flow successfully by configuring unique and identical ProcessDirect channel IDs

#### Prerequisites:

- You are logged in to the SAP Integration Suite tenant and navigated to the integration package **TechEd 2022 IN280**
- You had deployed the misconfigured integration flow *Hallo World -* `userID`

## Exercise steps

Run through the steps in the given order

1. *Click* on **Actions** of your integration flow *Hallo World - *`userID`* and then on **Configure**

    <br>![](/exercises/ex2/images/SuiteArtifactsActionsConfigure.png)
    
2. *Set* the fields *consumerChannel* and *producerChannel* to `channel_userID` and the field *userID* to `userID`
    
    **Note: The channel IDs should be unique and identical. Best to use your `userID`**
    
    **Deploy** the integration flow *Hallo World -* `userID`.
    
    <br>![](/exercises/ex2/images/SuiteDesignerConfigureCorrectly.png)
    
    A popup appears to save the configuration. *Save* it.
    
    Another popup appears regarding the deployment, *click* on *Ok*.

3. *Move* to the **integration content monitor**

    a. *Click* on *Integration - Monitor* in the left-side navigation
    
    b. *Click* on the first tile of *Manage Integration Content*

4. **Reload** the list of deployed artifacts until the integration flow *Hallo World -* `userID` you have deployment status changed from *Starting* to **Started**

    <br>![](/exercises/ex2/images/SuiteMPLSuccess.png)
    
5. *Move* to the **MPL monitor**

    a. Use the *Overview* link of the breadcrumb  in the top row to get back to the *monitor overview page*

    b. *Click* on the first tile *All Integration Flows* of the section *Monitor Message Processing*

6. **Select your message** *Hallo World -  `userID`* that should have been exchanged successfully

    <br>![](/exercises/ex2/images/SuiteMPLMessageSuccess.png)

    You might have to filter for your artifact  *Hallo World -* `userID` if the list of messages is lengthy 
    
## Summary

You've now configured the integration flow correctly and deployed it successfully.

<br>Continue to - [Exercise 2.9 - Watch the resolved deployment exception](/exercises/ex2/ex29/)



