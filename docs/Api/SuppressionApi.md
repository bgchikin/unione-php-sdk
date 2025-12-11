# UniOne\SuppressionApi

All URIs are relative to https://us1.unione.io/en/transactional/api/v1.

Method | HTTP request | Description
------------- | ------------- | -------------
[**suppressionDelete()**](SuppressionApi.md#suppressionDelete) | **POST** /suppression/delete.json | Deletes an email from suppression list (only records with is_deletable&#x3D;true). If there are no entries of this email in the suppression list, API error 3003 is returned. If such entries exist but no one can be deleted, API error 3004 is returned. If daily limit of deletes exceeded, API error 906 is returned.
[**suppressionGet()**](SuppressionApi.md#suppressionGet) | **POST** /suppression/get.json | Gets a reason and date of email suppression.
[**suppressionList()**](SuppressionApi.md#suppressionList) | **POST** /suppression/list.json | Returns a suppression list since provided date.
[**suppressionSet()**](SuppressionApi.md#suppressionSet) | **POST** /suppression/set.json | Adds an email address to the suppression list. You can always remove this address from the suppression list later using the [suppression/delete](#suppression-delete) method.


## `suppressionDelete()`

```php
suppressionDelete($suppressionDeleteRequest): \UniOne\Model\SuccessResponse
```

Deletes an email from suppression list (only records with is_deletable=true). If there are no entries of this email in the suppression list, API error 3003 is returned. If such entries exist but no one can be deleted, API error 3004 is returned. If daily limit of deletes exceeded, API error 906 is returned.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKeyAuth
$config = UniOne\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UniOne\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new UniOne\Api\SuppressionApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$suppressionDeleteRequest = new \UniOne\Model\SuppressionDeleteRequest(); // \UniOne\Model\SuppressionDeleteRequest

try {
    $result = $apiInstance->suppressionDelete($suppressionDeleteRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SuppressionApi->suppressionDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **suppressionDeleteRequest** | [**\UniOne\Model\SuppressionDeleteRequest**](../Model/SuppressionDeleteRequest.md)|  |

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

## `suppressionGet()`

```php
suppressionGet($suppressionGetRequest): \UniOne\Model\SuppressionGet200Response
```

Gets a reason and date of email suppression.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKeyAuth
$config = UniOne\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UniOne\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new UniOne\Api\SuppressionApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$suppressionGetRequest = new \UniOne\Model\SuppressionGetRequest(); // \UniOne\Model\SuppressionGetRequest

try {
    $result = $apiInstance->suppressionGet($suppressionGetRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SuppressionApi->suppressionGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **suppressionGetRequest** | [**\UniOne\Model\SuppressionGetRequest**](../Model/SuppressionGetRequest.md)|  |

### Return type

[**\UniOne\Model\SuppressionGet200Response**](../Model/SuppressionGet200Response.md)

### Authorization

[apiKeyAuth](../../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `suppressionList()`

```php
suppressionList($suppressionListRequest): \UniOne\Model\SuppressionList200Response
```

Returns a suppression list since provided date.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKeyAuth
$config = UniOne\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UniOne\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new UniOne\Api\SuppressionApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$suppressionListRequest = new \UniOne\Model\SuppressionListRequest(); // \UniOne\Model\SuppressionListRequest

try {
    $result = $apiInstance->suppressionList($suppressionListRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SuppressionApi->suppressionList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **suppressionListRequest** | [**\UniOne\Model\SuppressionListRequest**](../Model/SuppressionListRequest.md)|  |

### Return type

[**\UniOne\Model\SuppressionList200Response**](../Model/SuppressionList200Response.md)

### Authorization

[apiKeyAuth](../../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `suppressionSet()`

```php
suppressionSet($suppressionSetRequest): \UniOne\Model\SuccessResponse
```

Adds an email address to the suppression list. You can always remove this address from the suppression list later using the [suppression/delete](#suppression-delete) method.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKeyAuth
$config = UniOne\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UniOne\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new UniOne\Api\SuppressionApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$suppressionSetRequest = new \UniOne\Model\SuppressionSetRequest(); // \UniOne\Model\SuppressionSetRequest

try {
    $result = $apiInstance->suppressionSet($suppressionSetRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SuppressionApi->suppressionSet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **suppressionSetRequest** | [**\UniOne\Model\SuppressionSetRequest**](../Model/SuppressionSetRequest.md)|  |

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
