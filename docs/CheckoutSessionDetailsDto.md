

# CheckoutSessionDetailsDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Checkout session identifier |  |
|**price** | **BigDecimal** | Total purchase amount |  |
|**currency** | **String** | ISO currency code of the purchase |  |
|**storeName** | **String** | Title or name of the merchant/store selling the item |  |
|**status** | **String** | Current status of the checkout session |  |
|**billingAddress** | **Object** | Customer billing address details |  [optional] |
|**customFields** | **Object** | Custom fields collected during purchase |  [optional] |
|**sessionId** | **String** | The payment partner session ID |  [optional] |
|**paymentId** | **String** | Database payment transaction ID |  [optional] |
|**checkoutUrl** | **String** | Checkout session redirect URL if loaded in link mode |  [optional] |
|**product** | [**Product**](Product.md) | The details of the product being purchased |  [optional] |
|**entitlementGrants** | **List&lt;Object&gt;** | List of entitlement grants (e.g. GitHub repo invites) associated with this checkout. |  [optional] |



