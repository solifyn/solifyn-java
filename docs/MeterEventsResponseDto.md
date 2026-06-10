

# MeterEventsResponseDto

Represents a paginated-like response containing recent usage events recorded for a meter.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**meterId** | **String** | The unique meter ID. |  |
|**items** | [**List&lt;MeterUsageEventDto&gt;**](MeterUsageEventDto.md) | List of recent usage events. |  |
|**count** | **BigDecimal** | Number of returned usage events. |  |



