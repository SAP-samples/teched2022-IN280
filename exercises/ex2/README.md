# Exercise 2 - Monitoring a deployment issue

In this exercise, we will get experience with an integration flow that cannot be deployed. The deployment exception will be displayed in *Integration & Exception Monitoring*. 

#### Prerequisites:

- You are logged in to [SAP Cloud ALM](https://teched22-cloudalm-003.authentication.eu10.hana.ondemand.com/) and to the respective SAP Integration Suite tenant you have been assigned to (see Tenant Booker application)
- *If you want to perform configurations yourself:* your Cloud Integration service in SAP Cloud ALM has to connected to the real Cloud Integration tenant. If not please run through exercise [Configure the monitoring of Cloud Integration tenant in SAP CLoud ALM](../ex1/readme.md).

## Exercise steps

Run through the steps in the given order.

1.	Navigate to section *SAP Cloud ALM for Operation* and click on the card *Integration & Exception Monitoring*.

     <br>![](/exercises/ex1/images/CALMLandingIntExMon.png)

2. Bring the *Cloud Integration* service that you have registered **into scope**

   a) Select the *Scope selection* icon in the black top row

     <br>![](/exercises/ex2/images/ScopeSelectionService.png)

   b)  Filter for *Services*

   c)  Click on *Go* in the upper right corner for filtering

   d)  Select the *Cloud Integration* service that you have registered in Exercise ....

   e)  Click on the button *Apply* to save the configuration

     <br>![](/exercises/ex2/images/ScopeSelectionService.png)

3.	Familiarize yourself with the **Integration & Exception Monitoring overview page**

     This central view shows the status of integration scenarios and services in scope or set to favorites. It offers a first indicator where faulty messages or in case of Cloud Integration deployment exceptions of integration artifacts occurred.

     The exercise [Understand the Integration & Exception Monitoring overview page](./ex21/readme.md) provides you the insights of the color-coding and functionalities this page is offering.
       
5. *If you perform configurations yourself* [Activate alerts for deployment exceptions of integration artifacts](./ex22/readme.md)

5. [Deploy faulty integration flow](./ex23/readme.md)

6. [Understand the integration flow that might lead to a deployment exception](./ex20/readme.md)

7. [Display the deployment exception](./ex24/readme.md) in SAP Cloud ALM

8. [Watch a deployment exception in altering](/exercises/ex2/ex25)

8. [Configure the ProcessDirect channels correctly and deploy integration flow successfully](./ex26/)

9. [Watch the resolved deployment exception](./ex27/) in the SAP Cloud ALM

## Summary

You've now seen that ...


<!--
## Exercise 2.1 Sub Exercise 1 Description

After completing these steps you will have created...

1. Click here.
<br>![](/exercises/ex2/images/02_01_0010.png)

2.	Insert this line of code.
```abap
response->set_text( |Hello ABAP World! | ). 
```

## Exercise 2.2 Sub Exercise 2 Description

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


## Summary

You've now ...

Continue to - [Exercise 3](../ex3/README.md)
