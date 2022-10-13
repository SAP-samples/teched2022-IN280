# Add an HTTP endpoint

In this exercise, you will learn how to add an HTTP endpoint for the monitoring use cases to establish authenticated connectivity to a registered Cloud Integration instance.

0. If not already done, please login to SAP Cloud ALM, navigate to section *Administration* and click on *Landscape Management* tile. 
    Select the registered Cloud Integration instance.

1. Use the button *Add* in the *Endpoints* section
      
    > PICTURE
    
2.	In the upcoming window under *General* maintain the fields:
    - Endpoint name: `CALM-IntSuite-EU1_<userID-digits>`. Take the `<userID-digits>` from the tenant booker application, while removing the starting P/S character.
    - Optionally maintain a description
    - Use Case: select all monitoring use cases
      -- `Exception Monitoring`
      -- `Integration Monitoring`
      -- `Health Monitoring` 
    - Root URL: copy/paste the URL *Tenant URL for SAP Cloud Integration* from the *Tenant Booker application* and removing the ending path `/itspaces/`. 
    
3.	Under *Authentication* maintain the OAuth credentials:
    - Authentication type: `OAuth2ClientCredentials`
    - Copy/paste the client ID, client secret, and token service URL of the service instance 
      > listed in Chapter: System details 
    
    > PICTURE

4. Check the network connection to verify if the entered parameters are correct

5. When done, click on *Save*

6. In the service configuration page, you get an overview of all created endpoints and monitoring use cases assigned to them. 
 
    > PICTURE
    
7. You can also check the connectivity to endpoint using the Ping all Endpoints button.

    A popup shows you that the connection has been setup successfully.

    Close the window


##### After completing these steps you will have....

added an HTTP endpoint in LMS for all monitoring use cases to establish authenticated connectivity to a registered Cloud Integration instance.


Continue to - [Create a HTTP endpoint](exercises/README.md)
