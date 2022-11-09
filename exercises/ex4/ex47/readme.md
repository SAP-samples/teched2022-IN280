# Add an email recipient using Notification Management	

In this exercise, we will add an email recipient to SAP Cloud ALM and verify this email address. This might be relevant whenever you want to get alert notifications in your email inbox. 

Also in the alerting section you may assign a processor to a particular alert. This is only possible with verified email addresses.

>
> *Note 1:* all other attendees of the TechEd hands-on session will see the email-address. **Please be aware!**
>
> *Note 2:* Within this TechEd session you see the email addresses `userID@opensapusers.com`. These are no verified email addresses and cannot be used in any of the SAP Cloud ALM actions
> 


#### Prerequisites:
You are logged in to [SAP Cloud ALM](https://teched22-cloudalm-003.eu10.alm.cloud.sap/launchpad#Shell-home) 

## Exercise steps

Run through the steps in the given order.

1. From the SAP Cloud ALM homepage click on the card **Notification Management**

    <br>![](/exercises/ex1/images/CALMLandingNotifMgmt.png) 
   
2. *Click* on the **+** icon on the right side, add your email address, and *save* the configuration

    <br>![](/exercises/ex1/images/NMAddEmail.png) 
    
3. Go into your email inbox and verify the email address

4. After the verification you should see your email address listed as verified

    <br>![](/exercises/ex1/images/NMEmailVerified.png) 
    

## Summary

You've now added your email address to SAP Cloud ALM and verified it. You will be able to receive alerts in your email inbox and use the address in SAP Cloud ALM actions.

Next we will ....... Continue to - [Exercise 5](../ex5/README.md)





<!--
# Available metrics for Cloud Integration

In this exercise, we will ...

## Exercise steps

Run through the exercise steps in the given order.

#### Prequisites:
The Cloud Integration tenant is already registered. If not please run through exercises [Register a Cloud Integration tenant in LMS](../ex11/).

If not already done, please login to [SAP Cloud ALM tenant](https://teched22-cloudalm-003.authentication.eu10.hana.ondemand.com/).  

1.	Navigate t...

   <br>![](/exercises/ex1/images/CALMLandingHealthMon.png)
   
    >
    > *Important:*
    > Health monitoring do.....
    >

## Summary

You've now ...
After completing these steps you will have created...

Go back to - [Exercise 4.4 - Check alerts in Health Monitoring](/exercises/ex4/ex44/)


2.	Insert this line of code.
```abap
response->set_text( |Hello ABAP World! | ). 
```

-->
