

# JobApplication


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cvFile** | **String** | Relative path of the stored CV file under the upload dir. |  [optional]
**cvText** | **String** | Extracted CV text, used for match-scoring. |  [optional]
**email** | **String** |  |  [optional]
**matchReason** | **String** |  |  [optional]
**matchScore** | **Int** | 0-100 LLM match score against the posting&#39;s required profile. |  [optional]
**name** | **String** |  |  [optional]
**phone** | **String** |  |  [optional]
**postingId** | **UUID** | References the job_posting entity. |  [optional]
**source** | **String** | website | email | board | 
**status** | **ApplicationStatus** | new | reviewing | interview | hired | rejected | 



