# Exercise 1 - Configure the monitoring of Cloud Integration tenant in SAP CLoud ALM

In this exercise, we will establish an authenticated connection to a Cloud Integration tenant to get it monitored.

## Exercise steps

Run through the steps in the given order.

1. [Retrieve user / password](../ex0/ex02/) for SAP Integration Suite and SAP Cloud ALM
 
2. [Register a Cloud Integration tenant in SAP Cloud ALM](./ex11/)

3. [Add an HTTP endpoint to a managed service](./ex12/)
    
4. Activate the data collection of the selected monitoring use cases

   For *Health Monitoring* the data collection is already activated automaticalls after the creation of the HTTP endpoint.
   
   For the *Integration & Expception Monitoring* perform the steps descripbed in [Activate data collection for the use case Integration & Exception Monitoring](./ex13/)

## Summary

You've now set up the connectivity between SAP Cloud ALM monitoring use cases *Integration & Exception Monitoring* and *Health Montoring* to the a registered intance of a Cloud Integration capability of SAP Integration Suite. This is necessary to pull Cloud Integration for monitoring data.

Next we will .....Continue to - [Exercise 2](../ex2/README.md)

<!--
Provide the exercise content here directly in README.md using [markdown](https://guides.github.com/features/mastering-markdown/) and linking to the specific exercise pages, below is an example.

- [Getting Started](exercises/ex0/)
- [Exercise 1 - First Exercise Description](exercises/ex1/)
    - [Exercise 1.1 - Exercise 1 Sub Exercise 1 Description](exercises/ex1#exercise-11-sub-exercise-1-description)
-->
