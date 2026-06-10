

# WebhookEntitlementGrantPayload


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** | The unique entitlement grant ID. |  [optional] |
|**businessId** | **UUID** | The business ID context. |  [optional] |
|**customerId** | **UUID** | The customer ID. |  [optional] |
|**paymentId** | **UUID** | Associated payment transaction ID. |  [optional] |
|**productId** | **UUID** | The purchased product ID. |  [optional] |
|**type** | **String** | The type of entitlement (e.g. GITHUB). |  [optional] |
|**githubRepo** | **String** | Target GitHub repository (owner/repo) if type is GITHUB. |  [optional] |
|**githubPermission** | **String** | GitHub access permission level if type is GITHUB. |  [optional] |
|**githubUsername** | **String** | The connected customer GitHub username. |  [optional] |
|**status** | **String** | Delivery status of the collaborator invite (PENDING, DELIVERED, FAILED, REVOKED). |  [optional] |
|**oauthUrl** | **String** | OAuth URL to redirect the customer to. |  [optional] |
|**errorDetails** | **String** | Error message if invitation delivery failed. |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |
|**updatedAt** | **OffsetDateTime** |  |  [optional] |



