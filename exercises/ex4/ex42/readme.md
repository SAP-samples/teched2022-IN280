# Available metrics for Cloud Integration

In this exercise, we will ...

## Exercise steps

Run through the exercise steps in the given order.

#### Prequisites:
The Cloud Integration tenant is already registered. If not please run through exercises [Register a Cloud Integration tenant in LMS](../ex11/).

If not already done, please login to [SAP Cloud ALM tenant](https://teched22-cloudalm-003.authentication.eu10.hana.ondemand.com/).  

1.	Navigate t...

   <br>![](/exercises/ex1/images/CALMLandingHealthMon.png)
   
We have talked about metrics in general long enough. In the following, one can see the ones currently available for Cloud Integration together with the default thresholds that are defining the metrics ratings. (See also the column value in picture All metrics view). In case of the Cloud Integration capability of SAP Integration Suite, as of today the status of JMS queue resources, used for asynchronous messaging scenarios, and the validity of certificates and key pairs is monitored. The thresholds are the same as you know them from the local Cloud Integration monitoring, only the thresholds names differ.

Certificate validity: shows the remaining days until the certificate or key pair expires. There is no differentiation between keystore items provided by SAP or owned by customers. As default the metric is rated as Ok as long the validity is more than 30 days and then switches to Warning. If the certificate expires in less than 7 days, the rating is Critical. See Security artifact renewal in case of an upcoming expiration.

JMS resources:

Number of JMS queues shows the total number of used queues in relation to the limit (default: 30). It is rated as Critical if only one or no queue remains. The maximum message queues can be configured on the tenant. Read the blog for further information.
JMS queue capacity shows the total queue capacity in relation to the total available storage for JMS resources. If the MBs already in use reaches 80% of the total capacity available, the status will change to Warning, and if it reaches 95% the status will change to Critical.
JMS queue consumers, producers, transactions metrics are rated as Ok if any consumer, producer, or transaction are available.
The following three metric types are available for each JMS queue but additionally also as a separate one summarizing all JMS resources for the tenant:

JMS queue active shows whether a queue has been started or stopped.
JMS queue status: as a JMS queue consists of three sub-queues for processing a JMS message (main processing, storage for a retry in case of an error, and storage for chunks in case of large messages) the status depends on the usage of these sub-queues. If at least the usage of one sub-queue is 95% of the max capacity the JMS queue changes to the state Critical, between 80% and 95% in Warning and above in state Ok. In case a queue is stopped, Critical is reported along with text ‘Queue stopped’.
The summarizing status metric across all JMS queues goes to Critical if at least one of the JMS queues has status Critical, the same holds for
JMS queue message shows the total amount of messages in a queue. This metric is for information purposes only and is not counted in the overall service health score.




## Summary

You've now ...

Next we will ....... Continue to - [Exercise 5](../ex5/README.md)





<!--
# Available metrics for Cloud Integration

In this exercise, we will ...

## Exercise steps

Run through the exercise steps in the given order.

#### Prequisites:
The Cloud Integration tenant is already registered. If not please run through exercises [Register a Cloud Integration tenant in LMS](../ex11/).

If not already done, please login to [SAP Cloud ALM tenant](https://teched22-cloudalm-003.authentication.eu10.hana.ondemand.com/).  

1.	Navigate t...

   <br>![](/exercises/ex1/images/CALMLandingHealthMon.png)
   
    >
    > *Important:*
    > Health monitoring do.....
    >

## Summary

You've now ...
After completing these steps you will have created...

Next we will ....... Continue to - [Exercise 5](../ex5/README.md)


2.	Insert this line of code.
```abap
response->set_text( |Hello ABAP World! | ). 
```

-->
