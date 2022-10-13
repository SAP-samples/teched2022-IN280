# Register a Cloud Integration tenant in SAP Cloud ALM

In this exercise, you will how to register a Cloud Integration instance to SAP Cloud ALM.

0. If not already done, please login to SAP Cloud ALM, navigate to section *Administration* and click on *Landscape Management* tile.

1. OPTIONAL Use the *Add* button in the upper right corner.
      
    >(Should we create the service upfront?
    >
    > Usually, your cloud services are imported from the System Landscape Information Service (SLIS). As we are not in a customer landscape, we have to add the cloud service to the Landscape Management Service (LMS). 
    >
    > As SAP Integration Suite has to be pulled for monitoring information from SAP Cloud ALM and this set up isn’t configured by default the instance has to be registered manually.

2.	Enter all mandatory parameters under *General Properties*
    - Name: `CALM-IntSuite-EU10`
    - Optionally maintain a description
    - Tenant ID: `12345678901` (must be unique, we have to use userIDs)
        > We can also use 1234 concatecanted by the digits after the userID
    - Service Type: `SAP Integration Suite (Cloud Integration)`
    - Tenant Type: `Test`
    - Root URL: `https://teched-calm01.integrationsuite.cfapps.eu10-003.hana.ondemand.com` or use the URL that has been provided to you from the Tenant Booker application under *Tenant URL for SAP Cloud Integration*. Please remove the ending path `/itspaces/`.
   
   > PICTURE

  3. When done, click on *Save*

    > PICTURE
    
##### After completing these steps you will have....

registered a new instance of a Cloud Integration capability of SAP Integration Suite to the SAP Cloud ALM by leveraging the Landscape Management Service (LMS) service.


Continue to - [Create a HTTP endpoint](exercises/ex1/ex12/README.md)
