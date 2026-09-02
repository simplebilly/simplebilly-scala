

# ServiceJobCreate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**address** | **String** | Street + zip + city of the job location. |  [optional]
**customerEmail** | **String** | Customer email for email notifications. |  [optional]
**customerId** | **UUID** | References the customer entity. |  [optional]
**customerName** | **String** | Denormalized customer name for quick display. |  [optional]
**customerPhone** | **String** | Customer phone for SMS notifications later. |  [optional]
**description** | **String** | What work needs to be done. |  [optional]
**estimatedDurationMinutes** | **Int** | Estimated time for the job in minutes. |  [optional]
**lat** | **Double** | Latitude for map display (OpenStreetMap). |  [optional]
**lng** | **Double** | Longitude for map display (OpenStreetMap). |  [optional]
**notes** | **String** |  |  [optional]
**status** | **ServiceJobStatus** | Dispatch status: \&quot;pending\&quot;, \&quot;assigned\&quot;, \&quot;en_route\&quot;, \&quot;in_progress\&quot;, \&quot;completed\&quot;, \&quot;cancelled\&quot;. |  [optional]



