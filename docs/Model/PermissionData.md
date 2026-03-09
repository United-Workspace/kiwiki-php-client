# PermissionData

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**begins** | [**\DateTime**](\DateTime.md) | Start date of the permission without timezone offset. Europe/Berlin timezone is assumed. | [optional] 
**ends** | [**\DateTime**](\DateTime.md) | Expiration date of the permission without timezone offset. Europe/Berlin timezone is assumed. | [optional] 
**permission** | **string** | Access level | 
**sensors** | **int[]** | IDs of sensors that the permission should be granted for. | 
**timeofday_begins** | **string** | Start time of the permission on each day. Europe/Berlin timezone is assumed. | [optional] 
**timeofday_ends** | **string** | End time of the permission on each day. Europe/Berlin timezone is assumed. | [optional] 
**users** | **string[]** | Usernames/emails of users that the permission should be granted to. | 
**weekdays** | **string** | Weekdays on which the permission should be active. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


