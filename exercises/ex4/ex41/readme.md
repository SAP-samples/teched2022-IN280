# Understand ratings in Health Monitoring

In this exercise, we will understand 



The instance CALM-IntSuite-EU10 is rated as Warning with a high score of 92%. For this calculation 58 metrics are used. 13 metrics have only informative value and are not counted. 4 metrics are in Critical state and don’t get any metric high score. 41 out of 58 are Ok with 100%. The sum up divided by the relevant (58-13) metrics leads to a service rating score of 92%. The tenant is rated as Critical. 


## Summary

You've now ...

Continue to the main page of - [Exercise 4](../../ex4/)

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

