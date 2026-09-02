

# DeliveryDateUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customerId** | **String** | References the customer entity. |  [optional]
**fulfilledDate** | **LocalDate** | Date actually delivered (set on fulfillment). |  [optional]
**note** | **String** |  |  [optional]
**orderNumber** | **String** | Sales order number (&#x60;order.order_number&#x60;). |  [optional]
**originalDate** | **LocalDate** | Original date promised before rescheduling. |  [optional]
**productId** | **String** | Product line item this date applies to, if per-item. References the product entity. |  [optional]
**promisedDate** | **LocalDate** | Date promised to the customer. |  [optional]
**status** | **DeliveryDateStatus** | One of: promised | confirmed | rescheduled | fulfilled | late | cancelled |  [optional]



