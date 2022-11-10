# Exercise 1 - Configure the monitoring of Cloud Integration tenant in SAP CLoud ALM

In this exercise, we will establish an authenticated connection to a Cloud Integration tenant to get it monitored.

:warning: This exercise is not necessary to perform the exercises of IN280. Instead it is targeted to those attendees who would like to understand how to setup an authenticated connectivity to SAP Integration Suite. If you are not interested in the configuration you can use a pre-configured *Cloud Integration* service and jump directly to [Exercise 2](../ex2/README.md)

## Exercise steps

Run through the steps in the given order.

1. [Register a Cloud Integration service in LMS](./ex11/)

2. [Add an HTTP endpoint to a managed service](./ex12/)
    
3. [Activate data collection for the use case Integration & Exception Monitoring](./ex13/)

   For *Health Monitoring* the data collection is already activated automaticalls after the creation of the HTTP endpoint.

## Summary

You've now set up the connectivity between SAP Cloud ALM monitoring use cases *Integration & Exception Monitoring* and *Health Montoring* to the a registered intance of a Cloud Integration capability of SAP Integration Suite. This is necessary to pull Cloud Integration for monitoring data.

Next we will get experience with an integration flow that cannot be deployed. Continue to - [Exercise 2](../ex2/README.md)

<!--
Provide the exercise content here directly in README.md using [markdown](https://guides.github.com/features/mastering-markdown/) and linking to the specific exercise pages, below is an example.

- [Getting Started](exercises/ex0/)
- [Exercise 1 - First Exercise Description](exercises/ex1/)
    - [Exercise 1.1 - Exercise 1 Sub Exercise 1 Description](exercises/ex1#exercise-11-sub-exercise-1-description)
-->
