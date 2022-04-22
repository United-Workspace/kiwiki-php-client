# KiwiKi\SensorApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1FriendlyNamesSensorSensorIdPost**](SensorApi.md#v1FriendlyNamesSensorSensorIdPost) | **POST** /v1/friendly_names/sensor/{sensor_id}/ | Assign a custom name to a sensor (friendly name)
[**v1SensorsGet**](SensorApi.md#v1SensorsGet) | **GET** /v1/sensors/ | Get a list of visible sensors
[**v1SensorsSensorIdActActionPost**](SensorApi.md#v1SensorsSensorIdActActionPost) | **POST** /v1/sensors/{sensor_id}/act/{action}/ | Send a command to a sensor
[**v1SensorsSensorIdGet**](SensorApi.md#v1SensorsSensorIdGet) | **GET** /v1/sensors/{sensor_id}/ | Get sensor details
[**v1SensorsSensorIdPermissionsGet**](SensorApi.md#v1SensorsSensorIdPermissionsGet) | **GET** /v1/sensors/{sensor_id}/permissions/ | Get sensor permissions


# **v1FriendlyNamesSensorSensorIdPost**
> \KiwiKi\Model\FnameSet v1FriendlyNamesSensorSensorIdPost($fname_data)

Assign a custom name to a sensor (friendly name)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\SensorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$fname_data = new \KiwiKi\Model\\KiwiKi\Model\FnameData(); // \KiwiKi\Model\FnameData | 

try {
    $result = $apiInstance->v1FriendlyNamesSensorSensorIdPost($fname_data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SensorApi->v1FriendlyNamesSensorSensorIdPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fname_data** | [**\KiwiKi\Model\FnameData**](../Model/.md)|  |

### Return type

[**\KiwiKi\Model\FnameSet**](../Model/FnameSet.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1SensorsGet**
> \KiwiKi\Model\SensorResult v1SensorsGet($lat, $lng, $max_distance, $specifier, $street, $city, $state, $postal_code, $permission, $page_size, $page_number, $sort_by, $order_by, $search)

Get a list of visible sensors

Sensors can be filtered by various criteria.<br/>Only sensors visible assigned permission system are returned.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\SensorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$lat = new \stdClass; // object | Latitude (coordinate) in radians
$lng = new \stdClass; // object | Longitude (coordinate) in radians
$max_distance = new \stdClass; // object | Maximal distance from specified coordinates in kilometers
$specifier = "specifier_example"; // string | Match on `specifier` sensor property
$street = "street_example"; // string | Street name of sensor's address
$city = "city_example"; // string | City where sensor is located
$state = "state_example"; // string | Province (Land) of sensor's address
$postal_code = 56; // int | Postal code (Postleitzahl) of sensor's address
$permission = "permission_example"; // string | Require at least permission level X that user has over a sensor
$page_size = 20; // int | Maximal count of sensor in result list
$page_number = 1; // int | Number of page in paginated results
$sort_by = "sort_by_example"; // string | Field to sort results by
$order_by = "order_by_example"; // string | Direction of sorting results
$search = new \stdClass; // object | Fuzzy case-insensitive search through `specifier`, `street`, `postal_code` and `city` at once.

try {
    $result = $apiInstance->v1SensorsGet($lat, $lng, $max_distance, $specifier, $street, $city, $state, $postal_code, $permission, $page_size, $page_number, $sort_by, $order_by, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SensorApi->v1SensorsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **lat** | [**object**](../Model/.md)| Latitude (coordinate) in radians | [optional]
 **lng** | [**object**](../Model/.md)| Longitude (coordinate) in radians | [optional]
 **max_distance** | [**object**](../Model/.md)| Maximal distance from specified coordinates in kilometers | [optional]
 **specifier** | **string**| Match on &#x60;specifier&#x60; sensor property | [optional]
 **street** | **string**| Street name of sensor&#39;s address | [optional]
 **city** | **string**| City where sensor is located | [optional]
 **state** | **string**| Province (Land) of sensor&#39;s address | [optional]
 **postal_code** | **int**| Postal code (Postleitzahl) of sensor&#39;s address | [optional]
 **permission** | **string**| Require at least permission level X that user has over a sensor | [optional]
 **page_size** | **int**| Maximal count of sensor in result list | [optional] [default to 20]
 **page_number** | **int**| Number of page in paginated results | [optional] [default to 1]
 **sort_by** | **string**| Field to sort results by | [optional]
 **order_by** | **string**| Direction of sorting results | [optional]
 **search** | [**object**](../Model/.md)| Fuzzy case-insensitive search through &#x60;specifier&#x60;, &#x60;street&#x60;, &#x60;postal_code&#x60; and &#x60;city&#x60; at once. | [optional]

### Return type

[**\KiwiKi\Model\SensorResult**](../Model/SensorResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1SensorsSensorIdActActionPost**
> v1SensorsSensorIdActActionPost($sensor_id, $action)

Send a command to a sensor

Allows to run one of predefined actions on a door sensor.<br/>The most useful one is to open a door (``open``).<br/><br/>**Note**: sending a command to a sensor doesn't guarantee it's going to reach the target device (best effort).

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\SensorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sensor_id = 56; // int | 
$action = "action_example"; // string | 

try {
    $apiInstance->v1SensorsSensorIdActActionPost($sensor_id, $action);
} catch (Exception $e) {
    echo 'Exception when calling SensorApi->v1SensorsSensorIdActActionPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sensor_id** | **int**|  |
 **action** | **string**|  |

### Return type

void (empty response body)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1SensorsSensorIdGet**
> \KiwiKi\Model\SensorSingleResult v1SensorsSensorIdGet($sensor_id)

Get sensor details



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\SensorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sensor_id = 56; // int | 

try {
    $result = $apiInstance->v1SensorsSensorIdGet($sensor_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SensorApi->v1SensorsSensorIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sensor_id** | **int**|  |

### Return type

[**\KiwiKi\Model\SensorSingleResult**](../Model/SensorSingleResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1SensorsSensorIdPermissionsGet**
> \KiwiKi\Model\SensorPermissionsResult v1SensorsSensorIdPermissionsGet($sensor_id, $begins, $ends, $timing_state, $granted, $granted_by, $username, $name, $lastname, $segment_id, $page_size, $page_number, $sort_by, $order_by)

Get sensor permissions

Get the list of permissions for a certain sensor.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\SensorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sensor_id = 56; // int | 
$begins = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Filter by date time range. Permissions that overlap with the specified timespan (inclusive) will be included in the result (see `ends` parameter). Timezone needs to be specified.
$ends = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Filter by date time range. Permissions that overlap with the specified timespan (inclusive) will be included in the result (see `begins` parameter). Timezone needs to be specified.
$timing_state = array("timing_state_example"); // string[] | Filter by timing state of a permission.
$granted = array("granted_example"); // string[] | Filter by permission type.
$granted_by = "granted_by_example"; // string | Filter by username/email of the user that granted a permission.
$username = "username_example"; // string | Filter by username/email of the user that a permission has been granted.
$name = "name_example"; // string | Filter by forename of the user that a permission has been granted.
$lastname = "lastname_example"; // string | Filter by last name of the user that a permission has been granted.
$segment_id = array("segment_id_example"); // string[] | Filter by segment of the user that a permission has been granted.   * `00` - KIWI employee   * `05` - KIWI electrician   * `10` - Resident   * `15` - Resident (special)   * `20` - Small business employee   * `25` - Small business employee (special)   * `30` - Employee   * `35` - Employee (special)   * `40` - Service provider   * `45` - Service provider (special)   * `50` - Partner   * `55` - Partner (special)
$page_size = 20; // int | Maximal number of items per page.
$page_number = 1; // int | Number of page in paginated results.
$sort_by = "permission_id"; // string | Field to sort results by.
$order_by = "asc"; // string | Direction of sorting results.

try {
    $result = $apiInstance->v1SensorsSensorIdPermissionsGet($sensor_id, $begins, $ends, $timing_state, $granted, $granted_by, $username, $name, $lastname, $segment_id, $page_size, $page_number, $sort_by, $order_by);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SensorApi->v1SensorsSensorIdPermissionsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sensor_id** | **int**|  |
 **begins** | **\DateTime**| Filter by date time range. Permissions that overlap with the specified timespan (inclusive) will be included in the result (see &#x60;ends&#x60; parameter). Timezone needs to be specified. | [optional]
 **ends** | **\DateTime**| Filter by date time range. Permissions that overlap with the specified timespan (inclusive) will be included in the result (see &#x60;begins&#x60; parameter). Timezone needs to be specified. | [optional]
 **timing_state** | [**string[]**](../Model/string.md)| Filter by timing state of a permission. | [optional]
 **granted** | [**string[]**](../Model/string.md)| Filter by permission type. | [optional]
 **granted_by** | **string**| Filter by username/email of the user that granted a permission. | [optional]
 **username** | **string**| Filter by username/email of the user that a permission has been granted. | [optional]
 **name** | **string**| Filter by forename of the user that a permission has been granted. | [optional]
 **lastname** | **string**| Filter by last name of the user that a permission has been granted. | [optional]
 **segment_id** | [**string[]**](../Model/string.md)| Filter by segment of the user that a permission has been granted.   * &#x60;00&#x60; - KIWI employee   * &#x60;05&#x60; - KIWI electrician   * &#x60;10&#x60; - Resident   * &#x60;15&#x60; - Resident (special)   * &#x60;20&#x60; - Small business employee   * &#x60;25&#x60; - Small business employee (special)   * &#x60;30&#x60; - Employee   * &#x60;35&#x60; - Employee (special)   * &#x60;40&#x60; - Service provider   * &#x60;45&#x60; - Service provider (special)   * &#x60;50&#x60; - Partner   * &#x60;55&#x60; - Partner (special) | [optional]
 **page_size** | **int**| Maximal number of items per page. | [optional] [default to 20]
 **page_number** | **int**| Number of page in paginated results. | [optional] [default to 1]
 **sort_by** | **string**| Field to sort results by. | [optional] [default to permission_id]
 **order_by** | **string**| Direction of sorting results. | [optional] [default to asc]

### Return type

[**\KiwiKi\Model\SensorPermissionsResult**](../Model/SensorPermissionsResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

