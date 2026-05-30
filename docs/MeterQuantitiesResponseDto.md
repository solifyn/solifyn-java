

# MeterQuantitiesResponseDto

Represents aggregated usage quantities and calculated product costs for a meter within a selected date range.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**meterId** | **String** | The unique meter ID. |  |
|**name** | **String** | Meter display name. |  |
|**totalUsage** | **BigDecimal** | Total usage within the selected time range. |  |
|**costs** | [**List&lt;MeterQuantitiesCostDto&gt;**](MeterQuantitiesCostDto.md) | Cost breakdown for products attached to the meter. |  |



