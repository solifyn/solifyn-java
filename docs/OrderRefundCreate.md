

# OrderRefundCreate


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**amount** | **Integer** | The refund amount in cents. If full refund is true, this can represent the total amount. |  |
|**isFullRefund** | **Boolean** | Whether this is a full refund or a partial refund. |  |
|**idempotencyKey** | **String** | A unique idempotency key to prevent double refunds for transient network retries. |  |
|**autoRevokeSeats** | **Boolean** | Whether to automatically revoke seat add-ons matching the refund amount. |  [optional] |
|**revokeSeats** | [**List&lt;RevokeSeatDto&gt;**](RevokeSeatDto.md) | List of specific addons and the quantities of seats to revoke. |  [optional] |



