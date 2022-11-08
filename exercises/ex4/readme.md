# Exercise 4 - Analyze Cloud Integration resources

In this exercise, you will leverage the *Health Monitoring* application of SAP Cloud ALM and track resources of Cloud Integration as JMS queues and certificates. 

#### Prerequisites:
- You are logged in to [SAP Cloud ALM](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home)
- *If you are performing configurations yourself*, your Cloud Integration service in SAP Cloud ALM `CloudIntegration-<tenant_name>_<userID>`  should be connected to the Cloud Integration tenant. If not please run through exercise [Configure the monitoring of Cloud Integration tenant in SAP Cloud ALM](../ex1/readme.md)
-  If you are using the *preconfigured Cloud Integration service* in SAP Cloud ALM `CloudIntegration-<tenant_name>` nothing has to be done

## Exercise steps

Run through the exercise steps in the given order

1.	In the home page *select* the section *SAP Cloud ALM for Operation* and *click* on the card *Health Monitoring*.

      <br>![](/exercises/ex4/images/CALMLandingHealthMon.png)

2. Bring Cloud Integration services into scope

    <br>![](/exercises/ex4/images/HMScoping.png)

    You may bring the Cloud Integration service into scope that you have registerd during configuration but also any other service is possible.

3. Familiarize yourself with the Health Monitoring **overview page** 

   This central view shows the healthiness of connected services on the level of service types, e.g. all Cloud Integration tenants. It offers a first indicator where crucial changes and adjustments are necessary.
   
   The exercise [Understand the Health Monitoring overview page](./ex41/) provides you the insights of the color-coding and functionalities this page is offering.
   
4. *Click* on the title row of the card *SAP Integration Suite (Cloud Integration)* to drill down one level down.

    <br>![](/exercises/ex4/images/HMDrillDownToType.png)

5.  The **monitoring page** offers an overview on all registered services along with number of raised alerts, the tenant health rating, and the information on data quality. If alerts exist for an instance you may jump directly to the embedded alert inbox.

    <br>![](/exercises/ex4/images/HMDrillDownToInstance.png)

    The selected Cloud Integration service has a **health percentage** of 88% and the service is rated as *Warning*.

    *Recommended but optional*: [Understand how the health rating of a service is calculated](./ex41/)

6. Click* on one of the Cloud Integration services and drill down one level to the **metric overview of a Cloud Integration service**

    >
    > This page is the centerpiece of Health Monitoring and offers a quick health overview for a particular service, in our case the selected Cloud Integration service. The grouping of available metrics is pre-configured and depends on the service type and offered metrics. Cloud Integration offers as of today the status of **JMS queue resources** and the **validity of certificates**. The default thresholds are the same as you know them from the local Cloud Integration monitoring. The blog [Centralized health monitoring of SAP Cloud Integration using SAP Cloud ALM](https://blogs.sap.com/2022/02/07/centralized-health-monitoring-of-sap-cloud-integration-using-sap-cloud-alm/) explains in detail all metrics that are available in Health Monitoring for Cloud Integration.
     >  

    <br>![](/exercises/ex4/images/HMMetricOverview.png)

    By means of **rating colors** it is easy to track all monitored metrics briefly. Any rating in red or orange attracts attention and likely will be examined more closely.

    For identification purposes of various metrics of the same type **labels** have been introduced: 

    - Each JMS queue has a label 'queue* for its name
    - Certificates have the labels *alias* and *type* for the differentiation between a certificate and a key pair

    In the lower section, one can also see also tiles for each JMS queue, titled by their label. They have own metrics and are visualized as separately: *activation status*, *queue status*, and the *number of messages*

6. Check alerts

    Check raised alerts in the alerting section and configure your managed Cloud Integration to raise the alerts while performing the steps in [Check alerts in Health Monitoring](/exercises/ex4/ex44/)

7. Customize thresholds

   a. Edit metric configuration
   
   Set threshold for cloud services, either for all metrics of a cloud service in the clouser service overview or for specific metrics after selecting the correpoind service
   
   With treshold active you can override the metric rating reported by the service by creating custom rules. Seleect the metric you want to configure
   
>
> *Important*: Health monitoring does not offer any tools to update certificates or queues directly. This is only possible in the *keystore monitor* or *manage stores monitor* of Cloud Integration itself. 
>
> With *SAP Cloud ALM* one can get an overview of the health rating of all monitored Cloud Integration services at a glance or even all connected services and systems of your IT landscape. Operation teams benefit from this overview and can concentrate their efforts on the most important tasks and do not have to inspect all local monitoring tools. And they have the possibility to navigate from the health monitoring application to the Cloud Integration monitoring.
>
   
## Summary

You've now seen that Cloud Integration can be pulled for some metrics such as JMS resources and certificates to track them. Alerts and email notifications can be activated. Once a default or custom threshold is reached the activated reaction is triggered. 

