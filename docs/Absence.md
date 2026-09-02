

# Absence


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**absenceType** | **AbsenceType** | One of \&quot;vacation\&quot;, \&quot;sick\&quot;, \&quot;sabbatical\&quot;, \&quot;parental\&quot;, \&quot;other\&quot;. |  [optional]
**approvedAt** | **OffsetDateTime** |  |  [optional]
**approvedBy** | **UUID** | References the user entity. |  [optional]
**createdAt** | **OffsetDateTime** |  |  [optional]
**deletedAt** | **OffsetDateTime** |  |  [optional]
**employeeId** | **UUID** | References the employee entity. |  [optional]
**endDate** | **LocalDate** |  |  [optional]
**id** | **UUID** |  |  [optional]
**notes** | **String** |  |  [optional]
**startDate** | **LocalDate** |  |  [optional]
**status** | **AbsenceStatus** | One of \&quot;pending\&quot;, \&quot;approved\&quot;, \&quot;rejected\&quot;, \&quot;cancelled\&quot;. |  [optional]
**tenantId** | **UUID** |  |  [optional]
**updatedAt** | **OffsetDateTime** |  |  [optional]



