# IN280 - Central monitoring of integration scenarios using SAP Cloud ALM

## Overview

As IT landscapes with cloud applications and on-premise solutions are evolving quickly it is crucial today to oversee and react on business-critical issues instantly. The Integration & Exception Monitoring application of SAP Cloud ALM helps integration experts in their daily work to centrally get an overview of exceptions and failed messages across the entire landscape. 

In this session you will get a detailed overview on the capabilities of Integration & Exception Monitoring application in SAP Cloud ALM. You will learn 
- How to navigate through the application in order to monitor and analyze integration related issues and complete end-to-end message flows, how to search specific messages via application context information, how to configure scenarios and alerts and how to use the alert inbox.

## Overview

In this session you get a deeper insight into the integration monitoring and alerting tool, how to setup and monitor end-to-end integration scenarios centrally, perform a drill-down to single message details, and navigate to the local monitoring tools for issue resolution. You learn how to configure alerts and get receive auto-notifications through email.

In this session you get a deeper insight how to monitor integration scenarios centrally in SAP Cloud ALM:

1.	How to setup secure connectivity between SAP Integration Suite and SAP Cloud ALM to enable:
    -	Integration and exception monitoring
    -	Health monitoring
2.	How monitor end-to-end integration scenarios, perform a drill-down to single message details, and navigate to the local monitoring tools for issue resolution. 
3.	You learn how to configure alerts and get receive auto-notifications through email.

## Requirements

The requirements to follow the exercises in this repository are...

## System details

For running through the exercise steps, we will provide you access to the following systems:

- SAP Cloud ALM tenant
- SAP Integration Suite tenant

The details will be provided to you by the instructors.

When you run through the exercise steps, you need to ensure that the technical IDs that you will create are unique. Hence, reuse the digital numbers of your user.

## Exercises

In the following, the complete list of exercise steps are listed. You can run through them in the given order. You can use this section as an index or table of contents. Use the breadcrumb navigation on top of the pages to go back to the Table of Contents.

- [Exercise 0 - Prerequisites and additional information](/exercises/ex0/)
    - [Exercise 0.1 - Prereq configurations in SAP Integration Suite subaccounts](/exercises/ex0/ex01/)
    - [Exercise 0.2 - Retrieve user / password](/exercises/ex0/ex02/)
- [Exercise 1 - Configure the monitoring of Cloud Integration tenant in SAP CLoud ALM](/exercises/ex1/README.md)
    - [Exercise 1.1 - Register a Cloud Integration service in LMS](/exercises/ex1/ex11/)
    - [Exercise 1.2 - Add an HTTP endpoint to a managed service](/exercises/ex1/ex12/)
    - [Exercise 1.3 - Activate data collection for the use case Integration & Exception Monitoring](/exercises/ex1/ex13/)
- [Exercise 2 - Monitoring a deployment issue](/exercises/ex2/README.md)
    - [Exercise 2.0 - Understand the integration flow that might lead to a deployment exception](/exercises/ex2/ex20/)         
    - [Exercise 2.1 - Familiarize yourself with the Integration & Exception Monitoring overview page](/exercises/ex2/ex21/)
    - [Exercise 2.2 - Activate alerts for deployment exceptions of integration artifacts](/exercises/ex2/ex22/)
    - [Exercise 2.3 - Deploy a faulty integration flow](/exercises/ex2/ex23/)
    - [Exercise 2.4 - Display the deployment exception](/exercises/ex2/ex24/)
    - [Exercise 2.5 - Watch a deployment exception in alerting](/exercises/ex2/ex25/)
    - [Exercise 2.6 - Configure the ProcessDirect channels correctly and deploy integration flow successfully](/exercises/ex2/ex26/)
    - [Exercise 2.7 - Watch the resolved deployment exception](/exercises/ex2/ex27/)
- [Exercise 3 - Central monitoring of an integration scenario ent-to-end](/exercises/ex3/)
- [Exercise 4 - Analyze exhausted resources](/exercises/ex4/)
    - [Exercise 4.1 - Understand how a tenant's health rating is calculated](/exercises/ex4/ex41/)
    - [Exercise 4.2 - Understand the Health Monitoring overview page](/exercises/ex4/ex42/)
    - [Exercise 4.3 - Details on how to work with Cloud Integration metrics](/exercises/ex4/ex43/)
    - [Exercise 4.4 - Check alerts in Health Monitoring](/exercises/ex4/ex44/)
    - [Exercise 4.5 - Activate alerts](/exercises/ex4/ex45/)
    - [Exercise 4.6 - Overwrite thresholds](/exercises/ex4/ex46/)
    - [Exercise 4.7 - Add your email address to SAP Cloud ALM](/exercises/ex4/ex47/)

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (c) 2022 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.


<!--
Provide the exercise content here directly in README.md using [markdown](https://guides.github.com/features/mastering-markdown/) and linking to the specific exercise pages, below is an example.


- [Exercise 1 - First Exercise Description](exercises/ex1/)
    - [Exercise 1.1 - Exercise 1 Sub Exercise 1 Description](exercises/ex1#exercise-11-sub-exercise-1-description)
    - [Exercise 1.2 - Exercise 1 Sub Exercise 2 Description](exercises/ex1#exercise-12-sub-exercise-2-description)
- [Exercise 2 - Second Exercise Description](exercises/ex2/)
    - [Exercise 2.1 - Exercise 2 Sub Exercise 1 Description](exercises/ex2#exercise-21-sub-exercise-1-description)
    - [Exercise 2.2 - Exercise 2 Sub Exercise 2 Description](exercises/ex2#exercise-22-sub-exercise-2-description)



**OR** Link to the Tutorial Navigator for example...

Start the exercises [here](https://developers.sap.com/tutorials/abap-environment-trial-onboarding.html).

**IMPORTANT**

Your repo must contain the .reuse and LICENSES folder and the License section below. DO NOT REMOVE the section or folders/files. Also, remove all unused template assets(images, folders, etc) from the exercises folder. 
-->
