

# SubscriptionAction


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**freeDays** | **BigDecimal** | Number of free days to add (used with action: add_free_days) |  [optional] |
|**cancellationMode** | [**CancellationModeEnum**](#CancellationModeEnum) | Cancellation mode (used with action: cancel) |  [optional] |
|**voidPayments** | **Boolean** | Whether to void subsequent payments (used with action: pause) |  [optional] |
|**addonProductId** | **String** | ID of the addon product to adjust seats for (used with action: adjust_seats) |  [optional] |
|**newQuantity** | **BigDecimal** | The new seat quantity (used with action: adjust_seats) |  [optional] |
|**prorationType** | [**ProrationTypeEnum**](#ProrationTypeEnum) | Proration strategy mode (used with action: adjust_seats) |  [optional] |
|**idempotencyKey** | **String** | A unique idempotency key to prevent duplicate mutative actions for network transient retries. |  [optional] |



## Enum: CancellationModeEnum

| Name | Value |
|---- | -----|
| IMMEDIATE | &quot;immediate&quot; |
| AT_PERIOD_END | &quot;at_period_end&quot; |



## Enum: ProrationTypeEnum

| Name | Value |
|---- | -----|
| PRORATED_IMMEDIATELY | &quot;prorated_immediately&quot; |
| FULL_IMMEDIATELY | &quot;full_immediately&quot; |
| DIFFERENCE_IMMEDIATELY | &quot;difference_immediately&quot; |
| DO_NOT_BILL | &quot;do_not_bill&quot; |



