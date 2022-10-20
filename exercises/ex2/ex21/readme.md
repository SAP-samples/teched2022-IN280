# Understand the Integration & Exception Monitoring overview page

In this exercise, you will understand which information you may retrieve from the overpage page of Integration & Exception Monitoring.

All these steps are optional and only for your information.

*Note*: The screenshot below is taken from a demo tenant and shows an extended view covering a mix of business services and cloud services partically out of scope for these exercises. <br>

Focus on the Card *ExternalWorkforce*.

<br>![](/exercises/ex2/images/IMOverviewpageDetails.png)

a. *Click* on the *quality icon* and check whether the **data collection** is running successfully for the involved services.

   *Click* on the *Cloud Integration* service ´H2RCPI`. The status of monitoring messages and integration artifact exceptions is displayed seperately.

   <br>![](/exercises/ex2/images/IMDataQuality.png)

b. In case of raised alerts you would be able to jump directly to the embedded **alerting**

c. *Check* the **status of business service events** with the time-calender-icon

   It shows the events from the Cloud Availability Center. If a maintenance, disruption or degradation events raise up for a service it will be displayed here.

d. *Click* on the *Star* icon to set an entry to your **favorite** ones and track them more easily also in cases there are **not selected to your scope**

e. *Click* on the *info* icon and get an understanding of the color-coding on this page

   The color of the left side of each card is the overall status of the integration scenario or the service. It depends on the selected time frame.
   
   Inside of a card you may distinguish:
   - In case of monitoring a single cloud service the status of monitoring messages is separated from monitoring exceptions. Clicking on the red bar you may get directly to the list of faulty messages. Same for the others. 
   - In case of monitoring an integration scenario you see the status of each involved service by it's color

   <br>![](/exercises/ex2/images/IMOverviewInfoButton.png)

<br><br><br>Go back to the main [Exercise 2](../../ex2/readme.md)





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

