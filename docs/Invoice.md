

# Invoice


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attachments** | **AnyType** |  |  [optional]
**billingPeriodEnd** | **LocalDate** |  |  [optional]
**billingPeriodStart** | **LocalDate** |  |  [optional]
**cancellationDate** | **LocalDate** |  |  [optional]
**cancellationInvoiceId** | **String** | References the invoice entity. |  [optional]
**cancellationReason** | **String** |  |  [optional]
**contractId** | **UUID** | References the contract entity. |  [optional]
**currency** | **CurrencyCode** |  | 
**customerId** | **String** | References the customer entity. |  [optional]
**discountAmount** | **String** |  |  [optional]
**discountDays** | **Int** |  |  [optional]
**discountPercentage** | **String** |  |  [optional]
**documentType** | **DocumentType** |  |  [optional]
**dunningLevel** | **Int** |  |  [optional]
**inputVatAmount** | **String** |  |  [optional]
**inputVatDeductible** | **Boolean** |  |  [optional]
**inputVatPercentage** | **String** |  |  [optional]
**introductionText** | **String** |  |  [optional]
**invoiceType** | **InvoiceType** |  | 
**isCancelled** | **Boolean** |  |  [optional]
**isDraft** | **Boolean** |  |  [optional]
**isEuAcquisition** | **Boolean** |  |  [optional]
**isEuDelivery** | **Boolean** |  |  [optional]
**isIntraCommunityAcquisition** | **Boolean** |  |  [optional]
**isReverseCharge** | **Boolean** |  |  [optional]
**issueDate** | **LocalDate** |  | 
**ledgerAccount** | **String** |  |  [optional]
**lineItems** | **AnyType** |  | 
**margin25a** | **Boolean** |  |  [optional]
**margin25aGross** | **String** |  |  [optional]
**margin25aPurchasePrice** | **String** |  |  [optional]
**notes** | **String** |  |  [optional]
**orderNumber** | **String** |  |  [optional]
**originalPdfPath** | **String** |  |  [optional]
**paidAmount** | **String** |  |  [optional]
**paymentDueDate** | **LocalDate** |  |  [optional]
**paymentStatus** | **PaymentStatus** |  |  [optional]
**paymentTermsText** | **String** |  |  [optional]
**precedingSalesVoucherId** | **String** | References the preceding sales voucher entity. |  [optional]
**precedingSalesVoucherType** | **PrecedingSalesVoucherType** |  |  [optional]
**receiptConfirmationAvailable** | **Boolean** |  |  [optional]
**relatedInvoiceId** | **UUID** | References the invoice entity. |  [optional]
**relationshipType** | **String** |  |  [optional]
**senderSnapshot** | **AnyType** |  |  [optional]
**sentAt** | **OffsetDateTime** |  |  [optional]
**servicePeriodEnd** | **LocalDate** |  |  [optional]
**servicePeriodStart** | **LocalDate** |  |  [optional]
**status** | **InvoiceStatus** |  | 
**subtotal** | **String** |  | 
**supplierId** | **String** | References the supplier entity. |  [optional]
**taxExemptionReason** | **String** |  |  [optional]
**totalAmount** | **String** |  | 
**totalTax** | **String** |  | 
**vatCountry** | **CountryCode** |  |  [optional]
**vatSpecialCase** | **String** |  |  [optional]



