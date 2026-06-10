

# UpdateMeterDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Meter display name. |  [optional] |
|**description** | **String** | Meter description. |  [optional] |
|**eventName** | **String** | The event name tracked by this meter. |  [optional] |
|**aggregationType** | [**AggregationTypeEnum**](#AggregationTypeEnum) | Aggregation strategy for usage events. |  [optional] |
|**aggregationKey** | **String** | Metadata key used by SUM, MAX, or LAST aggregation modes. |  [optional] |
|**unit** | **String** | Measurement unit label. |  [optional] |
|**filters** | **Map&lt;String, Object&gt;** | Optional filter definition for advanced matching. |  [optional] |
|**enableFiltering** | **Boolean** | Enable filtering on usage event ingestion. |  [optional] |



## Enum: AggregationTypeEnum

| Name | Value |
|---- | -----|
| COUNT | &quot;COUNT&quot; |
| SUM | &quot;SUM&quot; |
| MAX | &quot;MAX&quot; |
| LAST | &quot;LAST&quot; |



