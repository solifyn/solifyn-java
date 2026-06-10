

# MeterIngestEventDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**eventId** | **String** | Unique usage event ID for idempotency. |  |
|**customerId** | **String** | Unique customer ID associated with the event. |  |
|**eventName** | **String** | Event name that should match a meter eventName. |  |
|**value** | **BigDecimal** | Event quantity value. |  [optional] |
|**metadata** | **Map&lt;String, Object&gt;** | Metadata attached to the usage event. |  [optional] |
|**timestamp** | **String** | Timestamp of the event in ISO 8601 format. |  [optional] |



