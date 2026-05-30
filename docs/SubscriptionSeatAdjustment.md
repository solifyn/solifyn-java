

# SubscriptionSeatAdjustment

Represents the detailed cost and billing impact of adjusting subscription seat add-on quantities.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**success** | **Boolean** | Indicates if the seat adjustment was successful |  |
|**subscriptionId** | **String** | The customer subscription ID |  |
|**addonProductId** | **String** | The unique ID of the addon product |  |
|**oldQuantity** | **BigDecimal** | The previous seat quantity |  |
|**newQuantity** | **BigDecimal** | The new seat quantity after adjustment |  |
|**quantityDelta** | **BigDecimal** | The difference in seat quantity |  |
|**prorationType** | **String** | The proration strategy type applied |  |
|**costImpact** | **BigDecimal** | Calculated pro-rata price cost impact in currency unit (charged or credited) |  |
|**currency** | **String** | Billing currency |  |



