

# EmployeeCreate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**address** | **String** |  |  [optional]
**backupEmployeeId** | **UUID** | References another employee who covers when this employee is absent. |  [optional]
**bic** | **String** |  |  [optional]
**city** | **String** |  |  [optional]
**country** | **CountryCode** |  |  [optional]
**dateOfBirth** | **LocalDate** |  |  [optional]
**departmentId** | **UUID** | References the department entity. |  [optional]
**email** | **String** |  |  [optional]
**firstName** | **String** |  |  [optional]
**gender** | **Gender** | Gender for pay-transparency reporting: \&quot;male\&quot;, \&quot;female\&quot; or \&quot;diverse\&quot;. |  [optional]
**hireDate** | **LocalDate** |  |  [optional]
**hourlyCost** | **String** | Hourly cost rate in EUR for labor-cost reporting; when unset the rate is derived from &#x60;monthly_salary / (weekly_hours * 4.33)&#x60;. |  [optional]
**iban** | **String** |  |  [optional]
**jobTitle** | **String** |  |  [optional]
**lastLogin** | **OffsetDateTime** |  |  [optional]
**lastName** | **String** |  |  [optional]
**lastUpdated** | **OffsetDateTime** |  |  [optional]
**monthlySalary** | **String** | Gross monthly salary in EUR for pay-transparency reporting. |  [optional]
**phone** | **String** |  |  [optional]
**state** | **String** |  |  [optional]
**status** | **EmployeeStatus** |  |  [optional]
**userId** | **UUID** | References the user entity. |  [optional]
**weeklyHours** | **String** | Contractual weekly working hours for pay-transparency normalization. |  [optional]
**zip** | **String** |  |  [optional]



