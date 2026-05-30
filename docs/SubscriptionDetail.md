

# SubscriptionDetail

Represents detailed information about a customer subscription including active base product configuration, billing and payment history, and purchased add-ons.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**subscription** | [**Subscription**](Subscription.md) | The main subscription details |  |
|**payments** | [**List&lt;Order&gt;**](Order.md) | The subscription payments / invoice billing history |  |
|**purchasedAddons** | [**List&lt;ResolvedAddon&gt;**](ResolvedAddon.md) | List of purchased addons associated with this subscription |  |
|**product** | [**SubscriptionDetailProduct**](SubscriptionDetailProduct.md) | The core product information associated with this subscription |  |



