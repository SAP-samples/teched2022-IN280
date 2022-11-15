# Exercise 3.4 - Analyze the path of a single message

In this exercise, you will analyze a single message that is part of the integration scenario *ExternalWorkforce*

#### Prerequisites:

- You are in *SAP Integration Suite messages list* of the business scenario *ExternalWorkforce*

## Exercise steps

Run through the steps in the given order

1.	*Click* on the first message to navigate to the **single message details view page**

    <br>![](/exercises/ex3/images/IMWorkforceFirstMessage.png) 

    The **single message details view page** consists of two sections:
     
2. In the **Message Details section** you get the *Technical Correlation*

    >
    > Single messages in a hybrid landscape are correlated to each other to **assemble an end-to-end message path**. To accomplish this the **SAP Passport mechanism** is leveraged. SAP applications are using this approach to mix in a *transaction ID* and a unique *correlation ID*.
    > 

3. *Click* on the tab **Related Messages & Exceptions** to see the **message path**

    <br>![](/exercises/ex3/images/IMWorkforceMessagePath.png) 

    In the assembled **message path** you see that a message has been sent from the *SAP Fieldglass* instance `MyFieldGlass_01` to the *Cloud Integration capability of SAP Integration Suite* instance `MyCPI_01` and further to the receiver *SAP S/4HANA Cloud* instance `MyS4HANACloud_01`.
    
    In the below list you see that the message `S33GT..` is related to the integration flow *Purchase Order Status Replication from SAP S4HANA to SAP Fieldglass_ERS*. Within the list *Related Messages* you can see that two messages are related. Additional you can recognize in the highlighted columns the **order of the sent messages**

    
4. Go back to the *SAP Integration Suite Messages* page leveraging the *breadcrumb* and *click* on number of messages in **ERROR** in the *header section* for filtering the message list below. *Select* the **failed message** `1EGT...`.

    <br>![](/exercises/ex3/images/IMWorkforceCPIMessageFailed.png) 

5. In the *message details* you see that the status of message `1EGT...` has failed

    <br>![](/exercises/ex3/images/IMWorkforceMessageDetailsFailed.png)

6. In the *Related messages & exceptions* section you get some hints where to find the issue

    <br>![](/exercises/ex3/images/IMWorkforceFailedMessagePath.png)

    There is a *Java script exception* with the integration flow *Replicate Purchase Requisition from SAP Fieldglass to SAP S4HANA*. To localize the error in details you may navigate to **Cloud Integration monitoring** using the link *Local Monitoring* in section *Message Details*. 

    >
    > *Note:* As we are in a demo environment this isn't possible.
    >    
    
    
## Summary

Now you have analyzed a single message that is part of the integration scenario *ExternalWorkforce*

<br>Continue to - [Exercise 3.5 - Search for a failed message](/exercises/ex3/ex35/)
