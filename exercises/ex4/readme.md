# Exercise 4 - Analyze Cloud Integration resources

In this exercise, you will leverage the *Health Monitoring* application of SAP Cloud ALM and track resources of Cloud Integration as JMS queues and certificates. 

#### Prerequisites:
 - You are logged in to [SAP Cloud ALM](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home)
 - :construction_worker: *If you have a self-managed `CloudIntegration-<tenant_name>-<userID>` service* it should be connected to the Cloud Integration tenant. If not please run through exercise [Configure the monitoring of Cloud Integration tenant in SAP Cloud ALM](/exercises/ex1/)


## Exercise steps

Run through the exercise steps in the given order

[Scenario introduction](/exercises/ex4/ex40)

1. [Bring a Cloud Integration service into scope](/exercises/ex4/ex41)

2. [Familiarize yourself with the Health Monitoring overview page](/exercises/ex4/ex42)

3. [Get an overview of all Cloud Integration tenants of SAP Integration Suite](/exercises/ex4/ex43)

4. *Optional:* [Understand how the health rating of a service is calculated](/exercises/ex4/ex44)

5. [Get an overview on monitored metrics of a Cloud Integration service](/exercises/ex4/ex45)

6. *Optional:* [Details on how to work with Cloud Integration metrics](/exercises/ex4/ex46/)

7. *If you are performing configurations yourself:* [Activate alerts](/exercises/ex4/ex47/)

8. [Check alerts in Health Monitoring](/exercises/ex4/ex48/)

9. [Overwrite thresholds](/exercises/ex4/ex49/)
   
>
> *Important*: Health monitoring does not offer any tools to update certificates or queues directly. This is only possible in the *keystore monitor* or *manage stores monitor* of Cloud Integration itself. 
>
> With *SAP Cloud ALM* one can get an overview of the health rating of all monitored Cloud Integration services at a glance or even all connected services and systems of your IT landscape. Operation teams benefit from this overview and can concentrate their efforts on the most important tasks and do not have to inspect all local monitoring tools. And they have the possibility to navigate from the health monitoring application to the Cloud Integration monitoring.
>
   
## Summary

You've now seen that Cloud Integration can be pulled for some metrics such as JMS resources and certificates to track them. Alerts and email notifications can be activated. Once a default or custom threshold is reached the activated reaction is triggered. 

