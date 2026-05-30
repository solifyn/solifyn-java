

# Withdrawal


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | The local withdrawal ID |  |
|**whopId** | **String** | The Whop withdrawal ID |  |
|**amount** | **BigDecimal** | The amount withdrawn in cents |  |
|**currency** | **String** | Three-letter ISO currency code |  |
|**status** | **String** | The status of the withdrawal request |  |
|**feeAmount** | **BigDecimal** | Fee amount charged for the withdrawal in cents |  [optional] |
|**feeType** | **String** | The fee structure type (inclusive or exclusive) |  [optional] |
|**markupFee** | **BigDecimal** | Markup fee applied in cents |  [optional] |
|**speed** | **String** | Speed of withdrawal (standard, instant) |  [optional] |
|**traceCode** | **String** | Bank trace or reference code for tracking the payout |  [optional] |
|**payerName** | **String** | The name of the entity or account paying out |  [optional] |
|**errorMessage** | **String** | Error message if the withdrawal failed |  [optional] |
|**businessId** | **String** | The business ID associated with this withdrawal |  |
|**createdAt** | **OffsetDateTime** | Timestamp when the withdrawal was requested |  |
|**updatedAt** | **OffsetDateTime** | Timestamp when the withdrawal status was updated |  |



