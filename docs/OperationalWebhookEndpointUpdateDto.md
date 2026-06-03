

# OperationalWebhookEndpointUpdateDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**url** | **String** | The URL to send webhook events to. |  |
|**description** | **String** | Optional description for the endpoint. |  [optional] |
|**disabled** | **Boolean** | Whether the endpoint is disabled. |  [optional] |
|**filterTypes** | **List&lt;String&gt;** | The operational event types this endpoint will receive. |  [optional] |
|**metadata** | **Object** | Metadata key-value pairs associated with the endpoint. |  [optional] |
|**throttleRate** | **BigDecimal** | Maximum messages per second to send to this endpoint. |  [optional] |
|**uid** | **String** | Optional unique user-defined identifier for the endpoint. |  [optional] |



