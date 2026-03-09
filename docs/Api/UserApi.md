# KiwiKi\UserApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1UsersPermissionsGet**](UserApi.md#v1UsersPermissionsGet) | **GET** /v1/users/permissions/ | Get user permissions
[**v1UsersPost**](UserApi.md#v1UsersPost) | **POST** /v1/users/ | Create a new user account
[**v1UsersUserIdEmailDelete**](UserApi.md#v1UsersUserIdEmailDelete) | **DELETE** /v1/users/{user_id}/email/ | Remove a user&#39;s email address
[**v1UsersUserIdEmailPut**](UserApi.md#v1UsersUserIdEmailPut) | **PUT** /v1/users/{user_id}/email/ | Change a user&#39;s email address
[**v1UsersUserIdGet**](UserApi.md#v1UsersUserIdGet) | **GET** /v1/users/{user_id}/ | Get detailed user information
[**v1UsersUserIdMoveOutPost**](UserApi.md#v1UsersUserIdMoveOutPost) | **POST** /v1/users/{user_id}/move/out/ | Move tenant out of an organization


# **v1UsersPermissionsGet**
> \KiwiKi\Model\UserPermissionsResult v1UsersPermissionsGet($user_id, $begins, $ends, $timing_state, $specifier, $street, $postal_code, $city, $granted, $granted_by, $include_created_permissions, $inactive_since, $include_deleted, $page_size, $page_number, $sort_by, $order_by)

Get user permissions

Get the list of permissions that a user has over sensors.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 56; // int | ID of the user, whose permissions should be returned. If omitted, permissions of session user are returned.
$begins = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Filter by date time range. Permissions that overlap with the specified timespan (inclusive) will be included in the result (see `ends` parameter). Timezone needs to be specified.
$ends = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Filter by date time range. Permissions that overlap with the specified timespan (inclusive) will be included in the result (see `begins` parameter). Timezone needs to be specified.
$timing_state = array("timing_state_example"); // string[] | Filter by timing state of a permission.
$specifier = "specifier_example"; // string | Filter by specifier of a permission's sensor.
$street = "street_example"; // string | Filter by street name of the address of a permission's sensor.
$postal_code = new \stdClass; // object | Filter by postal code of the address of a permission's sensor.
$city = "city_example"; // string | Filter by city of the address of a permission's sensor.
$granted = array("granted_example"); // string[] | Filter by permission type.
$granted_by = "granted_by_example"; // string | Filter by username/email of the user that granted a permission.
$include_created_permissions = false; // bool | Include permissions created by the user.
$inactive_since = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Include permissions that are inactive since a certain point of time.
$include_deleted = false; // bool | Include deleted permissions.
$page_size = 20; // int | Maximal number of items per page.
$page_number = 1; // int | Number of page in paginated results.
$sort_by = "permission_id"; // string | Field to sort results by.
$order_by = "asc"; // string | Direction of sorting results.

try {
    $result = $apiInstance->v1UsersPermissionsGet($user_id, $begins, $ends, $timing_state, $specifier, $street, $postal_code, $city, $granted, $granted_by, $include_created_permissions, $inactive_since, $include_deleted, $page_size, $page_number, $sort_by, $order_by);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->v1UsersPermissionsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **int**| ID of the user, whose permissions should be returned. If omitted, permissions of session user are returned. | [optional]
 **begins** | **\DateTime**| Filter by date time range. Permissions that overlap with the specified timespan (inclusive) will be included in the result (see &#x60;ends&#x60; parameter). Timezone needs to be specified. | [optional]
 **ends** | **\DateTime**| Filter by date time range. Permissions that overlap with the specified timespan (inclusive) will be included in the result (see &#x60;begins&#x60; parameter). Timezone needs to be specified. | [optional]
 **timing_state** | [**string[]**](../Model/string.md)| Filter by timing state of a permission. | [optional]
 **specifier** | **string**| Filter by specifier of a permission&#39;s sensor. | [optional]
 **street** | **string**| Filter by street name of the address of a permission&#39;s sensor. | [optional]
 **postal_code** | [**object**](../Model/.md)| Filter by postal code of the address of a permission&#39;s sensor. | [optional]
 **city** | **string**| Filter by city of the address of a permission&#39;s sensor. | [optional]
 **granted** | [**string[]**](../Model/string.md)| Filter by permission type. | [optional]
 **granted_by** | **string**| Filter by username/email of the user that granted a permission. | [optional]
 **include_created_permissions** | **bool**| Include permissions created by the user. | [optional] [default to false]
 **inactive_since** | **\DateTime**| Include permissions that are inactive since a certain point of time. | [optional]
 **include_deleted** | **bool**| Include deleted permissions. | [optional] [default to false]
 **page_size** | **int**| Maximal number of items per page. | [optional] [default to 20]
 **page_number** | **int**| Number of page in paginated results. | [optional] [default to 1]
 **sort_by** | **string**| Field to sort results by. | [optional] [default to permission_id]
 **order_by** | **string**| Direction of sorting results. | [optional] [default to asc]

### Return type

[**\KiwiKi\Model\UserPermissionsResult**](../Model/UserPermissionsResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1UsersPost**
> \KiwiKi\Model\UserCreatedResult v1UsersPost($user_data)

Create a new user account



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_data = new \KiwiKi\Model\UserData(); // \KiwiKi\Model\UserData | 

try {
    $result = $apiInstance->v1UsersPost($user_data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->v1UsersPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_data** | [**\KiwiKi\Model\UserData**](../Model/UserData.md)|  |

### Return type

[**\KiwiKi\Model\UserCreatedResult**](../Model/UserCreatedResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1UsersUserIdEmailDelete**
> \KiwiKi\Model\EmailRemovedResult v1UsersUserIdEmailDelete($user_id)

Remove a user's email address

You can only remove the email address of offline users managed by the session user's organization.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 56; // int | 

try {
    $result = $apiInstance->v1UsersUserIdEmailDelete($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->v1UsersUserIdEmailDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **int**|  |

### Return type

[**\KiwiKi\Model\EmailRemovedResult**](../Model/EmailRemovedResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1UsersUserIdEmailPut**
> \KiwiKi\Model\EmailChangeResult v1UsersUserIdEmailPut($user_id, $data)

Change a user's email address

You can only change the email address of the session user or offline users managed by the session user's organization.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 56; // int | 
$data = new \KiwiKi\Model\Data(); // \KiwiKi\Model\Data | 

try {
    $result = $apiInstance->v1UsersUserIdEmailPut($user_id, $data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->v1UsersUserIdEmailPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **int**|  |
 **data** | [**\KiwiKi\Model\Data**](../Model/Data.md)|  |

### Return type

[**\KiwiKi\Model\EmailChangeResult**](../Model/EmailChangeResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1UsersUserIdGet**
> \KiwiKi\Model\UserResult v1UsersUserIdGet($user_id)

Get detailed user information



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 56; // int | 

try {
    $result = $apiInstance->v1UsersUserIdGet($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->v1UsersUserIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **int**|  |

### Return type

[**\KiwiKi\Model\UserResult**](../Model/UserResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1UsersUserIdMoveOutPost**
> \KiwiKi\Model\UserMovedOut v1UsersUserIdMoveOutPost($user_id)

Move tenant out of an organization

If tenants are moved out of an apartment, they will lose all permissions granted by the apartment managers. Also, the user will no longer be managed by the organisation.<br/>If the user is an offline user, they will be deleted.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 56; // int | ID of the users that should be moved out.

try {
    $result = $apiInstance->v1UsersUserIdMoveOutPost($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->v1UsersUserIdMoveOutPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **int**| ID of the users that should be moved out. |

### Return type

[**\KiwiKi\Model\UserMovedOut**](../Model/UserMovedOut.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

