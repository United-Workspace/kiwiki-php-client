# KiwiKi\TaskApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1TasksTaskIdGet**](TaskApi.md#v1TasksTaskIdGet) | **GET** /v1/tasks/{task_id}/ | Get information about the status of a task


# **v1TasksTaskIdGet**
> \KiwiKi\Model\Task v1TasksTaskIdGet($task_id)

Get information about the status of a task



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$task_id = new \stdClass; // object | 

try {
    $result = $apiInstance->v1TasksTaskIdGet($task_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->v1TasksTaskIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **task_id** | [**object**](../Model/.md)|  |

### Return type

[**\KiwiKi\Model\Task**](../Model/Task.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

