# Register a Cloud Integration service in LMS

   >(Should we create the service upfront?
    >
    > Usually, your cloud services are imported from the System Landscape Information Service (SLIS). As we are not in a customer landscape, we have to add the cloud service to the Landscape Management Service (LMS). 
    >
    > As SAP Integration Suite has to be pulled for monitoring information from SAP Cloud ALM and this set up isn’t configured by default the instance has to be registered manually.


In this exercise, you will learn how to register a Cloud Integration instance in Landscape Management Service (LMS.

0. If not already done, please 

    - Login to *SAP Cloud ALM* using the link [https://teched22-cloudalm-003.authentication.eu10.hana.ondemand.com/](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home).
    - Within the SAP Cloud ALM landing page navigate to section *Administration* and click on *Landscape Management* tile. 
    - Select the registered Cloud Integration instance.

1. Use the *Add* button in the upper right corner

      <br>![](/exercises/ex1/images/LMSAdd.png)
      
2.	Enter all mandatory parameters under *General Properties*
    - *Name*: `CloudIntegration-TECHED-<tenant_name>_<userID-digits>`
       
       Copy the `<userID-digits>` from the tenant booker application, while removing the starting P/S character.
    - Optionally maintain a description
    - *Tenant ID*: `01234567<userID-digits>` 
    - *Service Type*: `SAP Integration Suite (Cloud Integration)`
    - *Tenant Type*: `Test`
    - *Root URL*: Copy the URL provided by the Tenant Booker application under the field *Tenant URL for SAP Cloud Integration*. Please remove the ending `/itspaces/`.
   
       <br>![](/exercises/ex1/images/LMSAddCPIservice.png)

  3. When done, click on *Save*
  
## Summary

After completing these steps you will have registered a new instance of a Cloud Integration capability of SAP Integration Suite to the SAP Cloud ALM by leveraging the Landscape Management Service (LMS) service.

Next we will create an HTTP endpoint to establish authenticated connectivity to this tenant. Continue to - [Exercise 1.2](../ex12/)
