

# UpdateCheckoutLinkDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**title** | **String** | The friendly display title of this checkout link |  [optional] |
|**productId** | **String** | Product database/Whop ID to sell |  [optional] |
|**collectionId** | **String** | Optional collection database ID to sell |  [optional] |
|**customerName** | **String** | Prefilled customer name for checkout inputs |  [optional] |
|**customerEmail** | **String** | Prefilled customer email for checkout inputs |  [optional] |
|**addressLine1** | **String** | Prefilled customer billing address line 1 |  [optional] |
|**city** | **String** | Prefilled customer billing city |  [optional] |
|**state** | **String** | Prefilled customer billing state |  [optional] |
|**postalCode** | **String** | Prefilled customer billing zip/postal code |  [optional] |
|**country** | **String** | Prefilled customer billing country (2-letter ISO) |  [optional] |
|**quantity** | **Object** | Override quantity for checkout session |  [optional] |
|**redirectUrl** | **String** | The absolute URL to redirect to upon successful payment completion |  [optional] |
|**cancelUrl** | **String** | The absolute URL to redirect to if a customer cancels the payment |  [optional] |
|**showDiscounts** | **Boolean** | Whether to display discount input form fields on checkout screen |  [optional] |



