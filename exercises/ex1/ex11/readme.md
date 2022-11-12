# Exercise 1.1 - Register a Cloud Integration service in LMS

In this exercise, you will learn how to register a Cloud Integration service in the *Landscape Management Service (LMS)* of SAP Cloud ALM. This service has a secure connection to a respective Cloud Integration tenant as part of SAP Integration Suite. 

**Note:** This exercise is only necessary if you configure a Cloud Integration service in SAP Cloud ALM yourself.

:warning: to be added: Overview on available SAP Integration Suite tenants and SAP Cloud ALM tenant for this session

<br>![](/exercises/ex1/images/RegisteredServicesToSuiteTenants.png)

#### Prerequisites

- You are logged in to the [SAP Cloud ALM tenant](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home)

## Exercise steps

Run through the steps in the given order

1. [Retrieve user / password](/exercises/ex0/ex02/) for SAP Integration Suite and SAP Cloud ALM

2. Navigate to the section *Administration* and click on *Landscape Management* tile. 

    <br>![](/exercises/ex1/images/CALMLandscapeAdministration.png)   

3. Use the *Add* button in the upper right corner

    <br>![](/exercises/ex1/images/LMSAdd.png)   
      
4.	Enter all mandatory parameters under *General Properties*

	<br>![](/exercises/ex1/images/LMSAddCPIservice.png)
	
    - *Name*: `CloudIntegration-<tenant_name>-<userID>`
       		
		- Copy the tenant name from  the [Tenant Booker application](/exercises/ex0/ex02/): either TECHED-US01, TECHED-US02, TECHED-E01, TECHED-EU02, TECHED-APJ01, or TECHED-APJ02
		- Use your `userID` from  the [Tenant Booker application](/exercises/ex0/ex02/)
		
	   
    - Optionally maintain a description
    - *Tenant ID*: `01234567<userID-digits>` removing the beginning character of your `userId`
    - *Service Type*: `SAP Integration Suite (Cloud Integration)`
    - *Tenant Role*: `Test`
    - *Root URL*: Copy the URL provided by the [Tenant Booker application](/exercises/ex0/ex02/), this is the second link *Tenant URL for SAP Cloud Integration*. **Please remove the ending `/itspaces/`**
   
 5. When done, click on *Save*
  
## Summary

After completing these steps you will have registered a new instance of a Cloud Integration capability of SAP Integration Suite to the SAP Cloud ALM by leveraging the Landscape Management Service (LMS) service.

<br>Continue to - [Exercise 1.2 -Add an HTTP endpoint to a managed service](../ex12/)
