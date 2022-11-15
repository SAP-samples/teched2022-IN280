# Exercise 1.3 - Activate data collection for the use case Integration & Exception Monitoring 

In this exercise, you will learn how to activate data collection specifically for the use case *Integration & Exception Monitoring*.

**Note:** This exercise is only necessary if you configure a Cloud Integration service in SAP Cloud ALM yourself.

#### Prerequisites:
- You are logged in to [SAP Cloud ALM](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home)
- An own managed *Cloud Integration* service `CloudIntegration-<tenant_name>_<userID>` should be already registered in LMS

## Exercise steps

Run through the steps in the given order

1. Navigate to section *SAP Cloud ALM for Operations* and click on the card **Integration & Exception Monitoring** 
      
2. Bring the **Cloud Integration service into the scope**

   If you start *Integration & Exception Monitoring* the first time the *Scope Selection* dialog opens automatically. If not *click* the **scope selection** icon in the black top row
   
    - *Filter* for **Services**
    - In field *Service Type* select the *SAP Integration Suite (Cloud Integration)* from the drop down list
    - *Click* on **Go** in the upper right corner for filtering
    - *Search and select* at least the **Cloud Integration service** that you have registered in [Register a Cloud Integration service in LMS](/exercises/ex1/ex11)
    
        **Note:** a demo landscape is very artificial. Therefore a large amount of Cloud Integration services are available, even for the same Cloud Integration tenant
        
        **Note:** you may select **additional services into your scope** as it is typical to have 2 to 3 integration tenants in an IT landscape. Keep the service `CloudIntegration-<tenant_name>_<userID>` in mind that you have registered. It is your **main service** the exercises are referencing.
        
    - **Apply** the configuration
      
     <br>![](/exercises/ex1/images/ScopeSelectionRegisteredService.png)
      
3. **Activate data collection**

    In the footer of your service's card you can recognize that no data has been collect so far
    
   <br>![](/exercises/ex1/images/IMOverviewNoData.png)

    a. *Click* on the **three dots** and then on **Edit Configuration**
    
    <br>![](/exercises/ex1/images/IMOverviewEditConfiguration.png)
    
    b. **Switch on** the data collection using the *toggle button*, **save** the configuration, and **close** the dialog
    
    <br>![](/exercises/ex1/images/IMConfigDataCollection.png)
	
    c. Proof whether the data collection is running successfully
    
    <br>![](/exercises/ex1/images/IMOverviewDataCollectionActivated.png)

     :custard: It takes some minutes until the *Data Quality* icon in the footer of the *Cloud Integration* service card gets updated
     
    d. **Refresh** the user interface to see whether the data collection has been started 
    
## Summary

You have activated the data collection for your own-managed Cloud Integration service `CloudIntegration-<tenant_name>_<userID>`

Congratulation. You have finalized Exercise 1. 

Continue to [Exercise 2 - Monitoring a deployment exception](/exercises/ex2/) 
