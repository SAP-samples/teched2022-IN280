# Exercise 3.3 - Watch all SAP Integration Suite messages of an integration scenario

In this exercise, you will see all messages exchanged via SAP Integration Suite for the integration scenario *ExternalWorkforce* in a selected time frame

#### Prerequisites:

- You are in *topology page* of the business scenario *ExternalWorkforce* in [*Integration & Exception Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=com.sap.crun.imapp.ui#/Home)
## Exercise steps

Run through the steps in the given order

1.	Click on the Cloud Integration node `MyCPI_01` and to **SAP Integration Suite Messages** on the right side to drill down to the next level

    <br>![](/exercises/ex3/images/IMWorkforceTopoCPI.png) 
     
2.	The **SAP Integration Suite messages page** shows the exchanged messages

    <br>![](/exercises/ex3/images/IMWorkforceCPIMessages.png) 
    
    >
    > ***Note:*** This message list depends on the corresponding service type, the selected business scenario and the selected time frame. 
    > 
    
    In the header section some stats are displayed and the integration flows that are relevant for the *ExternalWorkforce scenario* show up:
    - *Replicate Purchase Requisition from SAP Fieldglass to SAP S4HANA*
    - *Purchase Order Status Replication from SAP S4HANA to SAP Fieldglass_ERS*
    - *Replicate Purchase Order from SAP Fieldglass to SAP S4HANA*

    Below you see the list of messages transferred in the selected time frame and for each message beyond the message status also the package name, artifact name, and other fields.
    
    Erroneous messages are highlighted in red. As you can see one message sent by the SAP Fieldglass instance has failed, others have completed successfully. 
    
3. *Click* on **number of messages in ERROR** in the *header section* for filtering the message list below

    <br>![](/exercises/ex3/images/IMWorkforceCPIMessageFailed.png) 

    If you want you may gain further experience in filtering messages by sender, receiver, or flows

## Summary

Now you saw all messages exchanged via *SAP Integration Suite* for the integration scenario *ExternalWorkforce*

<br>Continue to - [Exercise 3.4 - Analyze the path of a single message](/exercises/ex3/ex34/)
