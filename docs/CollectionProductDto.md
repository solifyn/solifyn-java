

# CollectionProductDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** | The unique identifier (ID) of the product. |  |
|**name** | **String** | The display name of the product. |  |
|**price** | **BigDecimal** | The price amount of the product (e.g. 29.00). |  |
|**currency** | **String** | The three-letter ISO currency code (e.g. USD, VND, EUR). |  |
|**description** | **String** | A comprehensive rich text description of the product. |  [optional] |
|**status** | **String** | The lifecycle status of the product (e.g. ACTIVE, ARCHIVED). |  |
|**imageUrl** | **String** | URL of the product cover image. |  |
|**taxCategory** | [**TaxCategoryEnum**](#TaxCategoryEnum) | The tax classification for the product. |  |
|**pricingType** | [**PricingTypeEnum**](#PricingTypeEnum) | Pricing model of the product. |  |
|**discount** | **BigDecimal** | Discount value as a percentage or fixed amount. |  |
|**hasLicenseKey** | **Boolean** | Indicates if the product issues a cryptographically secure software license key upon checkout completion. |  |
|**hasDigitalDelivery** | **Boolean** | Whether the product includes digital file downloads upon purchase. |  |
|**hasGithubAccess** | **Boolean** | Whether the product includes GitHub repository access. |  |
|**githubRepo** | **String** | GitHub repository to grant access to (format: owner/repo). |  |
|**githubPermission** | [**GithubPermissionEnum**](#GithubPermissionEnum) | GitHub collaborator permission level. |  |
|**hasDiscordAccess** | **Boolean** | Whether the product includes Discord role access. |  |
|**discordGuildId** | **String** | Discord Guild (Server) ID to grant access to. |  |
|**discordRoleId** | **String** | Discord Role ID to assign to the user. |  |
|**isTaxInclusive** | **Boolean** | Whether the product price already includes applicable sales taxes. |  |
|**billingPeriod** | **Integer** | The subscription billing cycle interval in days (for subscription products). |  |
|**trialPeriodDays** | **Integer** | Trial duration in days for subscription products. |  |
|**expirationDays** | **Integer** | Automatic expiration period in days for the subscription entitlement. |  |
|**statementDescriptor** | **String** | Custom text displayed on customer credit card statements for purchases of this product. |  |
|**payWhatYouWant** | **Boolean** | Indicates if customers are allowed to enter a custom pricing amount at checkout. |  |
|**metadata** | **Map&lt;String, String&gt;** | Custom developer metadata key-value pairs associated with the product. |  |
|**customFields** | **List&lt;Object&gt;** | Custom form field questions to ask the customer during checkout. |  |
|**stock** | **Integer** | Available stock quantity, or null for unlimited inventory. |  |
|**activationLimit** | **Integer** | Maximum number of simultaneous active instances/devices allowed per issued license key (applicable if hasLicenseKey is true). |  |
|**isListed** | **Boolean** | Defines if the product is listed publicly on the merchant&#39;s storefront template. |  |
|**isFree** | **Boolean** | Whether the product is free. |  |
|**createdAt** | **OffsetDateTime** | Timestamp indicating exactly when the product was created. |  |
|**updatedAt** | **OffsetDateTime** | Timestamp indicating when the product was last modified. |  |
|**isPermanentlyDeleted** | **Boolean** | Indicates if the product has been permanently deleted. |  |
|**brandId** | **String** | Optional brand identifier. |  |
|**digitalLink** | **String** | Secure link for digital delivery. |  |
|**instructions** | **String** | Special instructions provided upon purchase. |  |
|**activationMessage** | **String** | Custom message displayed when a license key is activated. |  |
|**expiryHours** | **Integer** | Number of hours until the license key expires. |  |
|**businessId** | **String** | The unique identifier of the business owning this product. |  |
|**quantity** | **BigDecimal** | Quantity of the product in the collection |  |



## Enum: TaxCategoryEnum

| Name | Value |
|---- | -----|
| DIGITAL_PRODUCTS | &quot;digital_products&quot; |
| SAAS | &quot;saas&quot; |
| PHYSICAL_PRODUCTS | &quot;physical_products&quot; |
| SERVICE | &quot;service&quot; |



## Enum: PricingTypeEnum

| Name | Value |
|---- | -----|
| USAGE_BASED | &quot;usage_based&quot; |
| ONE_TIME | &quot;one_time&quot; |
| RENEWAL | &quot;renewal&quot; |



## Enum: GithubPermissionEnum

| Name | Value |
|---- | -----|
| PULL | &quot;pull&quot; |
| TRIAGE | &quot;triage&quot; |
| PUSH | &quot;push&quot; |
| MAINTAIN | &quot;maintain&quot; |
| ADMIN | &quot;admin&quot; |



