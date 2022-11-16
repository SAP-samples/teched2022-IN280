# IN280 - Central monitoring of integration scenarios using SAP Cloud Application Lifecycle Management (ALM)

## Overview

As IT landscapes with cloud applications and on-premise solutions are evolving quickly, it is crucial today to oversee and react to business-critical issues instantly. 
The Integration & Exception Monitoring application of SAP Cloud ALM helps integration experts in their daily work to centrally get an overview of exceptions and failed messages across the entire landscape. 
The Health Monitoring application of SAP Cloud ALM is a central place for tracking exhausting or expiring resources like certificates or JMS queues in SAP Integration Suite.

In this session you get a deeper insights on how to monitor integration scenarios centrally in SAP Cloud ALM:

- How to setup secure connectivity between SAP Integration Suite and SAP Cloud ALM to enable integration, exception and health monitoring  centrally
- How to navigate through the applications in order to monitor and analyze integration specific issues, and jump context-sensitive to the local monitoring for issue resolution
- How to monitor end-to-end integration scenarios, perform a drill-down to single message details
- How to track exhausting resources like JMS queues or expiring certificates
- How to activate alerts, track them, and receive auto-notifications through email

## Requirements

There are no prior requirements to this exercise. You can perform this even if you do not have any experience with integration or Cloud ALM platform from SAP. However, you will be able to derive increased value from this session if you have some knowledge on what SAP Integration Suite is all about and how it helps with enterprise-wide integration needs.

You can check out the following material:

- SAP Discovery Center mission that helps you to [Get Started with Integration Suite](https://discovery-center.cloud.sap/protected/index.html#/missiondetail/3258/3327)

- SAP Community blog posts [Central monitoring of integration scenarios](https://blogs.sap.com/2021/12/21/central-monitoring-of-integration-scenarios-using-sap-cloud-alm/) and [Centralized health monitoring of SAP Cloud Integration using SAP Cloud ALM](https://blogs.sap.com/2022/02/07/centralized-health-monitoring-of-sap-cloud-integration-using-sap-cloud-alm/)

- List of supported products and how to setup: [SAP Cloud ALM for Operations - Expert Portal](https://support.sap.com/en/alm/sap-cloud-alm/operations/expert-portal.html)

## System details

For running through the exercise steps, we will provide you access to the following systems:

- [System landscape](/exercises/ex0/README.md)
- [Access information](/exercises/ex0/ex02)

When you run through the exercise steps, you need to ensure that the technical IDs that you will create are unique. Hence, reuse your user ID.

## Exercises

If you want to do configuration steps by yourself and register a *Cloud Integration service* in SAP Cloud ALM, please start with [Exercise 1](/exercises/ex1/README.md)</br>
If you want to reuse pre-configured services in SAP Cloud ALM start with [Exercise 2](/exercises/ex2/README.md)

<br>![](/exercises/ex0/images/IN280Exercises.png)

The Exercises 2, 3, and 4 are independent from each other. 

The complete list of exercises are listed below. You can run through them in the given order and can use this section as table of contents. <br/>
Kindly use the breadcrumb navigation on top of the pages to come back to this section.

- [Exercise 1 - Register a self-managed Cloud Integration service in SAP CLoud ALM](/exercises/ex1/README.md)
    - [Register a Cloud Integration service in LMS](/exercises/ex1/ex11/)
    - [Add an HTTP endpoint to a managed service](/exercises/ex1/ex12/)
    - [Activate data collection for the use case Integration & Exception Monitoring](/exercises/ex1/ex13/)
- [Exercise 2 - Monitoring a deployment exception](/exercises/ex2/README.md)
    - [Scenario introduction](/exercises/ex2/ex20/)
    - [Bring a Cloud Integration service into scope](/exercises/ex2/ex21/)
    - [Familiarize yourself with the Integration & Exception Monitoring overview page](/exercises/ex2/ex22/)    
    - [Add your email address to SAP Cloud ALM](/exercises/ex2/ex23/) 
    - [Activate alerts for deployment exceptions of integration artifacts](/exercises/ex2/ex24/)
    - [Deploy a misconfigured integration flow](/exercises/ex2/ex25/)
    - [Display the deployment exception](/exercises/ex2/ex26/)
    - [Check a deployment exception alert](/exercises/ex2/ex27)
    - [Configure the ProcessDirect channels correctly](/exercises/ex2/ex28/)
    - [Check the resolved deployment exception](/exercises/ex2/ex29/)
    - [Search for customer header properties](/exercises/ex2/ex210/)
    - [Check the inbox for email notifications](/exercises/ex2/ex211/)
- [Exercise 3 - End-to-end monitoring of an integration scenario](/exercises/ex3/)
    - [Scenario introduction](/exercises/ex3/ex30/)
    - [Bring a business scenario into scope](/exercises/ex3/ex31)
    - [Overview on business scenario topology](/exercises/ex3/ex32)
    - [Watch all SAP Integration Suite messages of an integration scenario](/exercises/ex3/ex33/)
    - [Analyze the path of a single message](/exercises/ex3/ex34)
    - [Search for a failed message](/exercises/ex3/ex35)
    - [Check failed message alerts](/exercises/ex3/ex36)
- [Exercise 4 - Health monitoring of Cloud Integration resources](/exercises/ex4/readme.md)
    - [Scenario introduction](/exercises/ex4/ex40)
    - [Bring a Cloud Integration service into scope](/exercises/ex4/ex41)
    - [Health overview of IT landscape](/exercises/ex4/ex42)
    - [Health overview of all Cloud Integration services of SAP Integration Suite](/exercises/ex4/ex43)
    - [Calculation of a service's health rating](/exercises/ex4/ex44)
    - [Monitored metrics of Cloud Integration](/exercises/ex4/ex45)
    - [Details on metric page](/exercises/ex4/ex46/)
    - [Activate alerts](/exercises/ex4/ex47/)
    - [Check alerts in Health Monitoring](/exercises/ex4/ex48/)

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (c) 2022 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
