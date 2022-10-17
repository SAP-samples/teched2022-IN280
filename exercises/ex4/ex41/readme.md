# Understand metric ratings

This section servies for your understanding how the rating of a tenant's health is calculated in the Health Monitoring use case of SAP Cloud ALM.

The technical metrics from a monitored services can be used to calculate the overall health of a monitored service. E.g. Cloud Integration is pulled every 5 minutes.

Each service type offers its own metrics and ratings to Cloud ALM. 
<br>E.g. Cloud Integration offers exhaustion of JMS resources and expiry of certificates. On the other hand a SAP Integration Business Planning service offers metrics such as Active Users in a ABAP system or Delayed application jobs.

The service health is **calculated bottom up**: each metric, as a specific certificate validity or the activation status of a JMS (Java Messaging Service) queue, gets rated individually. 

Thresholds define when a metric receives a certain rating, such as *OK* or *Critical*. The metric rating is mapped to a metric health score to automate the calculation of the overall service’s health score. 

The health score of the overall service is determined by the mean score of all individual metrics. A service health percentage of less than 100% determines a service as in Warning, with less than 80% as in *Critical* state. And as soon as one metric is rated as Fatal the entire service has a health score of 0% and is in *Critical* state.

<br>![](/exercises/ex4/images/HMRatingDiagram.png)

Some metrics have only **informative** character, such as the total number of messages in a JMS queue. They are not included in the health calculation of a service.

*Example:* A Cloud Integration tenant offers 41 metrics. 3 metrics have only informative values and are not counted. Therefore only 38 are relevant for the calculation.
Sum up 10 metrics in *Critical* state mapped to a score of 0%, 1 in *Warning* 50%, and 27 with *Ok* 100%, the sum is 27,5 divided by 38, and rounded. 
<br>This results to a service health percentage of 72% and the service is rated as *Critical*.

<br>![](/exercises/ex4/images/HMRatingExample.png)

Continue to the main page of [Exercise 4](../../ex4/)

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

