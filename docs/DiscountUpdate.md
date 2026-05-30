

# DiscountUpdate


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Customer-facing name of the discount. |  [optional] |
|**type** | [**TypeEnum**](#TypeEnum) | Calculation type: percentage or fixed_amount. |  [optional] |
|**amount** | **BigDecimal** | The discount value. |  [optional] |
|**usageLimit** | **Integer** | Maximum number of redemptions allowed. |  [optional] |
|**expiresAt** | **OffsetDateTime** | Expiration timestamp for the discount. |  [optional] |
|**subscriptionCycles** | **Integer** | Number of subscription cycles this discount applies to. |  [optional] |
|**restrictedTo** | **List&lt;String&gt;** | List of product IDs this discount is restricted to. |  [optional] |
|**preserveOnPlanChange** | **Boolean** | Whether to preserve the discount when subscription plan changes. |  [optional] |
|**metadata** | **Object** | Custom metadata for the discount. |  [optional] |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| PERCENTAGE | &quot;percentage&quot; |
| FIXED_AMOUNT | &quot;fixed_amount&quot; |



