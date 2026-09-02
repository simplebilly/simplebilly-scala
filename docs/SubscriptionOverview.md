

# SubscriptionOverview

Tenant subscription overview for the billing page: current plan, status, period end, trial state, effective limits, current usage and feature flags. Backed by Paddle Billing webhook data written into `billing_info` + `tenants.plan`, and by the canonical plans in `crate::saasy::plans`.  JSON contract (camelCase, matches the frontend): `plan`, `planName`, `priceEur`, `status`, `currentPeriodEnd`, `manageUrl`, `trialEndsAt`, `isTrialing`, `limits:{maxUsers,maxInvoicesPerMonth,maxConnectors}`, `usage:{users,invoicesThisMonth,connectors,overageSeats}`, `features:{taxAutomations,fancyReports,erp}`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currentPeriodEnd** | **OffsetDateTime** |  |  [optional]
**features** | [**PlanFeatures**](PlanFeatures.md) |  | 
**isTrialing** | **Boolean** |  | 
**limits** | [**PlanLimits**](PlanLimits.md) |  | 
**manageUrl** | **String** |  |  [optional]
**plan** | **String** | Resolved plan id (free/starter/business/enterprise, or a custom override id). | 
**planName** | **String** |  | 
**priceEur** | **Double** | Monthly price in EUR; &#x60;-1.0&#x60; &#x3D; custom pricing (enterprise). | 
**quantity** | **Int** |  |  [optional]
**status** | **String** |  |  [optional]
**subscriptionId** | **String** |  |  [optional]
**trialEndsAt** | **OffsetDateTime** |  |  [optional]
**usage** | [**UsageSnapshot**](UsageSnapshot.md) |  | 



