# Exercise 3 - Central monitoring of an integration scenario end-to-end

For the following end-to-end monitoring exercise, one part of the integrated workflow of the **SAP S/4HANA Lean Procurement** has been chosen. A work order is created in SAP Fieldglass and the purchase requisition is replicated to SAP S/4HANA Cloud leveraging a prebuilt integration package (**[SAP S/4HANA Integration with SAP Fieldglass](https://api.sap.com/package/SAPS4HANAintegrationwithSAPFieldglass/overview)**) from [SAP API Business Hub](https://api.sap.com/). 

The relevant integration flows for the scenario are the following:
- [Replicate Purchase Requisition from SAP Fieldglass to SAP S4HANA](https://api.sap.com/integrationflow/Replicate_Purchase_Requisition_from_Fieldglass_to_S4HANA)
- [Purchase Order Status Replication from SAP S4HANA to SAP Fieldglass](https://api.sap.com/integrationflow/Purchase_Order_Status_Replication_from_S4HANA_to_Fieldglass)


See also the documentation of the process flow [Purchase Order and Invoicing](https://help.sap.com/docs/SAP_FIELDGLASS_INTEGRATION/bf3d1caf8c1f4f69801b37a45ac1d1b3/046b0d5f642346bd8624f1b741956585.html)

Below you see an overview of the integration scenario, relevant for this exercise.

<br>![](/exercises/ex3/images/IMDiagramFieldglassS4Int.png)

>
> *Note*: As we don’t have any chance to integrate real services in a TechEd demo environment, we have injected demo data to the SAP Cloud ALM tenant. The demo data had been extracted from a real service landscape. Therefore, you see valid data but jumping to local monitoring of the respective cloud services isn’t possible.
>

#### Prerequisites:
- You are logged in to  [SAP Cloud ALM](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home).

## Exercise steps

Run through the exercise steps in the given order.

1.	Navigate to section *SAP Cloud ALM for Operation* and open the application *Integration & Exception Monitoring*.

     <br>![](/exercises/ex1/images/CALMLandingIntExMon.png)

2. Bring the **end-to-end business scenario *ExternalWorkforce* into the scope**

   a) Select the *Scope selection* icon in the black top row

     <br>![](/exercises/ex3/images/IMScopeSelectionWorkforce.png)

   b)  Filter for *Business Services*

   c)  Click on *Go* in the upper right corner for filtering

   d)  Select the *ExternalWorkforce* scenario

   e)  Click on the button *Apply* to save the configuration

     <br>![](/exercises/ex3/images/ScopeSelectionService.png)

3.	*Recognize* that all three cloud services *SAP S/4HANA Cloud, SAP Integration Suite*, and *SAP Fieldglass* have faulty messages or an exception.

     <br>![](/exercises/ex3/images/IMWorkforce.png)

     You may also *click* on the information icon *i*. 
     
     If you want to know more about the overview page and understand the color-coding of a service's status please go through [Exercise 2.1 - Familiarize yourself with the Integration & Exception Monitoring overview page](/exercise/ex2/ex21/)

4.	*Click* on the *three dots ...* and select *Go to Details* to navigate to the **topology page**

    <br>![](/exercises/ex3/images/IMOverviewSwitchToDetails.png) 
   
5.	Oversee the numbers in the **topology view** of the *ExternalWorkforce* scenario: 29 messages have been exchanged, no exceptions have been detected, and 2 alerts have been raised

    <br>![](/exercises/ex3/images/IMWorkforceTopology.png) 

    >
    > In the *topology view* of the *Monitoring* section you see the involved services of a scenario. It offers you the collected stats within a selected time period.
    >
    > Each node represents a service. Also the border of the nodes may change depending on the status of the incoming and outgoing messages transferred and depending on the exceptions that may occur. All three services have some issues with the message exchange.
    >
   
6.	*Optionally* *click* on the SAP Fieldglass node *MyFieldGlass_01*

    <br>![](/exercises/ex3/images/IMWorkforceTopoFieldglass.png) 
    
    > *Integration & Exception Monitoring* is is retrieving monitoring information from SAP Fieldglass a webservice.

7.	*Optionally* *click* on the SAP S/4HANA Cloud node *MyS4HANACloud_01*

    <br>![](/exercises/ex3/images/IMWorkforceTopoFieldglass.png) 
    
    > *Integration & Exception Monitoring* is retrieving monitoring information from SAP S/4HANA over AIF (SAP Application Interface Framework) messages
    
8.	Click on the Cloud Integration node *MyCPI_01* and to *SAP Integration Suite Messages* on the right side to drill down to the next level, the artifacts used in Cloud Integration for this integration scenario.

    <br>![](/exercises/ex3/images/IMWorkforceTopoCPI.png) 
     
9.	*Familiarize* yourself with the **SAP Integration Suite messages** page

    <br>![](/exercises/ex3/images/IMWorkforceCPIMessages.png) 

    >
    > The message list depends on the corresponding service type, the selected business scenario and the selected time frame. 
    >
    > In case of the Cloud Integration capability of SAP Integration Suite you see beyond the message status the package name, artifact name, and other fields.
    >
    > You can see relevant integration flows relevant for the *ExternalWorkforce scenario* in the header section already:
    > - Replicate Purchase Requisition from SAP Fieldglass to SAP S4HANA
    > - Purchase Order Status Replication from SAP S4HANA to SAP Fieldglass_ERS
    > - Replicate Purchase Order from SAP Fieldglass to SAP S4HANA
    >
    >
    > Below you see the list of messages transferred in the selected time frame. Erroneous messages are highlighted in red.
    >

10.	*Click* on the first message to navigate to the **message view**. It consists of two sections:
     
     - *Click* on the first message to navigate to the **message view**

    <br>![](/exercises/ex3/images/IMWorkforceFirstMessage.png) 
   
     - *Click* on the tab *Related Messages & Exceptions* to see a **visualized message path**

    <br>![](/exercises/ex3/images/IMWorkforceMessagePath.png) 

    In this *single message details view page* you can analyze the message details and the assembled end-to-end message path.

    The message *S43..* has been sent from the *SAP Fieldglass* instance `MyFieldGlass_01` to the *Cloud Integration capability of SAP Integration Suite* instance `MyCPI_01` and further to the receiver *SAP S/4HANA Cloud* instance `MyS4HANACloud_01`.
   
     - *Click* on *Technical Correlation* to see the parameters of **SAP Passport**

    <br>![](/exercises/ex3/images/IMWorkforceSAPPassport.png)
    
    >
    > Single messages in a hybrid landscape are correlated to each other to understand the end-to-end message path. To accomplish this the **SAP Passport mechanism** is leveraged. SAP applications are using this approach to mix in a *transaction ID* and a unique *correlation ID*.
    > 
   
## Summary

You've now monitored end-to-end a message that has been sent from SAP Fieldglass to SAP S/4HANA Cloud mediated by the Cloud Integration capability of SAP Integration Suite.

Next we will search for message. Continue to - [Exercise 31](../ex31/readme.md)

<!--
<br>![](/exercises/ex2/images/02_01_0010.png)


After completing these steps you will have...

1.	Enter this code.
```abap
DATA(lt_params) = request->get_form_fields(  ).
READ TABLE lt_params REFERENCE INTO DATA(lr_params) WITH KEY name = 'cmd'.
  IF sy-subrc = 0.
    response->set_status( i_code = 200
                     i_reason = 'Everything is fine').
    RETURN.
  ENDIF.

```
-->

