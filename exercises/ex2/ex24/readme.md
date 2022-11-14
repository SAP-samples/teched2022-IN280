# Exercise 2.4 - Activate alerts for deployment exceptions of integration artifacts

In this exercise, you will activate the **alerting** of integration exceptions for a particular *Cloud Integration service*. 

 :heavy_exclamation_mark: *This exercise is only relevant if you are configuring a self-managed `CloudIntegration-<tenant_name>-<userID>` service*. If you use a preconfigured *Cloud Integration service* you can jump directly to - [Exercise 2.4 - Deploy a faulty integration flow](/exercises/ex2/ex24/)

#### Prerequisites:

- You are in [*Integration & Exception Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=com.sap.crun.imapp.ui#/Home) and have the respective default or self-managed *Cloud Integration service* in scope
- Data collection is activated as outlined in [Exercise 1.3](/exercises/ex1/ex13/)

## Exercise steps

Run through the steps in the given order

1. *Click* on the *three dots* and then on **Edit Configuration** on the card of the *Cloud Integration* service you have registered

   <br>![](/exercises/ex1/images/IMOverviewEditConfiguration.png)

2. *Check* whether the data collection is activated and *click* on the service link or the arrow on the right side and navigate to the details of the **service configuration**

   <br>![](/exercises/ex2/images/IMExceptConfigSelectService.png)
   
    A *Cloud Integration service* in SAP Cloud ALM serves three use cases: integration, exception, and health monitoring. The below **use cases** are part of *Integration & Exception Monitoring* and are displayed as **monitoring categories**:
    
	- *SAP Integration Suite Messages* for **integration monitoring**
	- *Integration Artifact Deployments* for **exception monitoring**

#### Adapt the **monitoring filter**

You will change the filter in a way that you will monitor only artifacts with *user ID*.

3. *Select* the **Integration Artifact Deployments** by *clicking* the *arrow* icon

   <br>![](/exercises/ex2/images/IMExceptSelectUsecase.png)
   
4. Within the *Integration Artifact Deployments filter page* **change the filter** 

	<br>![](/exercises/ex2/images/IMExceptConfigAddFilter.png)

    - Optional *Set* the field **Filter Name** to `ERROR <userID>`
    - *Change* the *Operator* of the line **Artifact Name** to `Contains` and the field *Value* to `userID`
    - If not available *Add* in line *Status* the *Value* `ERROR`
    - **Save** the *filter*

5. Go back to the *Configuration monitoring overview page* by using the **breadcrumb**

	<br>![](/exercises/ex2/images/IMExceptConfigAddFilterResult.png)
	
### Add a new event

6. Switch to the **Events tab**

	<br>![](/exercises/ex2/images/IMExceptConfigSwitchToEvents.png)

7. **Add** a new *event*

	<br>![](/exercises/ex2/images/IMExceptConfigAddEventButton.png)
	
8. *Enter* the following fields

    - *Select* the *Event Name* **Erroneous Integration Artifact** from the *drop down list*
    - *Set* the *Display Name* to  `<tenant_name> Deployment Exception` whereas `<tenant_name>` is one of `US01`, `US02`, `EU01`, `EU02`, `APJ01`, or `APJ02` corresponding to your service
    
    Then **activate** the alert by switching the *toggle* 

	<br>![](/exercises/ex2/images/IMExceptConfigActivateAlert.png)
	
9. *Optional:* if you want to **get email notification** on this event and have added your email address to SAP Cloud ALM as outlined in the previous [Exercise 2.3](/exercises/ex2/ex23/) then *switch the toggle* of the *Send Email To* section, *press* the **Add** button,  and *select* your available and **valid email address**.

    <br>![](/exercises/ex2/images/IMExceptConfigActivateEmail.png)

10. **Save** and **close** the configuration
   

## Summary

You've now activated events and alerts for all deployment exception that might occur in the *Cloud Integration* service your have registered. Future deployment exceptions will be displayed in the *Overview* page and in the *Exception* section, alerts will be displayed in the section *Alerting*.

<br>Continue to - [Exercise 2.5 - Deploy a misconfigured integration flow](/exercises/ex2/ex25/)
