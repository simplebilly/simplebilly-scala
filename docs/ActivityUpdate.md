

# ActivityUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**activityType** | **ActivityType** | One of: call | email | meeting | task | note |  [optional]
**assignedTo** | **String** | User responsible (&#x60;employee.employee_id&#x60;). |  [optional]
**contactId** | **String** | Contact this activity belongs to (&#x60;contact.contact_id&#x60;). References the contact entity. |  [optional]
**description** | **String** |  |  [optional]
**dueDate** | **LocalDate** | Follow-up / Wiedervorlage date. Open activities with a due date in the past are overdue. |  [optional]
**reminderDate** | **LocalDate** | When to remind about the follow-up. |  [optional]
**status** | **ActivityStatus** | One of: open | done | cancelled |  [optional]
**subject** | **String** | Short subject line. |  [optional]



