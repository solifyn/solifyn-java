

# CreateEntitlementDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | The user-friendly name of the entitlement |  |
|**type** | [**TypeEnum**](#TypeEnum) | The type of access to grant |  |
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



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| GITHUB | &quot;GITHUB&quot; |
| DISCORD | &quot;DISCORD&quot; |
| FRAMER | &quot;FRAMER&quot; |
| LICENSE | &quot;LICENSE&quot; |
| DIGITAL | &quot;DIGITAL&quot; |



