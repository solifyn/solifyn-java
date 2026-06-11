

# EntitlementGrantResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** | The unique entitlement grant ID. |  |
|**businessId** | **UUID** | The business ID context. |  |
|**customerId** | **UUID** | The customer ID. |  |
|**paymentId** | **UUID** | Associated payment transaction ID. |  [optional] |
|**productId** | **UUID** | The purchased product ID. |  |
|**type** | **String** | The type of entitlement (e.g. GITHUB, DISCORD, TELEGRAM). |  |
|**githubRepo** | **String** | Target GitHub repository (owner/repo) if type is GITHUB. |  [optional] |
|**githubPermission** | **String** | GitHub access permission level if type is GITHUB. |  [optional] |
|**githubUsername** | **String** | The connected customer GitHub username. |  [optional] |
|**discordGuildId** | **String** | Target Discord Guild ID if type is DISCORD. |  [optional] |
|**discordRoleId** | **String** | Target Discord Role ID if type is DISCORD. |  [optional] |
|**discordUsername** | **String** | The connected customer Discord username. |  [optional] |
|**discordUserId** | **String** | The connected customer Discord user ID. |  [optional] |
|**framerTemplateId** | **UUID** | The Framer template ID if type is FRAMER. |  [optional] |
|**framerRemixLink** | **String** | The single-use remix link generated for the customer if type is FRAMER. |  [optional] |
|**status** | **String** | Delivery status of the collaborator invite (PENDING, DELIVERED, FAILED, REVOKED). |  |
|**oauthUrl** | **String** | OAuth URL to redirect the customer to. |  [optional] |
|**errorDetails** | **String** | Error message if invitation delivery failed. |  [optional] |
|**metadata** | **Object** | Platform-specific metadata. |  [optional] |
|**createdAt** | **String** | Creation timestamp. |  |
|**updatedAt** | **String** | Modification timestamp. |  |



