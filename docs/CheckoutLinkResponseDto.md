

# CheckoutLinkResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** | The checkout link ID |  |
|**title** | **String** | The title of the checkout link |  [optional] |
|**productId** | **String** | The linked Product ID |  [optional] |
|**collectionId** | **String** | The linked Collection ID |  [optional] |
|**customerName** | **String** | Pre-filled customer name |  [optional] |
|**customerEmail** | **String** | Pre-filled customer email |  [optional] |
|**addressLine1** | **String** | Pre-filled address line 1 |  [optional] |
|**city** | **String** | Pre-filled city |  [optional] |
|**state** | **String** | Pre-filled state |  [optional] |
|**postalCode** | **String** | Pre-filled postal code |  [optional] |
|**country** | **String** | Pre-filled country |  [optional] |
|**quantity** | **BigDecimal** | Quantity to purchase |  |
|**redirectUrl** | **String** | URL to redirect to after successful payment |  [optional] |
|**cancelUrl** | **String** | URL to redirect to if payment is cancelled |  [optional] |
|**showDiscounts** | **Boolean** | Whether to show discounts on the checkout page |  |
|**createdAt** | **OffsetDateTime** | Timestamp when the link was created |  |
|**updatedAt** | **OffsetDateTime** | Timestamp when the link was last updated |  |



