# Exercise 1.2 - Add an HTTP endpoint to a managed service

In this exercise, you will learn how to add an HTTP endpoint to establish authenticated connectiion to a Cloud Integration tenant of SAP Integration Suite. This endpoint will be leveraged for all ALM monitoring use cases.

**Note:** This exercise is only necessary if you configure a Cloud Integration service in SAP Cloud ALM yourself.

#### Prerequisites

- You are logged in the [Landscape Management service](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=sap.crun.landscape) of [SAP Cloud ALM](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home)
- A *Cloud Integration* service is registered as outlined in [Exercise 1.1](/exercises/ex1/ex11/)

## Exercise steps

Run through the steps in the given order. 

1. *Click* on the button **Add** in the *Endpoints* section

    <br>![](/exercises/ex1/images/LMSAddEndpointButton.png)
       
2.	In the upcoming window under *General* maintain the fields:
    
    - *Endpoint name*: `<tenantID>-<userID>`
       
        *Copy* your `userID` from  the [Tenant Booker application](/exercises/ex0/ex02/)
		
    - Optionally maintain a description
    - *Use Case*: select all monitoring use cases
        - Exception Monitoring
        - Integration Monitoring
        - Health Monitoring
     - *Root URL*: Copy the URL provided by the [Tenant Booker application](/exercises/ex0/ex02/), this is the second link *Tenant URL for SAP Cloud Integration*. **Please remove the ending `/itspaces/`**
    
  
3.	Under *Authentication* maintain the OAuth credentials:
	
	- Authentication type: `OAuth2ClientCredentials`
	
	- Copy/paste the *client ID, client secret*, and *token service URL* provided via the  [Tenant Booker app](/exercises/ex0/ex02/) 

	   <br>![](/exercises/ex1/images/LMSAddEndpoint.png)

	  :warning: Just to be clear, please copy/paste the details from the **API Client ID / Secret**, see the screenshot below

		 <br>![](/exercises/ex1/images/BookerAppResultEndpoint.png)
    
4. *Check* the **network connection** to verify whether the entered parameters are correct

    <br>![](/exercises/ex1/images/LMSEndpointConnectionCheck.png)
    
    If you don't see the three use cases add them. If the connectivity fails check the parameters.
    
5. When done, click on **Save**

6. In the service configuration page, get an overview about all created endpoints and monitoring use cases assigned to them

6. You can also check the connectivity using the **Ping Endpoints** button. 

    <br>![](/exercises/ex1/images/LMSPingConnection.png)
    
    A popup shows up, close it. The rectangle icon in the *Status* column will switch to green indicating that the connection is established successfully.
    
    **Close** the detailed page for the selected service.
    
7.  Oversee the lifecycle status of all managed services

    The service you have registered should be now in status *Active*. If not do a browser refresh to get the page updated.

    <br>![](/exercises/ex1/images/LMSManagedServices.png)
    
## Summary

Now you have established authenticated connectivity from your registered Cloud Integration service to the *Cloud Integration tenant* of SAP Integration Suite for all use cases integration, exception, and health monitoring.

Continue to - [Exercise 1.3 - Activate data collection for the use case Integration & Exception Monitoring](/exercises/ex1/ex13/)
