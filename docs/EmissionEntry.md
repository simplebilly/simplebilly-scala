

# EmissionEntry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**activityValue** | **String** | Activity amount in &#x60;unit&#x60; (kWh, l, km, t, tkm, EUR). | 
**categoryId** | **String** | GHG-Protocol category key, e.g. \&quot;purchased_goods\&quot;, \&quot;business_travel\&quot;. | 
**description** | **String** |  | 
**efSource** | **String** | Emission-factor source, e.g. \&quot;UBA-2024\&quot;, \&quot;DEFRA-2024\&quot;. | 
**efVersion** | **String** |  | 
**method** | **EmissionMethod** | \&quot;activity\&quot; | \&quot;spend\&quot; | \&quot;supplier\&quot;. | 
**scope** | **GhgScope** | GHG scope: \&quot;1\&quot; | \&quot;2\&quot; | \&quot;3\&quot;. | 
**tco2e** | **String** | Computed server-side: activity * factor / 1000, rounded to 4 dp. | 
**unit** | **String** | Unit of the activity value. | 
**updatedAt** | **OffsetDateTime** |  |  [optional]
**year** | **Int** | Reporting year. | 



