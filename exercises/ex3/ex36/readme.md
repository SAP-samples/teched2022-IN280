# Exercise 3.6 - Check failed message alerts

In this exercise, you will watch alerts that have been raised for failed messages

#### Prerequisites:

- You are in [*Integration & Exception Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=com.sap.crun.imapp.ui#/Home) and have the integration scenario *ExternalWorkforce* in scope

## Exercise steps

Run through the steps in the given order

1. *Click* on the *exclamation mark* icon **!** in the left-side navigation and navigate to the **Alerting page**

2. *Select* the **Erroneous CPI Messages Detected(Grouped)** alert for the *Cloud Integration service* `MyCPI_01`

    <br>![](/exercises/ex3/images/IMWorkforceAlertingFailedMessage.png)
    
    Highlighted you see some information from SAP Integration Suite, mainly in related integration flow of this erroneous message. Also the SAP Fiedglass tenant has sent an error message and with that raised an alert 

2. In the **alert details page** you see all failed messages grouped together for the integration flow *Replicate Purchase Requisition from SAP Fieldglass to SAP S4HANA*.

    <br>![](/exercises/ex3/images/IMWorkforceAlertingFailedMessageDetails.png)

    You may navigate directly to the *message details page* using the *Message ID* `1EGT0e1kEW2C6kPVvE3GCitCRHyw` link
    
## Summary

Now you have seen how a failed message alert appears in the *alerting section* of *Integration & Exception Monitoring*

<br>Congratulation. You have finalized Exercise 3. Continue to [Exercise 4](/exercises/ex4/readme.md)
