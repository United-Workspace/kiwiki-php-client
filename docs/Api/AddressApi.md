# KiwiKi\AddressApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1AddressesSearchGet**](AddressApi.md#v1AddressesSearchGet) | **GET** /v1/addresses/search/ | Find an address in KIWI database


# **v1AddressesSearchGet**
> \KiwiKi\Model\AddressResult v1AddressesSearchGet($street, $number, $postal_code)

Find an address in KIWI database

An existing address indicates that this building is already KIWI equipped.<br/>If session key provided, the response will include the information regarding the sensor.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: header_token
$config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKey('Session-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KiwiKi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Session-Key', 'Bearer');

$apiInstance = new KiwiKi\Api\AddressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$street = "street_example"; // string | A street name
$number = "number_example"; // string | Building number
$postal_code = 56; // int | Postal code (Postleitzahl)

try {
    $result = $apiInstance->v1AddressesSearchGet($street, $number, $postal_code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressApi->v1AddressesSearchGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **street** | **string**| A street name |
 **number** | **string**| Building number | [optional]
 **postal_code** | **int**| Postal code (Postleitzahl) | [optional]

### Return type

[**\KiwiKi\Model\AddressResult**](../Model/AddressResult.md)

### Authorization

[header_token](../../README.md#header_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

