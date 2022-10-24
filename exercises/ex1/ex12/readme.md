# Add an HTTP endpoint to a managed service

In this exercise, you will learn how to add an HTTP endpoint to establish authenticated connectivity to a registered Cloud Integration instance. This endpoint will be valid for all ALM monitoring use cases.

### Prerequisites

- Login to *SAP Cloud ALM* and navigate to the *Landscape Management* service.

- A *Cloud Integration* service is registered as described in [Exercise 1.1](/exercises/ex1/ex11/)

## Exercise steps

Run through the steps in the given order. 

1. *Click* on the button *Add* in the *Endpoints* section

    <br>![](/exercises/ex1/images/LMSAddEndpointButton.png)
       
2.	In the upcoming window under *General* maintain the fields:
    
    - Endpoint name: `<tenantID>-<userID-digits>`. 
        
        Take the `<userID-digits>` from the tenant booker application.
		
    - Optionally maintain a description
    - Use Case: select all monitoring use cases
      -- `Exception Monitoring`
      -- `Integration Monitoring`
      -- `Health Monitoring` 
    - Root URL: copy/paste the URL *Tenant URL for SAP Cloud Integration* from the *Tenant Booker application* and removing the ending path `/itspaces/`. 
    
    <br>![](/exercises/ex1/images/LMSAddEndpoint.png)
    
3.	Under *Authentication* maintain the OAuth credentials:
    - Authentication type: `OAuth2ClientCredentials`
    - Copy/paste the *client ID, client secret*, and *token service URL* provided via the Tenant Booker app.
    
4. *Check* the *network connection* to verify if the entered parameters are correct

    <br>![](/exercises/ex1/images/LMSEndpointConnectionCheck.png)
    
5. When done, click on *Save*

6. In the service configuration page, get an overview about all created endpoints and monitoring use cases assigned to them

6. You can also check the connectivity using the *Ping Endpoints* button. 

    <br>![](/exercises/ex1/images/LMSPingConnection.png)
    
    A popup shows up, close it. The rectangle icon in the *Status* column will switch to green indicating that the connection is established successfully.
    
    Close the detailed page for the selected service.
    
7.  Oversee the lifecycle status of all managed services

    The service you have registered should be now in status *Active*. If not do a browser refresh to get the page updated.

    <br>![](/exercises/ex1/images/LMSManagedServices.png)
    
## Summary

After completing these steps you will have added an HTTP endpoint in LMS for all monitoring use cases to establish an authenticated connectivity from your registered Cloud Integration service to the *Cloud Integration tenant*.

Next we will activate the data collection for monitoring the Cloud Integration tenant. 

Continue to - [Exercise 1.3](../ex13/)
