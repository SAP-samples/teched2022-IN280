# Register a Cloud Integration service in LMS

   >(Should we create the service upfront?
    >
    > Usually, your cloud services are imported from the System Landscape Information Service (SLIS). As we are not in a customer landscape, we have to add the cloud service to the Landscape Management Service (LMS). 
    >
    > As SAP Integration Suite has to be pulled for monitoring information from SAP Cloud ALM and this set up isn’t configured by default the instance has to be registered manually.


In this exercise, you will learn how to register a Cloud Integration instance in Landscape Management Service (LMS.

### Overview on available SAP Integration Suite tenants and SAP Cloud ALM tenant for this session

<br>![](/exercises/ex1/images/RegisteredServicesToSuiteTenants.png)

### Prerequisites

- Login to *SAP Cloud ALM* using the link [https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home).

- Within the SAP Cloud ALM landing page navigate to section *Administration* and click on *Landscape Management* tile. 

## Exercise steps

Run through the steps in the given order.

1. Use the *Add* button in the upper right corner

      <br>![](/exercises/ex1/images/LMSAdd.png)
      
2.	Enter all mandatory parameters under *General Properties*

	<br>![](/exercises/ex1/images/LMSAddCPIservice.png)
	
    - *Name*: `CloudIntegration-<tenant_name>_<userID>`
       
		- Use your `<userID>`
		
		- Copy the tenant name from  the *Tenant Booker application*
	   
    - Optionally maintain a description
    - *Tenant ID*: `01234567<userID-digits>` removing the beginning character of your userId
    - *Service Type*: `SAP Integration Suite (Cloud Integration)`
    - *Tenant Type*: `Test`
    - *Root URL*: Copy the URL provided by the Tenant Booker application under the field *Tenant URL for SAP Cloud Integration*. Please remove the ending `/itspaces/`.
   


  3. When done, click on *Save*
  
## Summary

After completing these steps you will have registered a new instance of a Cloud Integration capability of SAP Integration Suite to the SAP Cloud ALM by leveraging the Landscape Management Service (LMS) service.

Next we will create an HTTP endpoint to establish authenticated connectivity to this tenant. Continue to - [Exercise 1.2](../ex12/)
