

# MeterUsageEventDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | The unique usage event ID. |  |
|**meterId** | **String** | The meter ID this event belongs to. |  |
|**customerId** | **String** | The customer ID associated with the usage event. |  |
|**value** | **BigDecimal** | Numeric usage value recorded for the event. |  |
|**metadata** | **Map&lt;String, Object&gt;** | Optional event metadata. |  [optional] |
|**timestamp** | **OffsetDateTime** | Timestamp when the usage event occurred. |  |
|**processedAt** | **OffsetDateTime** | Timestamp when the usage event was processed. |  |



