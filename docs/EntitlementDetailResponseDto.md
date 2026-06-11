

# EntitlementDetailResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | The unique entitlement ID |  |
|**businessId** | **String** | The owning business ID |  |
|**name** | **String** | The name of the entitlement |  |
|**type** | **String** | The type of access to grant |  |
|**status** | **String** | Status of the entitlement |  |
|**createdAt** | **OffsetDateTime** | When the entitlement was created |  |
|**updatedAt** | **OffsetDateTime** | When the entitlement was last updated |  |
|**githubRepo** | **String** | The GitHub repository (e.g., owner/repo) |  [optional] |
|**githubPermission** | **String** | The GitHub repository permission level |  [optional] |
|**discordGuildId** | **String** | The Discord Guild/Server ID |  [optional] |
|**discordRoleId** | **String** | The Discord Role ID to assign |  [optional] |
|**framerTemplateId** | **String** | The associated Framer Template ID |  [optional] |
|**licenseKey** | **String** | The static License Key (if not dynamically generated) |  [optional] |
|**activationLimit** | **BigDecimal** | The maximum activation limit for licenses |  [optional] |
|**activationMessage** | **String** | A message shown to the user upon license activation |  [optional] |
|**expiryHours** | **BigDecimal** | The number of hours until the entitlement expires |  [optional] |
|**digitalLink** | **String** | The digital download URL or redirect link |  [optional] |
|**instructions** | **String** | Custom setup instructions for the user |  [optional] |
|**grantsCount** | **BigDecimal** | Number of active customer grants issued from this entitlement |  |
|**products** | [**List&lt;LinkedProductDto&gt;**](LinkedProductDto.md) | Products that are currently linked to this entitlement |  |



