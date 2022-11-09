# Exercise 2 - Understand the integration flow that might lead to a deployment exception

We are using a very simple *Hallo World* integration flow for this exercise. The flow is leveraging ProcessDirect sender and receiver adapters that are typically used for  flow-to-flow between a standard SAP and a custom-specific integration flow. 

<br>![](/exercises/ex2/images/SuitePDConcept.png)

The integration flow is timer triggered and run only once after deployment. The *Producer* produce the payload **Hallo World** and adds some properties into the header. Headers and payloads can be transferred via ProcessDirect adapter to the *Consumer* process. This one extends the payload to **Hallo World ! Nice to see you!**  `P012345` **is at TechEd**

>
> *Important*: The ProcessDirect adapters use a channel for the flow-to-flow communication. The channelId must be unique and identical. If not, a deployment exception is raised. 
>  

Some information as the userID are written to *CustomHeaderProperties*. These can be tracked in *Integration & Exception Monitoring* in the tracking section.
