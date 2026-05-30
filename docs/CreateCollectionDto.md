

# CreateCollectionDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | The friendly name of the collection |  |
|**description** | **String** | A detailed description of this collection |  [optional] |
|**imageUrl** | **String** | The display cover image URL for this collection |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) | The collection status |  [optional] |
|**products** | [**List&lt;CollectionProductEntry&gt;**](CollectionProductEntry.md) | List of products to include in this collection. At least one product is required. |  |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| ACTIVE | &quot;ACTIVE&quot; |
| ARCHIVED | &quot;ARCHIVED&quot; |



