

# ConfigFieldInfo

Owned, API-safe copy of a [`ConfigField`] for DTOs / OpenAPI ([`ConfigField`] borrows `&'static str`, which cannot round-trip `Deserialize`).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | [**ConfigFieldKind**](ConfigFieldKind.md) |  | 
**label** | **String** |  | 
**name** | **String** |  | 
**placeholder** | **String** |  |  [optional]
**required** | **Boolean** |  | 



