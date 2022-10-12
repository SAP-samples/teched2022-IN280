# SETUP MONITORING OF SAP INTEGRATION SUITE WITH SAP CLOUD ALM 

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

For further information on how to the setup especially SAP Integration Suite running in the Neo environment please read the documentation at the SAP Cloud ALM product expert pages: https://support.sap.com/en/alm/sap-cloud-alm/operations/expert-portal/setup-managed-services/setup-cpi-cf.html.

## Level 2 Heading

After completing these steps you will have....

1.	Click here.
<br>![](/exercises/ex0/images/00_00_0010.png)

2.	Insert this code.
``` abap
 DATA(params) = request->get_form_fields(  ).
 READ TABLE params REFERENCE INTO DATA(param) WITH KEY name = 'cmd'.
  IF sy-subrc <> 0.
    response->set_status( i_code = 400
                     i_reason = 'Bad request').
    RETURN.
  ENDIF.
```

## Summary

Now that you have ... 
Continue to - [Exercise 1 - Exercise 1 Description](../ex1/README.md)
