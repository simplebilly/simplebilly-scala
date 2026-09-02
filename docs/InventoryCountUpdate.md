

# InventoryCountUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**countDate** | **LocalDate** |  |  [optional]
**countNumber** | **String** |  |  [optional]
**lineItems** | **AnyType** | JSON array of &#x60;{product_id, name, sku, expected_quantity, counted_quantity, bin_location?, batch_number?, variance}&#x60;. |  [optional]
**notes** | **String** |  |  [optional]
**status** | **InventoryCountStatus** | One of: draft | counting | reviewed | posted |  [optional]
**warehouseId** | **String** | References the warehouse entity. |  [optional]



