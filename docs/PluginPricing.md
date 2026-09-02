

# PluginPricing

How a plugin is priced in the marketplace. Tagged on `type` so the same enum deserializes both the API DTO and the `plugin_marketplace.json` manifest (`{\"type\":\"free\"}` / `{\"type\":\"one_time\",\"price\":99.0}` / `{\"type\":\"recurring\",\"price_per_month\":19.9}`).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**`type`** | [**`Type`**](#`Type`) |  | 
**price** | **Double** |  | 
**pricePerMonth** | **Double** |  | 


## Enum: `Type`
Allowed values: [free, one_time, recurring]




