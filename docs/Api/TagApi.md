# UniOne\TagApi

All URIs are relative to https://us1.unione.io/en/transactional/api/v1.

Method | HTTP request | Description
------------- | ------------- | -------------
[**tagDelete()**](TagApi.md#tagDelete) | **POST** /tag/delete.json | Removes tag.
[**tagList()**](TagApi.md#tagList) | **POST** /tag/list.json | This method returns the full list of user-defined tags. Does not receive any parameters.


## `tagDelete()`

```php
tagDelete($tagDeleteRequest): \UniOne\Model\SuccessResponse
```

Removes tag.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKeyAuth
$config = UniOne\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UniOne\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new UniOne\Api\TagApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$tagDeleteRequest = new \UniOne\Model\TagDeleteRequest(); // \UniOne\Model\TagDeleteRequest

try {
    $result = $apiInstance->tagDelete($tagDeleteRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TagApi->tagDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tagDeleteRequest** | [**\UniOne\Model\TagDeleteRequest**](../Model/TagDeleteRequest.md)|  |

### Return type

[**\UniOne\Model\SuccessResponse**](../Model/SuccessResponse.md)

### Authorization

[apiKeyAuth](../../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `tagList()`

```php
tagList($body): \UniOne\Model\TagList200Response
```

This method returns the full list of user-defined tags. Does not receive any parameters.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKeyAuth
$config = UniOne\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UniOne\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new UniOne\Api\TagApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$body = array('key' => new \stdClass); // object

try {
    $result = $apiInstance->tagList($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TagApi->tagList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **object**|  | [optional]

### Return type

[**\UniOne\Model\TagList200Response**](../Model/TagList200Response.md)

### Authorization

[apiKeyAuth](../../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
