# Exercise 3.4 - Analyze the path of a single message

In this exercise, you will analyze a single message that is part of the integration scenario *ExternalWorkforce*

#### Prerequisites:

- You are in *SAP Integration Suite messages list* of the business scenario *ExternalWorkforce*

## Exercise steps

Run through the steps in the given order.

1.	*Click* on the first message to navigate to the **single message details view page**

    <br>![](/exercises/ex3/images/IMWorkforceFirstMessage.png) 

    This page consists of two sections:
     
2. In the *Message Details* section *click* on *Technical Correlation* to see the parameters of **SAP Passport**

    <br>![](/exercises/ex3/images/IMWorkforceSAPPassport.png)

    >
    > Single messages in a hybrid landscape are correlated to each other to **assemble an end-to-end message path**. To accomplish this the **SAP Passport mechanism** is leveraged. SAP applications are using this approach to mix in a *transaction ID* and a unique *correlation ID*.
    > 

3. *Click* on the tab *Related Messages & Exceptions* to see the assembled **message path**

    <br>![](/exercises/ex3/images/IMWorkforceMessagePath.png) 

    The message `S43..` has been sent from the *SAP Fieldglass* instance `MyFieldGlass_01` to the *Cloud Integration capability of SAP Integration Suite* instance `MyCPI_01` and further to the receiver *SAP S/4HANA Cloud* instance `MyS4HANACloud_01`.
    
4. Go back to the *SAP Integration Suite Messages* page leveraging the *breadcrumb* and *select* the only *failed message* `1EGT...`

    <br>![](/exercises/ex3/images/IMWorkforceFailedMessage.png)

5. In the *message details* you see that the status of message `1EGT...` is failed

    <br>![](/exercises/ex3/images/IMWorkforceMessageDetailsFailed.png)

6. In the *Related messages & exceptions* section you get some hints where to find the issue

    <br>![](/exercises/ex3/images/IMWorkforceFailedMessagePath.png)

    There is a *Java script exception* with the integration flow *Replicate Purchase Requisition from SAP Fieldglass to SAP S4HANA*. To localize the error in details you may navigate to the **local Cloud Integration monitoring** using the link *Local Monitoring* in section *Message Details*. 

    >
    > *Note:* As we are in a demo environment this isn't possible.
    >    
    
    
## Summary

Now you have analyzed a single message that is part of the integration scenario *ExternalWorkforce*

<br>Continue to - [Exercise 3.5 - Search a failed message under tracking](/exercises/ex3/ex35/)
