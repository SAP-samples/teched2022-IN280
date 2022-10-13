# Configurations in SAP Integration Suite subaccounts

To enable OAuth authentication between SAP Cloud ALM and SAP Integration Suite a setup has to be performed. 
To minimize the additional effort for you, we have prepared some configurations already. In case you want to practice this configuration yourself you may read the below steps. They are only for your information. 

Please ensure for the **SAP Integration Suite** subaccount that the following steps have been made in the BTP Cockpit:
- Creation of a service instance of a service *Process Integration Runtime* with *api* plan and the roles:
  -	*MonitoringArtifactsDeploy*
  -	*MonitoringDataRead*
  - *HealthCheckMonitoringDataRead*
- Creation of a service key for the above instance that provides client ID, client secret, URL, and token URL

If you want to monitor the API Management capability of SAP Integration Suite a separate service instance with the role *APIPortal.Administrator* and the correspondent service key has to be created.

In the SAP Cloud ALM subaccount the role *Integration Monitoring Integration Architect* must be assigned.

For further information on how to the setup especially SAP Integration Suite running in the Neo environment please read the documentation at the [SAP Cloud ALM - Expert Portal pages](https://support.sap.com/en/alm/sap-cloud-alm/operations/expert-portal/setup-managed-services/setup-cpi-cf.html).

Continue to - [Setup the monitoring of SAP Integration Suite through SAP CLoud ALM](../ex1/README.md)
