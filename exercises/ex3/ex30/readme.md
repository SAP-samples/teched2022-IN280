# Scenario introduction: Central monitoring of an integration scenario end-to-end

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


<br>Start with - [Exercise 3.1 - Bring a business scenario into scope](/exercises/ex3/ex31/)
