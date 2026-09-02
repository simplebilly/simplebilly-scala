

# ProductionOrder


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bomId** | **UUID** | References the BOM entity. |  [optional]
**components** | **AnyType** | JSON snapshot of the BOM components at creation time. |  [optional]
**endDate** | **LocalDate** |  |  [optional]
**notes** | **String** |  |  [optional]
**orderNumber** | **String** |  | 
**productId** | **UUID** | The finished product to manufacture. References the product entity. | 
**quantity** | **Long** | Quantity of finished product to produce. | 
**sourceWarehouseId** | **String** | Warehouse components are consumed from. References the warehouse entity. |  [optional]
**startDate** | **LocalDate** |  |  [optional]
**status** | **ProductionOrderStatus** | One of: planned | in_production | completed | cancelled |  [optional]
**targetWarehouseId** | **String** | Warehouse the finished product is added to. References the warehouse entity. |  [optional]



