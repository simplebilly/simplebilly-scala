

# Job


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attempts** | **Int** |  |  [optional]
**jobType** | **String** | Discriminator the worker dispatches on (e.g. \&quot;webhook.deliver\&quot;). | 
**maxAttempts** | **Int** |  | 
**payload** | **AnyType** |  |  [optional]
**runAt** | **OffsetDateTime** | Earliest execution time; None &#x3D; run now. |  [optional]
**status** | **JobStatus** | pending | running | done | failed | 



