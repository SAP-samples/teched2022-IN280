# Access information

We have a specific application in place, the **Tenant Booker application** that provides all attendees access to the *SAP Cloud ALM* and all *SAP Integration Suite* tenants. Regarding the *SAP Integration Suite* tenants a load balancing will be practiced.

### Retrieve user and password

Go to the *Tenant Booker application* (link will be added directly before the hands-on session will start)

<br>![](/exercises/ex1/images/BookerApp.png)

As a result you get *user* and *password* for the logins to **SAP Integration Suite** as well as for **SAP Cloud ALM**

Please recognize the SAP Integration Suite tenant assigned to you and keep it in mind throughout the exercises. The screenshot shows that a attendee would be assigned to tenant `TECHED-US01`. Check your *tenant_name*, one of the ones mentioned in [System landscape](/exercises/ex0)

<br>![](/exercises/ex1/images/BookerAppResult.png) 
    
### System access

- *SAP Integration Suite* tenant: first link of the result list of the *Tenant Booker app*
- [*SAP Cloud ALM* tenant](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home)

### Additional hints for [Exercise 1.2](/exercises/ex1/ex12)

- Please ignore *Client ID* and *Client Secret* credentials and use only the API credentials
- Use the second link *Tenant URL for SAP Cloud Integration* as *Root URL* but without `/itspaces/` at the end

**Note:** Best practice is to keep the browser tab open for accessing *user/password* assigned to you

<br>Return back to your last exercise using the *browser back*
