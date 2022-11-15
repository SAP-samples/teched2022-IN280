# Exercise 3.2 - Overview on business scenario topology

In this exercise, you get an understanding of the topology of the selected integration scenario *ExternalWorkforce*. You see the sender `MyFieldglass_01`, the receiver `MyS4HANACloud_01`and the integration platform in the middle `MyCPI_01`. The view shows the number of exchanged messages and occurred exceptions. As alerts had been activated already, also the number of alerts are listed.

#### Prerequisites:

- You are in *overview page* of [*Integration & Exception Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=com.sap.crun.imapp.ui#/Home) and have the integration scenario *ExternalWorkforce* in scope

## Exercise steps

Run through the steps in the given order

1.	*Click* on the *three dots* and select **Go to Details** 

    <br>![](/exercises/ex3/images/IMOverviewSwitchToDetails.png) 

2.	Oversee the numbers in the **topology view** of the *ExternalWorkforce* scenario: 29 messages have been exchanged, no exceptions have been detected, and 2 alerts have been raised

    <br>![](/exercises/ex3/images/IMWorkforceTopology.png) 

    >
    > In the *topology view* of the *Monitoring* section you see the involved services of a scenario. It offers you the collected stats within a selected time period.
    >
    > Each node represents a service. Also the border of the nodes may change depending on the status of the incoming and outgoing messages transferred and depending on the exceptions that may occur. All three services have some issues with the exchanged messages.
    >

3.	*Optionally* *click* on the SAP Fieldglass node `MyFieldGlass_01`

    <br>![](/exercises/ex3/images/IMWorkforceTopoFieldglass.png) 

    *Integration & Exception Monitoring* is retrieving monitoring information from SAP Fieldglass through a webservice.

4.	*Optionally* *click* on the SAP S/4HANA Cloud node `MyS4HANACloud_01`

    <br>![](/exercises/ex3/images/IMWorkforceTopoS4.png) 

    *Integration & Exception Monitoring* is retrieving monitoring information from SAP S/4HANA over AIF (SAP Application Interface Framework) messages

5.	Click on the Cloud Integration node `MyCPI_01`

    <br>![](/exercises/ex3/images/IMWorkforceTopoCPI.png) 
   
    The Cloud Integration capability of SAP Integration Suite is pulled every 5 minutes via an internal OData API. 

## Summary

Now you got an understanding of the topology of the selected integration scenario *ExternalWorkforce*.

<br>Continue to - [Exercise 3.3 - Watch all SAP Integration Suite messages of an integration scenario](/exercises/ex3/ex33/)
