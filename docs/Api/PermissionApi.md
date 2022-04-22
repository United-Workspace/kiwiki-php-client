# KiwiKi\PermissionApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1PermissionsPermissionIdDelete**](PermissionApi.md#v1PermissionsPermissionIdDelete) | **DELETE** /v1/permissions/{permission_id}/ | Delete a user - sensor permission.
[**v1PermissionsPermissionIdPut**](PermissionApi.md#v1PermissionsPermissionIdPut) | **PUT** /v1/permissions/{permission_id}/ | Edit a user - sensor permission.
[**v1PermissionsUserSensorPost**](PermissionApi.md#v1PermissionsUserSensorPost) | **POST** /v1/permissions/user/sensor/ | Create a new user - sensor permission


# **v1PermissionsPermissionIdDelete**
> v1PermissionsPermissionIdDelete($permission_id)

Delete a user - sensor permission.



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\PermissionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$permission_id = 56; // int | ID of the permission that should be deleted.

try {
    $apiInstance->v1PermissionsPermissionIdDelete($permission_id);
} catch (Exception $e) {
    echo 'Exception when calling PermissionApi->v1PermissionsPermissionIdDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **permission_id** | **int**| ID of the permission that should be deleted. |

### Return type

void (empty response body)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1PermissionsPermissionIdPut**
> v1PermissionsPermissionIdPut($permission_id, $permission_data)

Edit a user - sensor permission.



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\PermissionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$permission_id = 56; // int | ID of the permission that should be edited.
$permission_data = new \KiwiKi\Model\\KiwiKi\Model\PermissionData(); // \KiwiKi\Model\PermissionData | 

try {
    $apiInstance->v1PermissionsPermissionIdPut($permission_id, $permission_data);
} catch (Exception $e) {
    echo 'Exception when calling PermissionApi->v1PermissionsPermissionIdPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **permission_id** | **int**| ID of the permission that should be edited. |
 **permission_data** | [**\KiwiKi\Model\PermissionData**](../Model/.md)|  |

### Return type

void (empty response body)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1PermissionsUserSensorPost**
> \KiwiKi\Model\PermissionCreated v1PermissionsUserSensorPost($permission_data)

Create a new user - sensor permission

Creates a Permission for list of users (by their emails) and list of<br/>sensors (by their IDs)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\PermissionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$permission_data = new \KiwiKi\Model\\KiwiKi\Model\PermissionData(); // \KiwiKi\Model\PermissionData | 

try {
    $result = $apiInstance->v1PermissionsUserSensorPost($permission_data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PermissionApi->v1PermissionsUserSensorPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **permission_data** | [**\KiwiKi\Model\PermissionData**](../Model/.md)|  |

### Return type

[**\KiwiKi\Model\PermissionCreated**](../Model/PermissionCreated.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

