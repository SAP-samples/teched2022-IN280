# Exercise 1.1 - Register a Cloud Integration service in LMS

In this exercise, you will learn how to register a Cloud Integration service in the *Landscape Management Service (LMS)* of SAP Cloud ALM that is monitoring a Cloud Integration tenant as part of SAP Integration Suite. 


### Overview on available SAP Integration Suite tenants and SAP Cloud ALM tenant for this session

<br>![](/exercises/ex1/images/RegisteredServicesToSuiteTenants.png)

#### Prerequisites

- You are logged in to the [SAP Cloud ALM tenant](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home)

## Exercise steps

Run through the steps in the given order.

1. [Retrieve user / password](../ex0/ex02/) for SAP Integration Suite and SAP Cloud ALM

2. Navigate to the section *Administration* and click on *Landscape Management* tile. 

    <br>![](/exercises/ex1/images/CALMLandscapeAdministration.png)   

3. Use the *Add* button in the upper right corner

    <br>![](/exercises/ex1/images/LMSAdd.png)   
      
4.	Enter all mandatory parameters under *General Properties*

	<br>![](/exercises/ex1/images/LMSAddCPIservice.png)
	
    - *Name*: `CloudIntegration-<tenant_name>_<userID>`
       
		- Use your `<userID>`
		
		- Copy the tenant name from  the *Tenant Booker application*
	   
    - Optionally maintain a description
    - *Tenant ID*: `01234567<userID-digits>` removing the beginning character of your userId
    - *Service Type*: `SAP Integration Suite (Cloud Integration)`
    - *Tenant Type*: `Test`
    - *Root URL*: Copy the URL provided by the Tenant Booker application under the field *Tenant URL for SAP Cloud Integration*. Please remove the ending `/itspaces/`.
   
 5. When done, click on *Save*
  
## Summary

After completing these steps you will have registered a new instance of a Cloud Integration capability of SAP Integration Suite to the SAP Cloud ALM by leveraging the Landscape Management Service (LMS) service.

<br>Continue to - [Exercise 1.2 -Add an HTTP endpoint to a managed service](../ex12/)
