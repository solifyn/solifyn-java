

# OperationalWebhookEndpointInDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**url** | **String** | The URL to send webhook events to. |  |
|**description** | **String** | Optional description for the endpoint. |  [optional] |
|**disabled** | **Boolean** | Whether the endpoint is disabled. |  [optional] |
|**filterTypes** | **List&lt;String&gt;** | The operational event types this endpoint will receive. |  [optional] |
|**metadata** | **Object** | Metadata key-value pairs associated with the endpoint. |  [optional] |
|**secret** | **String** | Optional custom endpoint signing secret (base64 encoded random bytes optionally prefixed with whsec_). If not set, the server will generate one. |  [optional] |
|**throttleRate** | **BigDecimal** | Maximum messages per second to send to this endpoint (outgoing messages will be throttled to this rate). |  [optional] |
|**uid** | **String** | Optional unique user-defined identifier for the endpoint. |  [optional] |



