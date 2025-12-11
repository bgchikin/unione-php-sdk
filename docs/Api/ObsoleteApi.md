# UniOne\ObsoleteApi

All URIs are relative to https://us1.unione.io/en/transactional/api/v1.

Method | HTTP request | Description
------------- | ------------- | -------------
[**unsubscribedCheck()**](ObsoleteApi.md#unsubscribedCheck) | **POST** /unsubscribed/check.json | Checks if an email is unsubscribed.
[**unsubscribedList()**](ObsoleteApi.md#unsubscribedList) | **POST** /unsubscribed/list.json | Returns a list of all unsubscribed emails since provided date.
[**unsubscribedSet()**](ObsoleteApi.md#unsubscribedSet) | **POST** /unsubscribed/set.json | Registers a new unsubscribed email.


## `unsubscribedCheck()`

```php
unsubscribedCheck($unsubscribedCheckRequest): \UniOne\Model\UnsubscribedCheck200Response
```

Checks if an email is unsubscribed.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKeyAuth
$config = UniOne\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UniOne\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new UniOne\Api\ObsoleteApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$unsubscribedCheckRequest = new \UniOne\Model\UnsubscribedCheckRequest(); // \UniOne\Model\UnsubscribedCheckRequest

try {
    $result = $apiInstance->unsubscribedCheck($unsubscribedCheckRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObsoleteApi->unsubscribedCheck: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **unsubscribedCheckRequest** | [**\UniOne\Model\UnsubscribedCheckRequest**](../Model/UnsubscribedCheckRequest.md)|  |

### Return type

[**\UniOne\Model\UnsubscribedCheck200Response**](../Model/UnsubscribedCheck200Response.md)

### Authorization

[apiKeyAuth](../../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `unsubscribedList()`

```php
unsubscribedList($unsubscribedListRequest): \UniOne\Model\UnsubscribedList200Response
```

Returns a list of all unsubscribed emails since provided date.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKeyAuth
$config = UniOne\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UniOne\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new UniOne\Api\ObsoleteApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$unsubscribedListRequest = new \UniOne\Model\UnsubscribedListRequest(); // \UniOne\Model\UnsubscribedListRequest

try {
    $result = $apiInstance->unsubscribedList($unsubscribedListRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObsoleteApi->unsubscribedList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **unsubscribedListRequest** | [**\UniOne\Model\UnsubscribedListRequest**](../Model/UnsubscribedListRequest.md)|  |

### Return type

[**\UniOne\Model\UnsubscribedList200Response**](../Model/UnsubscribedList200Response.md)

### Authorization

[apiKeyAuth](../../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `unsubscribedSet()`

```php
unsubscribedSet($unsubscribedSetRequest): \UniOne\Model\UnsubscribedSet200Response
```

Registers a new unsubscribed email.

After registering an email as unsubscribed all future attempts to send a message to this email will be rejected. Please note that there's no way to remove an email from unsubscribed thru the API. But you can send an email with a link to resubscribe using [email/subscribe](#email-subscribe) method or remove \"unsubscribed\" status manually on [Email Search page](https://cp.unione.io/en/user/email) in control panel (but only a limited number of unsubscribed email per day can be removed).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKeyAuth
$config = UniOne\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UniOne\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new UniOne\Api\ObsoleteApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$unsubscribedSetRequest = new \UniOne\Model\UnsubscribedSetRequest(); // \UniOne\Model\UnsubscribedSetRequest

try {
    $result = $apiInstance->unsubscribedSet($unsubscribedSetRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ObsoleteApi->unsubscribedSet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **unsubscribedSetRequest** | [**\UniOne\Model\UnsubscribedSetRequest**](../Model/UnsubscribedSetRequest.md)|  |

### Return type

[**\UniOne\Model\UnsubscribedSet200Response**](../Model/UnsubscribedSet200Response.md)

### Authorization

[apiKeyAuth](../../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
