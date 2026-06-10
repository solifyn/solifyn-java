

# Instance

Represents an active device or software instance that has been activated against a license key.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | The unique database identifier of this instance record. |  |
|**licenseId** | **String** | The internal ID of the parent license key this instance belongs to. |  |
|**instanceId** | **String** | The unique hardware hash or client-generated identifier of the activated device/machine. |  |
|**instanceName** | **String** | A human-readable display name for this instance, assigned by the client application. |  |
|**ipAddress** | **String** | The IP address recorded at the time of activation. |  |
|**activatedAt** | **String** | Timestamp when this device instance was first activated. |  |
|**lastSeenAt** | **String** | Timestamp of the most recent activation heartbeat or re-activation check from this device. |  |



