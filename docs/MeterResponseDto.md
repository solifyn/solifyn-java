

# MeterResponseDto

Represents a usage meter configured for event-based billing, including the tracked event name, aggregation strategy, optional filters, and archive status.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | The unique meter ID. |  |
|**businessId** | **String** | The business ID that owns this meter. |  |
|**name** | **String** | Meter display name. |  |
|**description** | **Object** | Meter description. |  [optional] |
|**eventName** | **String** | The event name tracked by this meter. |  |
|**aggregationType** | [**AggregationTypeEnum**](#AggregationTypeEnum) | Aggregation strategy for usage events. |  |
|**aggregationKey** | **Object** | Metadata key used for aggregation. |  [optional] |
|**unit** | **Object** | Measurement unit label. |  [optional] |
|**filters** | **Map&lt;String, Object&gt;** | Optional filter definition for advanced matching. |  [optional] |
|**archived** | **Boolean** | Whether the meter is archived. |  |
|**createdAt** | **OffsetDateTime** | Creation timestamp. |  |
|**updatedAt** | **OffsetDateTime** | Last update timestamp. |  |



## Enum: AggregationTypeEnum

| Name | Value |
|---- | -----|
| COUNT | &quot;COUNT&quot; |
| SUM | &quot;SUM&quot; |
| MAX | &quot;MAX&quot; |
| LAST | &quot;LAST&quot; |



