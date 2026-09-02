

# ImportJobStatus


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **String** | Set only when the job failed. |  [optional]
**jobId** | **String** |  | 
**processed** | **Long** |  | 
**progress** | **Int** | 0–100 | 
**provider** | **String** | Which competitor the import came from (lexoffice | billbee); the frontend uses it to label the job. Absent for legacy jobs. |  [optional]
**stage** | **String** | queued | fetching | downloading | importing | done | 
**status** | **String** | pending | running | done | failed | 
**total** | **Long** |  | 



