

# Order

Represents an order (payment) processed under your business, containing customer, billing, product cart, and refund details.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique internal database identifier. |  |
|**invoiceUrl** | **String** | The invoice print URL. |  |
|**customer** | [**OrderCustomer**](OrderCustomer.md) | Customer details. |  |
|**totalAmount** | **Integer** | Total paid amount in cents. |  |
|**subtotal** | **Integer** | Subtotal amount in cents. |  |
|**usdTotal** | **BigDecimal** | Total paid amount converted to USD. |  [optional] |
|**taxAmount** | **Integer** | Tax amount in cents. |  |
|**applicationFee** | **Integer** | Application fee in cents. |  |
|**amountAfterFees** | **Integer** | Net amount after fees in cents. |  |
|**currency** | **String** | Currency code. |  |
|**status** | **String** | Current status of the payment. |  |
|**createdAt** | **OffsetDateTime** | Payment creation timestamp. |  |
|**paidAt** | **OffsetDateTime** | Payment completion/paid timestamp. |  [optional] |
|**paymentMethod** | **String** | Payment method utilized. |  |
|**cardLastFour** | **String** | Last four digits of card used. |  [optional] |
|**cardNetwork** | **String** | Card network/brand. |  [optional] |
|**cardType** | **String** | Card type. |  [optional] |
|**billing** | [**OrderBilling**](OrderBilling.md) | Billing address details. |  [optional] |
|**productCart** | [**List&lt;OrderProductCart&gt;**](OrderProductCart.md) | Products purchased in this order. |  |
|**metadata** | **Object** | Custom metadata payload associated with this payment. |  [optional] |
|**order** | [**OrderDetail**](OrderDetail.md) | Order details snapshot. |  [optional] |
|**refundable** | **Boolean** | Indicates whether the order is eligible for refund. |  |
|**refunds** | [**List&lt;OrderRefund&gt;**](OrderRefund.md) | List of refunds associated with this payment. |  [optional] |
|**businessId** | **String** | Business unique ID identifier. |  |
|**businessName** | **String** | Business display title/name. |  |
|**billingReason** | **String** | Billing reason detail. |  [optional] |



