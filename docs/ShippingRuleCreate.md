

# ShippingRuleCreate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**carrier** | **String** | Provider that auto-filled this rule (e.g. \&quot;ups\&quot;), if any. |  [optional]
**country** | **CountryCode** | None &#x3D; applies to all countries. |  [optional]
**deliveryTime** | **String** | Delivery time text, e.g. \&quot;1-3\&quot;. |  [optional]
**isActive** | **Boolean** |  |  [optional]
**maxWeightKg** | **Double** |  |  [optional]
**minWeightKg** | **Double** |  |  [optional]
**name** | **String** | Delivery-method label, e.g. \&quot;Standardversand\&quot;. | 
**notes** | **String** |  |  [optional]
**price** | **String** | Shipping cost in the shop&#39;s currency. | 
**priority** | **Int** | Lower wins when multiple rules match. |  [optional]



