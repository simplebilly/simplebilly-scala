

# QuotaOverride

Schema of the `tenants.quotas` JSON override column. Any field that is present overrides the plan-derived value.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**features** | [**QuotaOverrideFeatures**](QuotaOverrideFeatures.md) |  |  [optional]
**maxConnectors** | **Int** |  |  [optional]
**maxInvoicesPerMonth** | **Long** |  |  [optional]
**maxUsers** | **Int** |  |  [optional]
**metered** | **Map&lt;String, Long&gt;** |  |  [optional]
**plan** | **String** | Custom plan id; unknown ids resolve to enterprise limits. |  [optional]



