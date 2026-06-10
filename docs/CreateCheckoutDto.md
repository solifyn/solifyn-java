

# CreateCheckoutDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**productId** | **String** | The public product identifier (product ID) |  |
|**currency** | **String** | Three-letter ISO currency code (lowercase) |  [optional] |
|**quantity** | **BigDecimal** | The quantity of items to buy |  [optional] |
|**discountCode** | **String** | Discount code to apply |  [optional] |
|**customPrice** | **BigDecimal** | Custom price paid by customer (for Pay What You Want products) |  [optional] |
|**customerEmail** | **String** | Email address of the customer |  [optional] |
|**checkoutData** | **Object** | JSON metadata or checkout custom information |  [optional] |
|**customFields** | **Object** | Custom text fields required for the purchase |  [optional] |
|**aff** | **String** | Affiliate partner tracking code |  [optional] |
|**checkoutId** | **String** | The existing checkout database ID to validate / update |  [optional] |



