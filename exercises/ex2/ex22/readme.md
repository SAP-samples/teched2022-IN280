# Exercise 2.2 - Familiarize yourself with the Integration & Exception Monitoring overview page

The overview page offers a **central view** that shows the status of integration scenarios and services that are in scope. It provides a first indicator where faulty messages or in case of Cloud Integration deployment exceptions occurred. In this exercise, you will get insights of the used color-coding and the functionalities this page is offering. 

*All these steps are optional and only for your information.* You may jump directly to [Exercise 2.3](/exercises/ex2/ex23/)

>
> **The below screenshots you can't see in our TechEd IN280 SAP Cloud ALM tenant. They are captured from another demo tenant but provides you an idea how an IT landscape could look like**
>

**Note:** Each card in the overview page represents a **service** or a **business scenario**. The left-side color reflects the overall status for the selected time.
You may identify the scenarios by the boxes of the involved services
The screenshot below is taken from a demo tenant and shows an extended view covering a mix of business services and cloud services partially out of scope for the IN280 hands-on. <br>

In the screenshots below we are focusing on the card of the business scenario *ExternalWorkforce*. **During the exercise you may try it out with one of the Cloud Integration service you have in your scope**

<br>![](/exercises/ex2/images/IMOverviewpageDetails.png)

1. *Click* on the *quality icon* and check whether the **data collection** is running successfully for the involved services.

    Within the popup that shows up *click* on the **Cloud Integration service**. The status of monitoring messages and integration artifact exceptions is displayed separately from each other.

    <br>![](/exercises/ex2/images/IMDataQuality.png)

2. In case of raised alerts you would be able to jump directly to the embedded **alerting** by clicking on the *number of alerts* in the footer of each card

3. *Check* the **status of business service events** with the time-calendar-icon

    It shows the events from the **Cloud Availability Center**. If a maintenance, disruption or degradation events raise up for a service it will be displayed here.

4. *Click* on the *Star* icon to set an entry to your **favorite** ones and track them more easily also in cases there are **not selected to your scope**

5. *Click* on the *information* icon **(i)** and get an understanding of the **color-coding** of a service's status
    
    The color of the left side of each card is the overall status of the integration scenario or the service. It depends on the selected time frame.

    Inside of a card you may distinguish:
    - In case of monitoring a single cloud service the status of monitoring messages is separated from monitoring exceptions. Clicking on the red bar you may get directly to the list of faulty messages. Same for the others. 
    - In case of monitoring an integration scenario you see the status of each involved service by it's color

    <br>![](/exercises/ex2/images/IMOverviewInfoButton.png)

       
## Summary

Now you have understood the color-coding the Integration & Exception Monitoring is using and the functionalities the overview page is offering.

<br>Continue to - [Exercise 2.3 - Activate alerts for deployment exceptions of integration artifacts](/exercises/ex2/ex23/)



