# Activate alerts for deployment exceptions for integration artifacts

In this exercise, you will activate the alerting for a particular Cloud Integration service to get an alert once a deployment exception happens

###
Prerequisites:
......

## Exercise steps

Run through the exercise steps in the given order.

1. *Activate data collection if not already done

    The card for your registered *Cloud Integration* service likely doesn't collect no data so far
    
   <br>![](/exercises/ex2/images/IMOverviewNoData.png)

    a. *Click* on the *three dots* and then on *Edit Configuration*
    
    <br>![](/exercises/ex2/images/IMOverviewEditConfiguration.png)
    
    b. *Switch on* the data collection using the *toggle button*, save the configuration, and close the dialog
    
    <br>![](/exercises/ex2/images/IMConfigDataCollection.png)
	
    c. Proof whether the data collection is running successfully
    
    <br>![](/exercises/ex2/images/IMOverviewDataCollectionActivated.png)

2. *Click* on the *three dots* and then on *Edit Configuration* the *Cloud Integration* service you have registered

   <br>![](/exercises/ex2/images/IMOverviewEditConfiguration.png)

2. *Click* on the service link or the arrow on the right side and navigate to the details of the **service configuration**

   <br>![](/exercises/ex2/images/IMExceptConfigSelectService.png)

   During setting up the service for the *Cloud Integration* tenant *Landscape Management Service* we have selected several use cases. These two use cases are displayed here as *monitoring categories*:
   - *SAP Integration Suite Messages* for *Integration Monitoring*
   - *Integration Artifact Deployments* for *Exception Monitoring*

   If there are several endpoints available you *select* one.

3. *Click* on the *arrow* on the right side of the row *Integration Artifact Deployments*

   <br>![](/exercises/ex2/images/IMExceptSelectUsecase.png)

4. *Add a filter* on integration artifact deployments that might occur
	
	a. *Click* on the button *Add*
	
	b. *Specify* a filter name: `<userID> exceptions` while `userID` is the one provided you by the Tenant Booker application.
	
	c. Add an additional filter criteria: the *Artifact Name* should contain the world *Hallo*. Adapt the tree fields accordingly
	
	d. *Save* the filter
	
	<br>![](/exercises/ex2/images/IMExceptConfigAddFilter.png)
	
5. Switch to the *Events* tab 

	<br>![](/exercises/ex2/images/IMExceptConfigSwitchToEvents.png)

6. Use the switch button to *activate* the event *Erroneous Integration Artifact*, *save* the configuration for this event, and *switch* to the *Events Details*

	<br>![](/exercises/ex2/images/IMExceptConfigActivateEvent.png)
	
7. *Activate* the alert for the *Alerting* section by switching the *toggle* 

	<br>![](/exercises/ex2/images/IMExceptConfigActivateAlert.png)
	
6. *Save* and *close* the configuration
   

## Summary

You've now activated events and alerts for all deployment exception that might occor in the *Cloud Integration* service your have registered. Future deployment exceptions will be displayed in the *Overview* page and in the *Exception* section, alerts will be displayed in the section *Alerting*.

Go back to [Exercise 4](../../ex4/readme.md)





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
