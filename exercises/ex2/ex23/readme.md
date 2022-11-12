# Exercise 2.3 - Activate alerts for deployment exceptions of integration artifacts

In this exercise, you will activate  **monitoring** and  **alerting** of integration exceptions for a particular *Cloud Integration service*

#### Prerequisites:

- You are in [*Integration & Exception Monitoring*](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=com.sap.crun.imapp.ui#/Home) and have the respective default or self-managed *Cloud Integration service* `CloudIntegration-<tenant_name>_<userID>` in scope
- *If you are performing configurations yourself:* you have activated the data collection as outlined in [Exercise 1.3](/exercises/ex1/ex13/)

## Exercise steps

Run through the steps in the given order

1. *Click* on the *three dots* and then on *Edit Configuration* on the card of the *Cloud Integration* service you have registered

   <br>![](/exercises/ex1/images/IMOverviewEditConfiguration.png)

2. *Check* whether the data collection is activated and *click* on the service link or the arrow on the right side and navigate to the details of the **service configuration**

   <br>![](/exercises/ex2/images/IMExceptConfigSelectService.png)
   
    A *Cloud Integration service* in SAP Cloud ALM serves three use cases: integration, exception, and health monitoring. The below **use cases** are part of *Integration & Exception Monitoring* and are displayed as **monitoring categories**:
    
	- *SAP Integration Suite Messages* for **integration monitoring**
	- *Integration Artifact Deployments* for **exception monitoring**

#### Adapt the **monitoring filter**

❗ If you are using the default preconfigured *Cloud Integration services* the monitoring filter is a generic one and can't be changed. Filtering is with the purpose of this exercise not allowed **Please jump to the step 6**

If you configure your *self-managed Cloud Integration service* `CloudIntegration-<tenant_name>-<userID>` you can adapt the **monitoring filter** as per your needs.
You will change the filter in a way that you will monitor only artifacts with *user ID* in the name.

3. *Select* the **Integration Artifact Deployments** by *clickig* the *arrow* icon

   <br>![](/exercises/ex2/images/IMExceptSelectUsecase.png)
   
4. Within the *Integration Artifact Deployments filter page* **add a new filter** 

	<br>![](/exercises/ex2/images/IMExceptConfigAddFilter.png)

    - *Set* the field **Filter Name** to `ERROR <userID>`
    - *Change* the *Operator* of the line **Artifact Name** to `Contains`and the field *Value* to `userID`
    - *Add* in line *Status* the *Value* `ERROR`
    - **Save** the *filter*

5. Go back to the *Configuration monitoring overview page* by using the **breadcrumb**

	<br>![](/exercises/ex2/images/IMExceptConfigAddFilterResult.png)
    
    You should see now an additional *Integration Artifact Deployments* entry that is activated automatically
	
### Add a new event

6. Switch to the **Events tab** and **add* a new *event*

	<br>![](/exercises/ex2/images/IMExceptConfigSwitchToEvents.png)

	<br>![](/exercises/ex2/images/IMExceptConfigAddEventButton.png)
	
7. *Choose* the event type **Erroneous Integration Artifact**  and **activate** the alert by switching the *toggle* 

	<br>![](/exercises/ex2/images/IMExceptConfigActivateAlert.png)
	
8. **Save** and **close** the configuration
   

## Summary

You've now activated events and alerts for all deployment exception that might occur in the *Cloud Integration* service your have registered. Future deployment exceptions will be displayed in the *Overview* page and in the *Exception* section, alerts will be displayed in the section *Alerting*.

<br>Continue to - [Exercise 2.4 - Deploy a faulty integration flow](/exercises/ex2/ex24/)
