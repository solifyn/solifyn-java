

# WebhookPaymentPayload


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Internal payment ID. |  [optional] |
|**status** | **String** |  |  [optional] |
|**substatus** | **String** |  |  [optional] |
|**customerId** | **String** |  |  [optional] |
|**customerEmail** | **String** |  |  [optional] |
|**customerName** | **String** |  |  [optional] |
|**customerUsername** | **String** |  |  [optional] |
|**productTitle** | **String** |  |  [optional] |
|**productRoute** | **String** |  |  [optional] |
|**planId** | **String** |  |  [optional] |
|**membershipId** | **String** |  |  [optional] |
|**membershipStatus** | **String** |  |  [optional] |
|**billingReason** | **String** |  |  [optional] |
|**amount** | **String** | Dollar value, 2 d.p. |  [optional] |
|**subtotal** | **String** |  |  [optional] |
|**usdTotal** | **String** |  |  [optional] |
|**feeAmount** | **String** |  |  [optional] |
|**amountAfterFees** | **String** |  |  [optional] |
|**taxAmount** | **String** |  |  [optional] |
|**taxBehavior** | **String** |  |  [optional] |
|**taxRefundedAmount** | **String** |  |  [optional] |
|**refundedAmount** | **String** |  |  [optional] |
|**settlementAmount** | **String** |  |  [optional] |
|**settlementCurrency** | **String** |  |  [optional] |
|**settlementExchangeRate** | **String** |  |  [optional] |
|**currency** | **String** |  |  [optional] |
|**refundable** | **Boolean** |  |  [optional] |
|**retryable** | **Boolean** |  |  [optional] |
|**autoRefunded** | **Boolean** |  |  [optional] |
|**paymentMethod** | **String** |  |  [optional] |
|**cardBrand** | **String** |  |  [optional] |
|**cardLast4** | **String** |  |  [optional] |
|**cardExpMonth** | **Integer** |  |  [optional] |
|**cardExpYear** | **Integer** |  |  [optional] |
|**billingAddress** | [**WebhookPaymentPayloadBillingAddress**](WebhookPaymentPayloadBillingAddress.md) |  |  [optional] |
|**licenseKey** | **String** |  |  [optional] |
|**filesSnapshot** | **List&lt;Object&gt;** |  |  [optional] |
|**checkoutId** | **String** |  |  [optional] |
|**discountCode** | **String** |  |  [optional] |
|**failureMessage** | **String** |  |  [optional] |
|**paidAt** | **OffsetDateTime** |  |  [optional] |
|**refundedAt** | **OffsetDateTime** |  |  [optional] |
|**disputeAlertedAt** | **OffsetDateTime** |  |  [optional] |
|**lastPaymentAttempt** | **OffsetDateTime** |  |  [optional] |
|**nextPaymentAttempt** | **OffsetDateTime** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |
|**updatedAt** | **OffsetDateTime** |  |  [optional] |
|**paymentEventType** | **String** |  |  [optional] |
|**lastEventType** | **String** |  |  [optional] |
|**businessId** | **String** |  |  [optional] |



