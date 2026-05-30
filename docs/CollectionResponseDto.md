

# CollectionResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** | The collection ID |  |
|**name** | **String** | The name of the collection |  |
|**description** | **String** | A brief description of the collection |  [optional] |
|**imageUrl** | **String** | URL of the collection image |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) | Status of the collection |  |
|**businessId** | **String** | The unique identifier of the business owning this collection. |  |
|**isPermanentlyDeleted** | **Boolean** | Indicates if the collection has been permanently deleted. |  |
|**createdAt** | **OffsetDateTime** | Timestamp when the collection was created |  |
|**updatedAt** | **OffsetDateTime** | Timestamp when the collection was last updated |  |
|**products** | [**List&lt;CollectionProductRefDto&gt;**](CollectionProductRefDto.md) | List of product references (id + quantity). Full product details are available via GET /products/:id. |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| ACTIVE | &quot;ACTIVE&quot; |
| ARCHIVED | &quot;ARCHIVED&quot; |



