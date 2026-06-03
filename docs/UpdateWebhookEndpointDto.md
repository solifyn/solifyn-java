

# UpdateWebhookEndpointDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**url** | **String** | The URL to send webhook events to. |  [optional] |
|**description** | **String** | Optional description for the webhook endpoint. |  [optional] |
|**events** | **List&lt;String&gt;** | The list of subscribed event types. |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) | The status of the webhook endpoint. |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| ACTIVE | &quot;ACTIVE&quot; |
| INACTIVE | &quot;INACTIVE&quot; |



