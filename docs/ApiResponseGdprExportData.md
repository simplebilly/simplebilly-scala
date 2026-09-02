

# ApiResponseGdprExportData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**activityLog** | [**Seq&lt;GdprActivity&gt;**](GdprActivity.md) |  | 
**apiKeys** | [**Seq&lt;GdprApiKey&gt;**](GdprApiKey.md) | Key identifiers and names only — never a usable credential. | 
**billing** | [**Seq&lt;GdprBillingInfo&gt;**](GdprBillingInfo.md) |  | 
**exportedAt** | **OffsetDateTime** |  | 
**generatedByAi** | **Boolean** | Honesty field: this document is a plain data dump, never AI-generated. | 
**notifications** | [**Seq&lt;GdprNotification&gt;**](GdprNotification.md) |  | 
**refreshTokens** | [**Seq&lt;GdprRefreshToken&gt;**](GdprRefreshToken.md) | Session records: metadata only, never the token hash. | 
**tenants** | [**Seq&lt;GdprTenant&gt;**](GdprTenant.md) |  | 
**usageEvents** | [**Seq&lt;GdprUsageEvent&gt;**](GdprUsageEvent.md) |  | 
**user** | [**GdprUser**](GdprUser.md) |  | 



