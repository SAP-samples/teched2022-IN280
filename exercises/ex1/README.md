# Setup the monitoring of SAP Integration Suite through SAP CLoud ALM

1. Go to the Tenant Booker application to retrieve your user and password for the login in to SAP Integration Suite and SAP Cloud ALM. This booker app provides you the relevant roles for this exercise.

    <br>![](/exercises/ex1/images/BookerApp.png)
  
    Please ignore CLient ID and Client Secret. This info is realted to TechEd sessions that use the booker app, too.
    Regarding the second URL, we will leverage this URL without '/idpsaces/' during HTTP endpoint creation in the Landscape Management Service of SAP Cloud ALM.

   Keep the browser tab open for accessing user/password assigned to you.
  
2. Login to SAP Cloud ALM using the link [teched22-cloudalm-003](https://teched22-cloudalm-003.authentication.eu10.hana.ondemand.com/).

3. After login, you see the SAP Cloud ALM landing page. The booker app had provided you all relevant roles.

    Please navigate to section *Administration* and click on the tile *Landscape Management*.

4. [Register a Cloud Integration tenant in SAP Cloud ALM](exercises/ex1/ex11)

5. [Add an HTTP endpoint to a managed service](exercises/ex1/ex12)
    
6.  See the lifecycle status of all managed services

    The service you have registered should be now in status *Active*. If not do a browser refresh to get the page updated.

    > PICTURE
    
7. Activate data collection for the use case Integration & Exception Monitoring 

##### After completing these steps you will have....

set up the connectivity between SAP Cloud ALM monitoring use cases *Integration & Exception Monitoring* and *Health Montoring* to the a registered intance of a Cloud Integration capability of SAP Integration Suite. This is necessary to pull Cloud Integration for monitoring data.

Continue to - [Monitoring a deployment issue](../ex2/README.md)
