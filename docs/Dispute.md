

# Dispute


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | The dispute ID |  |
|**whopId** | **String** | The Whop Dispute ID |  |
|**amount** | **BigDecimal** | The dispute amount |  |
|**currency** | **String** | The currency code |  |
|**status** | **String** | The status of the dispute |  |
|**reason** | **String** | The reason for the dispute |  [optional] |
|**editable** | **Boolean** | Whether the evidence is still editable |  |
|**needsResponseBy** | **OffsetDateTime** | Timestamp by when evidence must be submitted |  [optional] |
|**visaRdr** | **Boolean** | Whether Visa RDR was applied |  |
|**billingAddress** | **String** | Customer billing address details |  [optional] |
|**customerName** | **String** | Customer name |  [optional] |
|**customerEmail** | **String** | Customer email address |  [optional] |
|**notes** | **String** | Additional notes |  [optional] |
|**productDescription** | **String** | Product or service description |  [optional] |
|**serviceDate** | **String** | Service or purchase date |  [optional] |
|**accessActivityLog** | **String** | Log of access activity |  [optional] |
|**evidence** | [**DisputeEvidenceDto**](DisputeEvidenceDto.md) | Evidence attachments associated with the dispute |  [optional] |
|**paymentId** | **String** | The associated payment ID |  |
|**businessId** | **String** | The associated business ID |  |
|**createdAt** | **OffsetDateTime** | Timestamp when the dispute was created |  |
|**updatedAt** | **OffsetDateTime** | Timestamp when the dispute was last updated |  |



