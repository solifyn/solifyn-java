

# LicensesCreateRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**productId** | **UUID** | The unique product identifier (internal product ID or ID) for which the license key will be issued. |  |
|**customerId** | **String** | The unique customer identifier (internal customer ID or ID) who will own this license key. |  |
|**activationLimit** | **Integer** | The maximum number of concurrent device or server activations allowed for this license key. |  [optional] |
|**expiryHours** | **Integer** | Relative validity period of the license in hours starting from the time of creation. |  [optional] |
|**key** | **String** | Optional custom license key string. If not provided, a random uppercase cryptographic serial key (e.g., ABCD-EFGH) will be generated automatically. |  [optional] |



