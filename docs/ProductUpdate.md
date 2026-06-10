

# ProductUpdate


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Product display name. |  [optional] |
|**description** | **String** | A description of the product. |  [optional] |
|**price** | **BigDecimal** | Price value. |  [optional] |
|**currency** | [**CurrencyEnum**](#CurrencyEnum) | Product pricing currency. |  [optional] |
|**imageUrl** | **String** | URL of the product cover image. |  [optional] |
|**taxCategory** | [**TaxCategoryEnum**](#TaxCategoryEnum) | Tax classification. |  [optional] |
|**discount** | **BigDecimal** | Percentage or flat rate discount. |  [optional] |
|**hasLicenseKey** | **Boolean** | Whether to automatically issue license keys upon successful orders. |  [optional] |
|**hasDigitalDelivery** | **Boolean** | Whether the purchase includes downloadable files. |  [optional] |
|**hasGithubAccess** | **Boolean** | Whether the purchase includes GitHub repository access. |  [optional] |
|**githubRepo** | **String** | GitHub repository to grant access to (format: owner/repo). |  [optional] |
|**githubPermission** | [**GithubPermissionEnum**](#GithubPermissionEnum) | GitHub collaborator permission level. |  [optional] |
|**hasDiscordAccess** | **Boolean** | Whether the purchase includes Discord server role access. |  [optional] |
|**discordGuildId** | **String** | Discord Guild (Server) ID to grant access to. |  [optional] |
|**discordRoleId** | **String** | Discord Role ID to assign to the user. |  [optional] |
|**isTaxInclusive** | **Boolean** | Whether tax is included in the base price. |  [optional] |
|**activationLimit** | **Integer** | Maximum concurrent activated instances allowed per license key. |  [optional] |
|**brandId** | **String** | Brand id for the product, if not provided will default to primary brand. |  [optional] |
|**billingPeriod** | **Integer** | Billing period in days (for Subscription products). |  [optional] |
|**trialPeriodDays** | **Integer** | Trial duration in days. |  [optional] |
|**expirationDays** | **Integer** | Subscription expiration duration in days. |  [optional] |
|**statementDescriptor** | **String** | Custom billing descriptor. |  [optional] |
|**payWhatYouWant** | **Boolean** | Allow pay-what-you-want pricing. |  [optional] |
|**metadata** | **Map&lt;String, String&gt;** | Developer key-value metadata pairs. |  [optional] |
|**customFields** | [**List&lt;ProductCreateCustomFieldsInner&gt;**](ProductCreateCustomFieldsInner.md) | Form field configurations to gather during checkout. |  [optional] |
|**stock** | **Integer** | Initial stock quantity limit. |  [optional] |
|**isListed** | **Boolean** | Whether the product is publicly visible. |  [optional] |
|**isFree** | **Boolean** | Whether the product is free of charge. |  [optional] |
|**addons** | [**List&lt;ProductCreateAddonsInner&gt;**](ProductCreateAddonsInner.md) | Product addons configurations. |  [optional] |



## Enum: CurrencyEnum

| Name | Value |
|---- | -----|
| USD | &quot;USD&quot; |
| SGD | &quot;SGD&quot; |
| INR | &quot;INR&quot; |
| AUD | &quot;AUD&quot; |
| BRL | &quot;BRL&quot; |
| CAD | &quot;CAD&quot; |
| DKK | &quot;DKK&quot; |
| EUR | &quot;EUR&quot; |
| NOK | &quot;NOK&quot; |
| GBP | &quot;GBP&quot; |
| SEK | &quot;SEK&quot; |
| CHF | &quot;CHF&quot; |
| HKD | &quot;HKD&quot; |
| HUF | &quot;HUF&quot; |
| JPY | &quot;JPY&quot; |
| MXN | &quot;MXN&quot; |
| MYR | &quot;MYR&quot; |
| PLN | &quot;PLN&quot; |
| CZK | &quot;CZK&quot; |
| NZD | &quot;NZD&quot; |
| AED | &quot;AED&quot; |
| COP | &quot;COP&quot; |
| RON | &quot;RON&quot; |
| THB | &quot;THB&quot; |
| BGN | &quot;BGN&quot; |
| IDR | &quot;IDR&quot; |
| DOP | &quot;DOP&quot; |
| PHP | &quot;PHP&quot; |
| TRY | &quot;TRY&quot; |
| KRW | &quot;KRW&quot; |
| TWD | &quot;TWD&quot; |
| VND | &quot;VND&quot; |
| PKR | &quot;PKR&quot; |
| CLP | &quot;CLP&quot; |
| UYU | &quot;UYU&quot; |
| ARS | &quot;ARS&quot; |
| ZAR | &quot;ZAR&quot; |
| DZD | &quot;DZD&quot; |
| TND | &quot;TND&quot; |
| MAD | &quot;MAD&quot; |
| KES | &quot;KES&quot; |
| KWD | &quot;KWD&quot; |
| JOD | &quot;JOD&quot; |
| ALL | &quot;ALL&quot; |
| XCD | &quot;XCD&quot; |
| AMD | &quot;AMD&quot; |
| BSD | &quot;BSD&quot; |
| BHD | &quot;BHD&quot; |
| BOB | &quot;BOB&quot; |
| BAM | &quot;BAM&quot; |
| KHR | &quot;KHR&quot; |
| CRC | &quot;CRC&quot; |
| XOF | &quot;XOF&quot; |
| EGP | &quot;EGP&quot; |
| ETB | &quot;ETB&quot; |
| GMD | &quot;GMD&quot; |
| GHS | &quot;GHS&quot; |
| GTQ | &quot;GTQ&quot; |
| GYD | &quot;GYD&quot; |
| ILS | &quot;ILS&quot; |
| JMD | &quot;JMD&quot; |
| MOP | &quot;MOP&quot; |
| MGA | &quot;MGA&quot; |
| MUR | &quot;MUR&quot; |
| MDL | &quot;MDL&quot; |
| MNT | &quot;MNT&quot; |
| NAD | &quot;NAD&quot; |
| NGN | &quot;NGN&quot; |
| MKD | &quot;MKD&quot; |
| OMR | &quot;OMR&quot; |
| PYG | &quot;PYG&quot; |
| PEN | &quot;PEN&quot; |
| QAR | &quot;QAR&quot; |
| RWF | &quot;RWF&quot; |
| SAR | &quot;SAR&quot; |
| RSD | &quot;RSD&quot; |
| LKR | &quot;LKR&quot; |
| TZS | &quot;TZS&quot; |
| TTD | &quot;TTD&quot; |
| UZS | &quot;UZS&quot; |
| RUB | &quot;RUB&quot; |
| CNY | &quot;CNY&quot; |



## Enum: TaxCategoryEnum

| Name | Value |
|---- | -----|
| DIGITAL_PRODUCTS | &quot;digital_products&quot; |
| SAAS | &quot;saas&quot; |
| PHYSICAL_PRODUCTS | &quot;physical_products&quot; |
| SERVICE | &quot;service&quot; |



## Enum: GithubPermissionEnum

| Name | Value |
|---- | -----|
| PULL | &quot;pull&quot; |
| TRIAGE | &quot;triage&quot; |
| PUSH | &quot;push&quot; |
| MAINTAIN | &quot;maintain&quot; |
| ADMIN | &quot;admin&quot; |



