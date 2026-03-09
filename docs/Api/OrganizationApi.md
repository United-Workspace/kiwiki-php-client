# KiwiKi\OrganizationApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1OrganizationsOrganizationIdCustomAttributesDataSensorSensorIdGet**](OrganizationApi.md#v1OrganizationsOrganizationIdCustomAttributesDataSensorSensorIdGet) | **GET** /v1/organizations/{organization_id}/custom-attributes-data/sensor/{sensor_id}/ | Get an organization sensor&#39;s custom attributes data
[**v1OrganizationsOrganizationIdCustomAttributesDataSensorSensorIdPost**](OrganizationApi.md#v1OrganizationsOrganizationIdCustomAttributesDataSensorSensorIdPost) | **POST** /v1/organizations/{organization_id}/custom-attributes-data/sensor/{sensor_id}/ | Edit an organization sensor&#39;s attribute (one or multiple)
[**v1OrganizationsOrganizationIdCustomAttributesSensorAttribKeyDelete**](OrganizationApi.md#v1OrganizationsOrganizationIdCustomAttributesSensorAttribKeyDelete) | **DELETE** /v1/organizations/{organization_id}/custom-attributes/sensor/{attrib_key}/ | Delete an organization&#39;s custom attribute
[**v1OrganizationsOrganizationIdCustomAttributesSensorAttribKeyPost**](OrganizationApi.md#v1OrganizationsOrganizationIdCustomAttributesSensorAttribKeyPost) | **POST** /v1/organizations/{organization_id}/custom-attributes/sensor/{attrib_key}/ | Edit an organization&#39;s custom attribute label
[**v1OrganizationsOrganizationIdCustomAttributesSensorGet**](OrganizationApi.md#v1OrganizationsOrganizationIdCustomAttributesSensorGet) | **GET** /v1/organizations/{organization_id}/custom-attributes/sensor/ | Get a list of organization&#39;s custom attributes
[**v1OrganizationsOrganizationIdCustomAttributesSensorPost**](OrganizationApi.md#v1OrganizationsOrganizationIdCustomAttributesSensorPost) | **POST** /v1/organizations/{organization_id}/custom-attributes/sensor/ | Create an organization&#39;s custom attribute
[**v1OrganizationsOrganizationIdCustomFieldsFieldIdGet**](OrganizationApi.md#v1OrganizationsOrganizationIdCustomFieldsFieldIdGet) | **GET** /v1/organizations/{organization_id}/custom-fields/{field_id}/ | Get a user&#39;s custom field
[**v1OrganizationsOrganizationIdCustomFieldsFieldIdManageDelete**](OrganizationApi.md#v1OrganizationsOrganizationIdCustomFieldsFieldIdManageDelete) | **DELETE** /v1/organizations/{organization_id}/custom-fields/{field_id}/manage/ | Delete an organization&#39;s custom field
[**v1OrganizationsOrganizationIdCustomFieldsFieldIdManagePost**](OrganizationApi.md#v1OrganizationsOrganizationIdCustomFieldsFieldIdManagePost) | **POST** /v1/organizations/{organization_id}/custom-fields/{field_id}/manage/ | Edit organization&#39;s custom field name
[**v1OrganizationsOrganizationIdCustomFieldsFieldIdPost**](OrganizationApi.md#v1OrganizationsOrganizationIdCustomFieldsFieldIdPost) | **POST** /v1/organizations/{organization_id}/custom-fields/{field_id}/ | Edit user&#39;s custom field value
[**v1OrganizationsOrganizationIdCustomFieldsGet**](OrganizationApi.md#v1OrganizationsOrganizationIdCustomFieldsGet) | **GET** /v1/organizations/{organization_id}/custom-fields/ | Get a list of organization&#39;s custom fields
[**v1OrganizationsOrganizationIdCustomFieldsPost**](OrganizationApi.md#v1OrganizationsOrganizationIdCustomFieldsPost) | **POST** /v1/organizations/{organization_id}/custom-fields/ | Create an organization&#39;s custom field
[**v1OrganizationsOrganizationIdCustomFieldsUserUserIdGet**](OrganizationApi.md#v1OrganizationsOrganizationIdCustomFieldsUserUserIdGet) | **GET** /v1/organizations/{organization_id}/custom-fields/user/{user_id}/ | Get a list of the user&#39;s custom fields


# **v1OrganizationsOrganizationIdCustomAttributesDataSensorSensorIdGet**
> \KiwiKi\Model\OrganizationCustomAttributesDataResult v1OrganizationsOrganizationIdCustomAttributesDataSensorSensorIdGet($organization_id, $sensor_id)

Get an organization sensor's custom attributes data



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\OrganizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization_id = 56; // int | 
$sensor_id = 56; // int | 

try {
    $result = $apiInstance->v1OrganizationsOrganizationIdCustomAttributesDataSensorSensorIdGet($organization_id, $sensor_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationApi->v1OrganizationsOrganizationIdCustomAttributesDataSensorSensorIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization_id** | **int**|  |
 **sensor_id** | **int**|  |

### Return type

[**\KiwiKi\Model\OrganizationCustomAttributesDataResult**](../Model/OrganizationCustomAttributesDataResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1OrganizationsOrganizationIdCustomAttributesDataSensorSensorIdPost**
> \KiwiKi\Model\OrganizationCustomAttributeDataEditedResult v1OrganizationsOrganizationIdCustomAttributesDataSensorSensorIdPost($organization_id, $sensor_id, $body_values)

Edit an organization sensor's attribute (one or multiple)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\OrganizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization_id = 56; // int | 
$sensor_id = 56; // int | 
$body_values = new \KiwiKi\Model\BodyValues(); // \KiwiKi\Model\BodyValues | 

try {
    $result = $apiInstance->v1OrganizationsOrganizationIdCustomAttributesDataSensorSensorIdPost($organization_id, $sensor_id, $body_values);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationApi->v1OrganizationsOrganizationIdCustomAttributesDataSensorSensorIdPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization_id** | **int**|  |
 **sensor_id** | **int**|  |
 **body_values** | [**\KiwiKi\Model\BodyValues**](../Model/BodyValues.md)|  |

### Return type

[**\KiwiKi\Model\OrganizationCustomAttributeDataEditedResult**](../Model/OrganizationCustomAttributeDataEditedResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1OrganizationsOrganizationIdCustomAttributesSensorAttribKeyDelete**
> \KiwiKi\Model\OrganizationCustomAttributeDeletedResult v1OrganizationsOrganizationIdCustomAttributesSensorAttribKeyDelete($organization_id, $attrib_key)

Delete an organization's custom attribute



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\OrganizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization_id = 56; // int | 
$attrib_key = "attrib_key_example"; // string | 

try {
    $result = $apiInstance->v1OrganizationsOrganizationIdCustomAttributesSensorAttribKeyDelete($organization_id, $attrib_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationApi->v1OrganizationsOrganizationIdCustomAttributesSensorAttribKeyDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization_id** | **int**|  |
 **attrib_key** | **string**|  |

### Return type

[**\KiwiKi\Model\OrganizationCustomAttributeDeletedResult**](../Model/OrganizationCustomAttributeDeletedResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1OrganizationsOrganizationIdCustomAttributesSensorAttribKeyPost**
> \KiwiKi\Model\OrganizationCustomAttributeEditedResult v1OrganizationsOrganizationIdCustomAttributesSensorAttribKeyPost($organization_id, $attrib_key, $body_values)

Edit an organization's custom attribute label



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\OrganizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization_id = 56; // int | 
$attrib_key = "attrib_key_example"; // string | 
$body_values = new \KiwiKi\Model\BodyValues2(); // \KiwiKi\Model\BodyValues2 | 

try {
    $result = $apiInstance->v1OrganizationsOrganizationIdCustomAttributesSensorAttribKeyPost($organization_id, $attrib_key, $body_values);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationApi->v1OrganizationsOrganizationIdCustomAttributesSensorAttribKeyPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization_id** | **int**|  |
 **attrib_key** | **string**|  |
 **body_values** | [**\KiwiKi\Model\BodyValues2**](../Model/BodyValues2.md)|  |

### Return type

[**\KiwiKi\Model\OrganizationCustomAttributeEditedResult**](../Model/OrganizationCustomAttributeEditedResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1OrganizationsOrganizationIdCustomAttributesSensorGet**
> \KiwiKi\Model\OrganizationCustomAttributesListResult v1OrganizationsOrganizationIdCustomAttributesSensorGet($organization_id)

Get a list of organization's custom attributes



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\OrganizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization_id = 56; // int | 

try {
    $result = $apiInstance->v1OrganizationsOrganizationIdCustomAttributesSensorGet($organization_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationApi->v1OrganizationsOrganizationIdCustomAttributesSensorGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization_id** | **int**|  |

### Return type

[**\KiwiKi\Model\OrganizationCustomAttributesListResult**](../Model/OrganizationCustomAttributesListResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1OrganizationsOrganizationIdCustomAttributesSensorPost**
> \KiwiKi\Model\OrganizationCustomAttributeCreatedResult v1OrganizationsOrganizationIdCustomAttributesSensorPost($organization_id, $body_values)

Create an organization's custom attribute



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\OrganizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization_id = 56; // int | 
$body_values = new \KiwiKi\Model\BodyValues1(); // \KiwiKi\Model\BodyValues1 | 

try {
    $result = $apiInstance->v1OrganizationsOrganizationIdCustomAttributesSensorPost($organization_id, $body_values);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationApi->v1OrganizationsOrganizationIdCustomAttributesSensorPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization_id** | **int**|  |
 **body_values** | [**\KiwiKi\Model\BodyValues1**](../Model/BodyValues1.md)|  |

### Return type

[**\KiwiKi\Model\OrganizationCustomAttributeCreatedResult**](../Model/OrganizationCustomAttributeCreatedResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1OrganizationsOrganizationIdCustomFieldsFieldIdGet**
> \KiwiKi\Model\OrganizationUserCustomFieldResult v1OrganizationsOrganizationIdCustomFieldsFieldIdGet($organization_id, $field_id, $user_id)

Get a user's custom field



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\OrganizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization_id = 56; // int | 
$field_id = 56; // int | 
$user_id = new \stdClass; // object | 

try {
    $result = $apiInstance->v1OrganizationsOrganizationIdCustomFieldsFieldIdGet($organization_id, $field_id, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationApi->v1OrganizationsOrganizationIdCustomFieldsFieldIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization_id** | **int**|  |
 **field_id** | **int**|  |
 **user_id** | [**object**](../Model/.md)|  |

### Return type

[**\KiwiKi\Model\OrganizationUserCustomFieldResult**](../Model/OrganizationUserCustomFieldResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1OrganizationsOrganizationIdCustomFieldsFieldIdManageDelete**
> \KiwiKi\Model\OrganizationCustomFieldDeletedResult v1OrganizationsOrganizationIdCustomFieldsFieldIdManageDelete($organization_id, $field_id)

Delete an organization's custom field



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\OrganizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization_id = 56; // int | 
$field_id = 56; // int | 

try {
    $result = $apiInstance->v1OrganizationsOrganizationIdCustomFieldsFieldIdManageDelete($organization_id, $field_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationApi->v1OrganizationsOrganizationIdCustomFieldsFieldIdManageDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization_id** | **int**|  |
 **field_id** | **int**|  |

### Return type

[**\KiwiKi\Model\OrganizationCustomFieldDeletedResult**](../Model/OrganizationCustomFieldDeletedResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1OrganizationsOrganizationIdCustomFieldsFieldIdManagePost**
> \KiwiKi\Model\OrganizationCustomFieldEditedResult v1OrganizationsOrganizationIdCustomFieldsFieldIdManagePost($organization_id, $field_id, $body_values)

Edit organization's custom field name



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\OrganizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization_id = 56; // int | 
$field_id = 56; // int | 
$body_values = new \KiwiKi\Model\BodyValues5(); // \KiwiKi\Model\BodyValues5 | 

try {
    $result = $apiInstance->v1OrganizationsOrganizationIdCustomFieldsFieldIdManagePost($organization_id, $field_id, $body_values);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationApi->v1OrganizationsOrganizationIdCustomFieldsFieldIdManagePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization_id** | **int**|  |
 **field_id** | **int**|  |
 **body_values** | [**\KiwiKi\Model\BodyValues5**](../Model/BodyValues5.md)|  |

### Return type

[**\KiwiKi\Model\OrganizationCustomFieldEditedResult**](../Model/OrganizationCustomFieldEditedResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1OrganizationsOrganizationIdCustomFieldsFieldIdPost**
> \KiwiKi\Model\UserCustomFieldValueEditedResult v1OrganizationsOrganizationIdCustomFieldsFieldIdPost($organization_id, $field_id, $body_values)

Edit user's custom field value



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\OrganizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization_id = 56; // int | 
$field_id = 56; // int | 
$body_values = new \KiwiKi\Model\BodyValues4(); // \KiwiKi\Model\BodyValues4 | 

try {
    $result = $apiInstance->v1OrganizationsOrganizationIdCustomFieldsFieldIdPost($organization_id, $field_id, $body_values);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationApi->v1OrganizationsOrganizationIdCustomFieldsFieldIdPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization_id** | **int**|  |
 **field_id** | **int**|  |
 **body_values** | [**\KiwiKi\Model\BodyValues4**](../Model/BodyValues4.md)|  |

### Return type

[**\KiwiKi\Model\UserCustomFieldValueEditedResult**](../Model/UserCustomFieldValueEditedResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1OrganizationsOrganizationIdCustomFieldsGet**
> \KiwiKi\Model\OrganizationCustomFieldsListResult v1OrganizationsOrganizationIdCustomFieldsGet($organization_id)

Get a list of organization's custom fields



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\OrganizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization_id = 56; // int | 

try {
    $result = $apiInstance->v1OrganizationsOrganizationIdCustomFieldsGet($organization_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationApi->v1OrganizationsOrganizationIdCustomFieldsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization_id** | **int**|  |

### Return type

[**\KiwiKi\Model\OrganizationCustomFieldsListResult**](../Model/OrganizationCustomFieldsListResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1OrganizationsOrganizationIdCustomFieldsPost**
> \KiwiKi\Model\OrganizationCustomFieldCreatedResult v1OrganizationsOrganizationIdCustomFieldsPost($organization_id, $body_values)

Create an organization's custom field



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\OrganizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization_id = 56; // int | 
$body_values = new \KiwiKi\Model\BodyValues3(); // \KiwiKi\Model\BodyValues3 | 

try {
    $result = $apiInstance->v1OrganizationsOrganizationIdCustomFieldsPost($organization_id, $body_values);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationApi->v1OrganizationsOrganizationIdCustomFieldsPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization_id** | **int**|  |
 **body_values** | [**\KiwiKi\Model\BodyValues3**](../Model/BodyValues3.md)|  |

### Return type

[**\KiwiKi\Model\OrganizationCustomFieldCreatedResult**](../Model/OrganizationCustomFieldCreatedResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1OrganizationsOrganizationIdCustomFieldsUserUserIdGet**
> \KiwiKi\Model\OrganizationUserCustomFieldsListResult v1OrganizationsOrganizationIdCustomFieldsUserUserIdGet($organization_id, $user_id)

Get a list of the user's custom fields



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\OrganizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization_id = 56; // int | 
$user_id = 56; // int | 

try {
    $result = $apiInstance->v1OrganizationsOrganizationIdCustomFieldsUserUserIdGet($organization_id, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationApi->v1OrganizationsOrganizationIdCustomFieldsUserUserIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization_id** | **int**|  |
 **user_id** | **int**|  |

### Return type

[**\KiwiKi\Model\OrganizationUserCustomFieldsListResult**](../Model/OrganizationUserCustomFieldsListResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

