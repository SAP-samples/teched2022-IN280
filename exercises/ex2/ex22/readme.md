# Activate alerts for deployment exceptions of integration artifacts

In this exercise, you will activate the **monitoring** and the **alerting** of integration exceptions for a particular Cloud Integration service. 
*This exercise is only required if you want to perform all configurations yourself.*

#### Prerequisites:

- You are in [*Integration & Exception Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=com.sap.crun.imapp.ui#/Home) and have the respective *Cloud Integration service* `CloudIntegration-<tenant_name>_<userID>` or `CloudIntegration-<tenant_name>` in scope.
- You have activited the data collection as outlined in [Exercise 1.3](/exercises/ex1/ex13/).

## Exercise steps

Run through the steps in the given order.

1. *Click* on the *three dots* and then on *Edit Configuration* on the card of the *Cloud Integration* service you have registered

   <br>![](/exercises/ex1/images/IMOverviewEditConfiguration.png)

2. *Click* on the service link or the arrow on the right side and navigate to the details of the **service configuration**

   <br>![](/exercises/ex2/images/IMExceptConfigSelectService.png)

   During setting up the service for the *Cloud Integration* tenant in the *Landscape Management Service* application we have selected three use cases. The below **two use cases** are displayed in *Integration & Exception Monitoring* as *monitoring categories*:
   - *SAP Integration Suite Messages* for **Integration Monitoring**
   - *Integration Artifact Deployments* for **Exception Monitoring**

   If there are several endpoints available *select* one.

3. *Click* on the *arrow* on the right side of the row *Integration Artifact Deployments*

   <br>![](/exercises/ex2/images/IMExceptSelectUsecase.png)

4. *Add a filter* on integration artifact deployments
	
	a. *Click* on the button *Add*
	
	b. *Specify* the name of the filter: `<userID> exceptions` while `userID` is the one provided to you
	
	c. Add an additional filter criteria: the *Artifact Name* should contain ´Hallo´. Adapt the tree fields accordingly
	
	d. *Save* the filter
	
	>
	> By means of this filter you will see exception that occur on all *Hallo World* integration flows that all participants will deploy. The filter can be adpated later to display only your exceptions.
	> 
	
	<br>![](/exercises/ex2/images/IMExceptConfigAddFilter.png)
	
5. Switch to the *Events* tab 

	<br>![](/exercises/ex2/images/IMExceptConfigSwitchToEvents.png)

6. *Add* a new *event* 

	<br>![](/exercises/ex2/images/IMExceptConfigAddEventButton.png)
	
7. *Choose* the event type **Erroneous Integration Artifact**  and *activate* the alert for the *Alerting* section by switching the *toggle* 

	<br>![](/exercises/ex2/images/IMExceptConfigActivateAlert.png)
	
8. *Save*  the configuration for this event and *close* the configuration
   

## Summary

You've now activated events and alerts for all deployment exception that might occor in the *Cloud Integration* service your have registered. Future deployment exceptions will be displayed in the *Overview* page and in the *Exception* section, alerts will be displayed in the section *Alerting*.

Go back to [Exercise 2](../../ex2/) 





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
