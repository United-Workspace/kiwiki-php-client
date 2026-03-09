# KiwiKi\SessionApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1SessionDelete**](SessionApi.md#v1SessionDelete) | **DELETE** /v1/session/ | Clean up user session
[**v1SessionPost**](SessionApi.md#v1SessionPost) | **POST** /v1/session/ | Create user session


# **v1SessionDelete**
> \KiwiKi\Model\InlineResponse200 v1SessionDelete()

Clean up user session

This effectively logs an user out.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\SessionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->v1SessionDelete();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SessionApi->v1SessionDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\KiwiKi\Model\InlineResponse200**](../Model/InlineResponse200.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1SessionPost**
> \KiwiKi\Model\SessionResult v1SessionPost($credentials)

Create user session

Establish an authenticated user session.<br/>Before most API requests can be made, a login session must be started by providing a valid username and password. A **session key** will then be given back from the API, which can be used for authentication on further API requests.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new KiwiKi\Api\SessionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$credentials = new \KiwiKi\Model\Credentials(); // \KiwiKi\Model\Credentials | 

try {
    $result = $apiInstance->v1SessionPost($credentials);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SessionApi->v1SessionPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **credentials** | [**\KiwiKi\Model\Credentials**](../Model/Credentials.md)|  |

### Return type

[**\KiwiKi\Model\SessionResult**](../Model/SessionResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

