

# Refund


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** | The refund ID |  |
|**whopId** | **String** | The Whop Refund ID |  |
|**idempotencyKey** | **String** | Client-generated key to prevent duplicate refunds |  [optional] |
|**amount** | **BigDecimal** | Refunded amount |  |
|**currency** | **String** | Currency code |  |
|**status** | [**StatusEnum**](#StatusEnum) | Status of the refund |  |
|**provider** | **String** | The payment provider used |  [optional] |
|**reason** | **String** | Reason for the refund |  [optional] |
|**referenceValue** | **String** | Acquirer Reference Number (ARN) or tracking number |  [optional] |
|**paymentId** | **UUID** | The associated Payment ID |  |
|**providerCreatedAt** | **OffsetDateTime** | Timestamp when the refund was processed by the provider |  [optional] |
|**createdAt** | **OffsetDateTime** | Timestamp when the refund was created in our system |  |
|**updatedAt** | **OffsetDateTime** | Timestamp when the refund was last updated |  |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;pending&quot; |
| SUCCEEDED | &quot;succeeded&quot; |
| FAILED | &quot;failed&quot; |
| CANCELED | &quot;canceled&quot; |



