# Configure the monitoring of Cloud Integration tenant in SAP CLoud ALM

1. [Retrieve user / password](../../ex0/ex02/README.md) for SAP Integration Suite and SAP Cloud ALM
 
2. Login to SAP Cloud ALM using the link [teched22-cloudalm-003](https://teched22-cloudalm-003.authentication.eu10.hana.ondemand.com/).

3. Within the SAP Cloud ALM landing page navigate to section *Administration* and click on the tile *Landscape Management*

4. [Register a Cloud Integration tenant in SAP Cloud ALM](./ex11/README.md)

5. [Add an HTTP endpoint to a managed service](/exercises/ex1/ex12/README.md)
    
6.  Oversee the lifecycle status of managed services

    The service you have registered should be now in status *Active*. If not do a browser refresh to get the page updated.

    > PICTURE
    
7. [Activate data collection for the use case Integration & Exception Monitoring](exercises/ex1/ex13)


##### After completing these steps you will have....

set up the connectivity between SAP Cloud ALM monitoring use cases *Integration & Exception Monitoring* and *Health Montoring* to the a registered intance of a Cloud Integration capability of SAP Integration Suite. This is necessary to pull Cloud Integration for monitoring data.

Continue to - [Monitoring a deployment issue](exercises/ex2/README.md)
