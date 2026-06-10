

# Discount

Represents a discount code created under your business, containing type, amount, usage limits, and expiration details.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | The unique prefix-based identifier of the discount (e.g., &#x60;disc_cs8f67sd7f6fw3fs&#x60;). |  |
|**discountId** | **String** | Alias for the unique identifier of the discount. |  |
|**code** | **String** | The unique discount code (e.g. SAVE10) used during checkout. |  |
|**name** | **String** | The customer-facing name of the discount code (e.g. Summer Sale). |  [optional] |
|**type** | [**TypeEnum**](#TypeEnum) | The discount calculation type: percentage or fixed_amount. |  |
|**amount** | **Integer** | The discount value. For percentage type, it is in basis points (e.g. 1000 &#x3D; 10.00%). For fixed_amount type, it is in cents (e.g. 1000 &#x3D; $10.00). |  |
|**usageLimit** | **Integer** | Maximum number of times this discount code can be redeemed. Null represents unlimited usage. |  |
|**timesUsed** | **Integer** | The number of times this discount code has been successfully redeemed. |  |
|**expiresAt** | **OffsetDateTime** | The expiration timestamp after which the discount code is no longer valid. |  |
|**status** | [**StatusEnum**](#StatusEnum) | The current status of the discount. |  |
|**businessId** | **String** | The unique identifier associated with the business this discount belongs to. |  |
|**createdAt** | **OffsetDateTime** | Timestamp indicating exactly when the discount was created. |  |
|**updatedAt** | **OffsetDateTime** | Timestamp indicating when the discount was last updated. |  |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| PERCENTAGE | &quot;percentage&quot; |
| FIXED_AMOUNT | &quot;fixed_amount&quot; |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| ACTIVE | &quot;active&quot; |
| EXPIRED | &quot;expired&quot; |



