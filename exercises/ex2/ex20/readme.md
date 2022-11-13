# Scenario introduction: Deployment exception of an integration flow

With the exception monitoring of SAP Cloud ALM it is possible to monitor exceptions. In case of the *Cloud Integration capability of SAP Integration Suite* these are deployment exceptions.

As an example for this exercise an integration flow has been prepared in the Cloud Integration capability of SAP Integration Suite that cannot be deployed in the way as it is configured. It is a very simple *Hallo World* flow that is leveraging **ProcessDirect sender and receiver adapters** that are typically used for flow-to-flow communication between a standard SAP and a custom-specific integration flow. 

<br>![](/exercises/ex2/images/IFlowHalloWorld.png)

The integration flow is timer triggered and run only once after deployment. We don't have any sender or receiver.  The *Producer Integration Process* produces the payload **Hallo World** via Groovy script and adds some properties into the header. Headers and payloads can be transferred via ProcessDirect adapter to the *Consumer Integration Process*. This process extends the payload to **Hallo World ! Nice to see you!**  `userID` **is at TechEd**.

<br>![](/exercises/ex2/images/SuitePDConcept.png)

>
> **Important**: The ProcessDirect adapters use a channel for the flow-to-flow communication. The channelId must be unique and identical. If not, a deployment exception is raised. This behavior is used for this exercise.
>  

Some information as the *userID* are written to *custom header properties *. These can be tracked in *Integration & Exception Monitoring* in the tracking section.

Continue to [Exercise 2.1 - Bring a Cloud Integration service into scope](/exercises/ex2/ex21/)
