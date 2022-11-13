# Exercise 2.1 - Bring a Cloud Integration service into scope

In this exercise, you will bring a *Cloud Integration* service into scope

#### Prerequisites:

- You are logged in to the [SAP Cloud ALM tenant](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home)
- :construction_worker: *If you are performing configurations yourself:* your self-managed Cloud Integration service `CloudIntegration-<tenant_name>-<userID>` should be registered and a secure connection established as outlined in [Register a Cloud Integration service in LMS](/exercises/ex1/ex11/)

## Exercise steps

Run through the steps in the given order

1.	*Navigate* to the section *SAP Cloud ALM for Operation* and click on the card **Integration & Exception Monitoring**

    <br>![](/exercises/ex1/images/CALMLandingIntExMon.png)

2. If you start *Integration & Exception Monitoring* the first time the *Scope Selection* dialog opens automatically.    
   If not *click* the **scope selection** icon in the black top row

    <br>![](/exercises/ex2/images/ScopeSelectionService.png)    

3. *Filter* for **Services**

4. In field **Service Type** select the *SAP Integration Suite (Cloud Integration)* from the drop down list

5. *Click* on **Go** in the upper right corner for filtering

6. *Search and select* at least the **Cloud Integration service** you are assigned to. Please check the  [Tenant Booker application](/exercises/ex0/ex02/) 

    :construction_worker: If you have registered an own *Cloud Integration service* `CloudIntegration-<tenant_name>-<userID>` select this one
    
    **Note:** every demo landscape is very artificial. Within this hands-on a large amount of Cloud Integration services is excepted, even for the same Cloud Integration tenant

    **Note:** you may select **additional services into your scope** as it is typical to have 2 to 3 integration tenants in an IT landscape. Keep the service in mind that you have registered. It is your **main service** the exercises are referencing.

    *If you are performing configurations yourself:* select at least the `CloudIntegration-<tenant_name>_<userID>` service. Otherwise select `CloudIntegration-<tenant_name>`. 
    
    You may add further services if you want but this isn't necessary for the exercise
    
7. **Apply** the selection


       
## Summary

Now the *Cloud Integration* service you want to monitor is in your scope.

<br>Continue to - [Exercise 2.2 - Familiarize yourself with the Integration & Exception Monitoring overview page](/exercises/ex2/ex22/)

