# Exercise 1.3 - Activate data collection for the use case Integration & Exception Monitoring 

In this exercise, you will learn how to activate the data collection specifically for the use case *Integration & Exception Monitoring*.
*This exercise is only necessary if you configure a Cloud Integration service in SAP Cloud ALM yourself.*

#### Prerequisites:
The Cloud Integration tenant `CloudIntegration-<tenant_name>_<userID>` is already registered and an endpoint is created for the use cases *Integration Monitoring* and *Exception Monitoring*. If not please run through exercises [Register a Cloud Integration tenant in LMS](../ex11/) and [Add an HTTP endpoint to a managed service](../ex12/).

## Exercise steps

Run through the steps in the given order.

1. Navigate to section *SAP Cloud ALM for Operations* and click on the card *Integration & Exception Monitoring* if are not already there
      
    <br>![](/exercises/ex1/images/CALMLandingIntExMon.png)
  
2. Bring the **Cloud Integration service into the scope**, if not already done

   If you start *Integration & Exception Monitoring* the first time the *Scope Selection* Diaglog opens automatically.
   
    <br>![](/exercises/ex1/images/InitialScopeSelection.png)
   
    a)  Filter for *Services*
    
    b)  Click on *Go* in the upper right corner for filtering
    
    c)  Search and select the Cloud Integration service instance that you have registered in Exercise [Register a Cloud Integration tenant in SAP Cloud ALM](exercises/ex1/ex11)

    d)  Click on the button *Apply* to save the configuration
      
     <br>![](/exercises/ex1/images/ScopeSelectionService.png)
      
3. **Activate data collection**

    In the footer of your service's card you can recognize that no data has been collect so far.
    
   <br>![](/exercises/ex1/images/IMOverviewNoData.png)

    a. *Click* on the *three dots* and then on *Edit Configuration*
    
    <br>![](/exercises/ex1/images/IMOverviewEditConfiguration.png)
    
    b. *Switch on* the data collection using the *toggle button*, save the configuration, and close the dialog
    
    <br>![](/exercises/ex1/images/IMConfigDataCollection.png)
	
    c. Proof whether the data collection is running successfully
    
    <br>![](/exercises/ex1/images/IMOverviewDataCollectionActivated.png)

    It takes some minutes until the *Data Quality* icon in the footer of the *Cloud Integration* service card is updated.
    
## Summary

After completing these steps you will have activated the data collection in *Integration & Exception Monitoring* for a managed Cloud Integration service `CloudIntegration-<tenant_name>_<userID>`.

Return back to [Exercise 1 - Configure the monitoring of Cloud Integration tenant in SAP CLoud ALM](../../ex1/README.md) <br>or to [Exercise 2.2 - Activate alerts for deployment exceptions of integration artifacts](../../ex2/ex22/) 
