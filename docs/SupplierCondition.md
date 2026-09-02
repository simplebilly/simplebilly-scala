

# SupplierCondition


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **String** | Currency for the minimum order value. | 
**deliveryTerms** | **String** | Incoterms, e.g. \&quot;EXW\&quot;, \&quot;DAP\&quot;. |  [optional]
**earlyPaymentDiscountPercent** | **String** | Early-payment discount percentage (Skonto), e.g. 2.0. |  [optional]
**isDefault** | **Boolean** | Is this the default condition for the supplier? |  [optional]
**minimumOrderValue** | **String** | Minimum order value required for this supplier. |  [optional]
**notes** | **String** |  |  [optional]
**paymentDueDays** | **Int** | Number of days within which payment is due. |  [optional]
**paymentTerms** | **String** | Payment terms, e.g. \&quot;14 Tage, 2% Skonto\&quot;. |  [optional]
**supplierContactId** | **String** | The supplier this condition applies to (&#x60;contact_id&#x60;). References the supplier entity. | 
**supplierName** | **String** | The name of the supplier, denormalized for easy listing. |  [optional]
**volumeDiscountTiers** | **AnyType** | Tiered discounts: JSON array of &#x60;{min_quantity, discount_percent}&#x60;. |  [optional]



