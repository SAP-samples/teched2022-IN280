# Exercise 4.0 - Scenario introduction: Health monitoring of Cloud Integration resources

Health monitoring is focusing on **technical aspects** to identify service disruptions and degradations. All the checks that can be performed are very **service specific**. 

At the current state the *Cloud Integration capability of SAP Integration Suite* offers the possibility to monitor **exhausted JMS resources** and **expired certificates**.

### Benefit

The **benefit** of *SAP Cloud ALM* is to get an overview of the **health rating across all monitored Cloud Integration services** or even **across all connected services and systems of your IT landscape**. Operation teams benefit from this overview and can concentrate their efforts on the most important tasks and do not have to inspect all local monitoring tools separately. 

*Important*: Health monitoring does not offer any tools to update certificates or queues. This is only possible in the *keystore monitor* or *manage stores monitor* of Cloud Integration itself. 

### System preparation

- Several certificates have been uploaded that are partially already expired or will soon expire
- JMS queues have been created and filled with messages
- Some queues have been stopped to provoke critical states
- The queue sizes of some queues have been reduced to reach "earlier" the max capacity

<br>Continue to - [Exercise 4.1 - Bring a Cloud Integration service into scope](/exercises/ex4/ex41/)
