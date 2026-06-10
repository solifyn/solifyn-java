

# License

Represents a cryptographically secure software license key issued to a customer upon purchase or manual issuance.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | The unique prefix-based identifier of the license key. |  |
|**key** | **String** | The cryptographically generated license key string delivered to the customer. |  |
|**status** | [**StatusEnum**](#StatusEnum) | Lifecycle status of the license. ACTIVE &#x3D; active. DISABLED &#x3D; suspended. REVOKED &#x3D; hard-revoked. |  |
|**businessId** | **String** | The unique identifier associated with the business this license belongs to. |  |
|**productId** | **String** | The unique ID of the product this license key is associated with. |  |
|**paymentId** | **String** | The unique payment identifier that triggered the issuance of this license key. |  |
|**customerId** | **String** | The unique customer identifier (ID) who received this license key. |  |
|**activationLimit** | **BigDecimal** | Maximum number of simultaneous active device instances allowed for this license. Null means unlimited. |  |
|**activationMessage** | **String** | Optional message displayed to the customer upon successful activation. |  |
|**instancesCount** | **BigDecimal** | Running count of how many times this license key has been activated. |  |
|**expiryHours** | **BigDecimal** | Relative expiry duration in hours from the time of issuance. |  |
|**expiresAt** | **String** | Absolute expiration timestamp. The license becomes invalid after this point. |  |
|**filters** | **Object** | Optional custom metadata filters associated with the license. |  |
|**archived** | **Boolean** | Indicates if the license key is archived. |  |
|**createdAt** | **String** | Timestamp indicating exactly when the license key was issued. |  |
|**updatedAt** | **String** | Timestamp indicating when the license key was last modified. |  |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| ACTIVE | &quot;ACTIVE&quot; |
| DISABLED | &quot;DISABLED&quot; |
| REVOKED | &quot;REVOKED&quot; |



