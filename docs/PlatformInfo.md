

# PlatformInfo

Public metadata for one registered plugin (admin UI). Maps 1:1 from [`plugin_core::PluginInfo`] (same field shape as before).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**author** | **String** |  | 
**changelog** | [**Seq&lt;ChangelogEntry&gt;**](ChangelogEntry.md) |  | 
**configFieldNames** | **Seq&lt;String&gt;** |  | 
**configFields** | [**Seq&lt;ConfigFieldInfo&gt;**](ConfigFieldInfo.md) |  | 
**displayName** | **String** |  | 
**platform** | **String** |  | 
**pricing** | [**PluginPricing**](PluginPricing.md) |  | 
**supportedEntities** | **Seq&lt;String&gt;** |  | 
**supportsExport** | **Boolean** |  | 
**supportsImport** | **Boolean** |  | 
**supportsOauth** | **Boolean** |  | 
**version** | **String** |  | 



