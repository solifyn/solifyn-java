

# SubscriptionsAction201Response


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | The unique ID of the subscription |  |
|**status** | **String** | The status of the subscription (e.g. completed, active, trialing, past_due, canceled) |  |
|**createdAt** | **OffsetDateTime** | Timestamp when the subscription was created |  |
|**joinedAt** | **OffsetDateTime** | Timestamp when the member joined |  |
|**updatedAt** | **OffsetDateTime** | Timestamp when the subscription was last updated |  |
|**manageUrl** | **String** | The management URL for the billing/subscription |  |
|**member** | [**SubscriptionMemberDto**](SubscriptionMemberDto.md) | The member details |  |
|**user** | [**SubscriptionUserDto**](SubscriptionUserDto.md) | The user details |  |
|**renewalPeriodStart** | **Object** | Start timestamp of the current renewal period |  |
|**renewalPeriodEnd** | **Object** | End timestamp of the current renewal period |  |
|**cancelAtPeriodEnd** | **Boolean** | Whether the subscription is set to cancel at the end of the billing period |  |
|**cancelOption** | **Object** | The cancel option details |  |
|**cancellationReason** | **Object** | The reason for cancellation |  |
|**canceledAt** | **Object** | Timestamp when the subscription was canceled |  |
|**currency** | **String** | Billing currency |  |
|**company** | [**SubscriptionCompanyDto**](SubscriptionCompanyDto.md) | The company context details |  |
|**plan** | [**SubscriptionPlanDto**](SubscriptionPlanDto.md) | The plan associated with this subscription |  |
|**promoCode** | **Object** | The promo code applied to the subscription |  |
|**product** | [**SubscriptionProductDto**](SubscriptionProductDto.md) | The product associated with the subscription |  |
|**licenseKey** | **Object** | The license key associated with this subscription |  |
|**metadata** | **Object** | Additional metadata for the subscription |  |
|**paymentCollectionPaused** | **Boolean** | Whether the payment collection is currently paused |  |
|**checkoutConfigurationId** | **String** | The checkout configuration ID used |  |
|**price** | **Object** | The price/amount of the membership |  [optional] |
|**type** | **Object** | The type of the membership plan |  [optional] |
|**customerId** | **Object** | The business customer ID |  [optional] |
|**success** | **Boolean** | Indicates if the seat adjustment was successful |  |
|**subscriptionId** | **String** | The customer subscription ID |  |
|**addonProductId** | **String** | The unique ID of the addon product |  |
|**oldQuantity** | **BigDecimal** | The previous seat quantity |  |
|**newQuantity** | **BigDecimal** | The new seat quantity after adjustment |  |
|**quantityDelta** | **BigDecimal** | The difference in seat quantity |  |
|**prorationType** | **String** | The proration strategy type applied |  |
|**costImpact** | **BigDecimal** | Calculated pro-rata price cost impact in currency unit (charged or credited) |  |



