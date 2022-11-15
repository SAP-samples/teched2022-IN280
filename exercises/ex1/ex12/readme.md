# Exercise 1.2 - Add an HTTP endpoint to a managed service

In this exercise, you will learn how to add an HTTP endpoint for establishing an authenticated connectiion to a Cloud Integration tenant in SAP Integration Suite. This endpoint will be leveraged by all ALM monitoring use cases.

:construction_worker: **Note: This exercise is only necessary if you configure a Cloud Integration service in SAP Cloud ALM yourself**

#### Prerequisites

- You are logged in the [Landscape Management service](https://teched22-cloudalm-003.eu10.alm.cloud.sap/shell/run?sap-ui-app-id=sap.crun.landscape) of [SAP Cloud ALM](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home)
- A *Cloud Integration* service is registered as outlined in [Exercise 1.1](/exercises/ex1/ex11/)

## Exercise steps

Run through the steps in the given order

1. *Click* on the button **Add** in the *Endpoints* section

    <br>![](/exercises/ex1/images/LMSAddEndpointButton.png)
       
2. In the upcoming window under *General* maintain the fields

    <br>![Replace the highlighted parts by the Tenant Booker app info](/exercises/ex1/images/LMSAddEndpointGeneral.png)
    
    Highlighted are the *tenant specific* information you have to replace
    
    - *Endpoint name*: `<tenant_name>-<userID>` with *tenant names* such as TECHED-US01, TECHED-US02, TECHED-EU01, TECHED-EU02, TECHED-APJ01, or TECHED-APJ02
       
        *Copy* your `<tenant_name>` and `userID` from  the **Tenant Booker application** linked in [Access information](/exercises/ex0/ex02/) 
		
    - *Optionally* maintain a description
    - *Use Case*: select all monitoring use cases
        - Exception Monitoring
        - Integration Monitoring
        - Health Monitoring
     - *Root URL*: this field is available automatically

3.	Under *Authentication* maintain the **OAuth credentials**

    <br>![Highlighted the tenant name](/exercises/ex1/images/LMSAddEndpointAuthentication.png)
    
    Highlighted are the *tenant specific* information you have to enter
    
	- Authentication type: `OAuth2ClientCredentials`
	
	- Copy/paste the *client ID, client secret*, and *token service URL* from the **Tenant Booker application** linked in [Access information](/exercises/ex0/ex02/) 
  
	  :warning: Just to be clear, please copy/paste the details from the **API Client ID / Secret**, see the screenshot below. These credentials relate to the *Process Integration* **API plan**!

      <br>![Highlighted the tenant name](/exercises/ex1/images/BookerAppResultEndpointAuthentication.png)
   
4. *Check* the **network connection** to verify whether the entered parameters are correct

    <br>![](/exercises/ex1/images/LMSEndpointConnectionCheck.png)
    
    :warning: If you don't see the three use cases add them. If the connectivity fails check the parameters.
    
5. When done, **save** the endpoint configuration

6. In the **service configuration page**, get an overview of all created endpoints and monitored use cases

6. You can also check the connectivity using the **Ping Endpoints** button. 

    <br>![](/exercises/ex1/images/LMSPingConnection.png)
    
    A popup shows up, close it. The rectangle icon in the *Status* column will switch to green indicating that the connection is established successfully.
    
    **Close** the detailed page for the selected service.
    
7.  Oversee the lifecycle status of all managed services

    The service you have registered will be in status **Active**. This will take a while, and do a browser refresh to get the page updated.

    <br>![](/exercises/ex1/images/LMSManagedServices.png)
    
## Summary

Now you have established authenticated connectivity from your registered Cloud Integration service to the *Cloud Integration tenant* of SAP Integration Suite for all use cases integration, exception, and health monitoring.

Continue to - [Exercise 1.3 - Activate data collection for the use case Integration & Exception Monitoring](/exercises/ex1/ex13/)
