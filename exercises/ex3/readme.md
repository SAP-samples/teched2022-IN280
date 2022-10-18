# Exercise 3 - Central monitoring of an integration scneario end-to-end

For the following end-to-end monitoring exercise, one part of the integrated workflow of the SAP S/4HANA Lean Procurement has been chosen. A work order is created in SAP Fieldglass and the purchase requisition is replicated to SAP S/4HANA Cloud leveraging the prebuilt integration package on : **[SAP S/4HANA Integration with SAP Fieldglass](https://api.sap.com/package/SAPS4HANAintegrationwithSAPFieldglass/overview)** from [SAP API Business Hub](https://api.sap.com/). 

The relevant integration flows for the scenario are the following:
- [Replicate Purchase Requisition from SAP Fieldglass to SAP S4HANA](https://api.sap.com/integrationflow/Replicate_Purchase_Requisition_from_Fieldglass_to_S4HANA)
- [Purchase Order Status Replication from SAP S4HANA to SAP Fieldglass](https://api.sap.com/integrationflow/Purchase_Order_Status_Replication_from_S4HANA_to_Fieldglass)


See also the documentation of the process flow [Purchase Order and Invoicing](https://help.sap.com/docs/SAP_FIELDGLASS_INTEGRATION/bf3d1caf8c1f4f69801b37a45ac1d1b3/046b0d5f642346bd8624f1b741956585.html)

Below you see an overview of this integration scenario.

<br>![](/exercises/ex3/images/IMDiagramFieldglassS4Int.png)

>
> As we don’t have any chance to provide real services, we have injected demo data to your SAP Cloud ALM tenants that was been extracted from a real service landscape. Therefore, jumping to local monitoring to the respective cloud services isn’t possible.
>

#### Prequisites:
- You are logged in to the [SAP Cloud ALM tenant](https://teched22-cloudalm-003.authentication.eu10.hana.ondemand.com/login).

## Exercise steps

Run through the exercise steps in the given order.

1.	Navigate to section *SAP Cloud ALM for Operation* and click on the card *Integration & Exception Monitoring*.

     <br>![](/exercises/ex1/images/CALMLandingIntExMon.png)

2. Bring the **end-to-end business scenario into the scope**

   a) Select the *Scope selection* icon in the black top row

     <br>![](/exercises/ex3/images/IMScopeSelectionWorkforce.png)

   b)  Filter for *Business Services*

   c)  Click on *Go* in the upper right corner for filtering

   d)  Select the *ExternalWorkforce* scenario

   d)  Click on the button *Apply* to save the configuration

     <br>![](/exercises/ex3/images/ScopeSelectionService.png)

3.	*Optionally* you may *add* this scenario to your *favorites*

     <br>![](/exercises/ex3/images/IMWorkforceFavourite.png) 

4.	*Click* on the information icon **(i)** and understand the color coding of a service’s status

   >
   > Each card in the overview page represents a service or a business scenario. The left-side color reflects the overall status for the selected time.
   >

   <br>![](/exercises/ex3/images/IMOverviewCardInfo.png) 
   
   All three cloud services *SAP S/4HANA Cloud, SAP Integration Suite*, and *SAP Fieldglass* have faulty messages or an exception

5.	*Click* on the three dots and select *Go to Details* to navigate to the **topology page**

   <br>![](/exercises/ex3/images/IMOverviewSwitchToDetails.png) 
   
6.	Oversee the numbers in the **Topology view**: 36 messages have been exchanged, more than 100 exceptions detected, and 5 alerts has been raised

   <br>![](/exercises/ex3/images/IMWorkforceTopology.png) 
   
   >
   > In the *topology view* of the *Monitoring* section you see the involved services of a scenario. It offers you the collected stats of the selected time period.
   >
   > Each node represents a service. Again, the node border changes the color depending on the status of the incoming and outgoing messages transferred or depending on the occurred exceptions. All three services have some issues with the message exchange.
   >
   
7.	*Optionally* *click* on the SAP Fieldglass node *MyFieldGlass_01*

   <br>![](/exercises/ex3/images/IMWorkforceTopoFieldglass.png) 
   
8.	Click on the Cloud Integration node *MyCPI_01* and to messages on the right side to drill down to the next level, the artifacts used in Cloud Integration for this integration scenario.

   <br>![](/exercises/ex3/images/IMWorkforceTopoCPI.png) 
   
9.	....

   <br>![](/exercises/ex3/images/IMWorkforceTopoS4.png) 
    
10.	Use the *arrow* on the right of the first interface to drill down to the next level of information, the **interface list**

   <br>![](/exercises/ex3/images/IMWorkforceCPIInterfaceList.png) 
   
   All relevant integration flows of Cloud Integration relevant for the selected business scenario are listed.
   
11.	*Optionally* adapt the message list as per your needs

   <br>![](/exercises/ex3/images/IMWorkforceMessageListAdapt.png) 
   
   The message level page lists all messaging for a particular interface. The erroneous messages are highlighted in red.

   The message list depends on the corresponding service type. In case of the Cloud Integration capability of SAP Integration Suite you see beyond the message status the package name, artifact name, and other fields.

   
12.	*Click* on the first message .....

   <br>![](/exercises/ex3/images/IMWorkforceFirstMessage.png) 
   
   Text
   
13.	*Scroll down* to the *Related Messages & Exceptions* section to see the visualized message path

   <br>![](/exercises/ex3/images/IMWorkforceFirstMessage.png) 
   
   In this *single message details view page* you can analyze the message details and the assembled end-to-end message path.
   
   The message *S43..* has been sent from the *SAP Fieldglass* instance `MyFieldGlass_01` to the *Cloud Integration capability of SAP Integration Suite* instance `MyCPI_01` and further to the receiver *SAP S/4HANA Cloud* instance `MyS4HANACloud_01`.
   
14.	*Click* on *Technical Correlation* to see the parameters of **SAP Passport**

   <br>![](/exercises/ex3/images/IMWorkforceSAPPassport.png) 
   
   Single messages in the hybrid landscape are correlated to each other to an end-to-end message flow. To accomplish this the **SAP Passport mechanism** is leveraged. SAP applications are using this approach to mix in a *transaction ID* and a unique *correlation ID*.
   
   
   
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

