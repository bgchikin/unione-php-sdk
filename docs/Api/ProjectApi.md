# UniOne\ProjectApi

All URIs are relative to https://us1.unione.io/en/transactional/api/v1.

Method | HTTP request | Description
------------- | ------------- | -------------
[**projectCreate()**](ProjectApi.md#projectCreate) | **POST** /project/create.json | Creates a new project.
[**projectDelete()**](ProjectApi.md#projectDelete) | **POST** /project/delete.json | Deletes a project.
[**projectList()**](ProjectApi.md#projectList) | **POST** /project/list.json | Lists projects.
[**projectUpdate()**](ProjectApi.md#projectUpdate) | **POST** /project/update.json | Updates a project.


## `projectCreate()`

```php
projectCreate($projectCreateRequest): \UniOne\Model\ProjectCreate200Response
```

Creates a new project.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKeyAuth
$config = UniOne\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UniOne\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new UniOne\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$projectCreateRequest = new \UniOne\Model\ProjectCreateRequest(); // \UniOne\Model\ProjectCreateRequest

try {
    $result = $apiInstance->projectCreate($projectCreateRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->projectCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **projectCreateRequest** | [**\UniOne\Model\ProjectCreateRequest**](../Model/ProjectCreateRequest.md)|  |

### Return type

[**\UniOne\Model\ProjectCreate200Response**](../Model/ProjectCreate200Response.md)

### Authorization

[apiKeyAuth](../../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectDelete()`

```php
projectDelete($projectDeleteRequest): \UniOne\Model\SuccessResponse
```

Deletes a project.

The project will be moved to the \"trash bin\" before being permanently deleted. You can restore the project by contacting support.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKeyAuth
$config = UniOne\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UniOne\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new UniOne\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$projectDeleteRequest = new \UniOne\Model\ProjectDeleteRequest(); // \UniOne\Model\ProjectDeleteRequest

try {
    $result = $apiInstance->projectDelete($projectDeleteRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->projectDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **projectDeleteRequest** | [**\UniOne\Model\ProjectDeleteRequest**](../Model/ProjectDeleteRequest.md)|  |

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

## `projectList()`

```php
projectList($projectListRequest): \UniOne\Model\ProjectList200Response
```

Lists projects.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKeyAuth
$config = UniOne\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UniOne\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new UniOne\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$projectListRequest = new \UniOne\Model\ProjectListRequest(); // \UniOne\Model\ProjectListRequest

try {
    $result = $apiInstance->projectList($projectListRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->projectList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **projectListRequest** | [**\UniOne\Model\ProjectListRequest**](../Model/ProjectListRequest.md)|  |

### Return type

[**\UniOne\Model\ProjectList200Response**](../Model/ProjectList200Response.md)

### Authorization

[apiKeyAuth](../../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectUpdate()`

```php
projectUpdate($projectUpdateRequest): \UniOne\Model\ProjectUpdate200Response
```

Updates a project.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKeyAuth
$config = UniOne\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UniOne\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new UniOne\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$projectUpdateRequest = new \UniOne\Model\ProjectUpdateRequest(); // \UniOne\Model\ProjectUpdateRequest

try {
    $result = $apiInstance->projectUpdate($projectUpdateRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->projectUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **projectUpdateRequest** | [**\UniOne\Model\ProjectUpdateRequest**](../Model/ProjectUpdateRequest.md)|  |

### Return type

[**\UniOne\Model\ProjectUpdate200Response**](../Model/ProjectUpdate200Response.md)

### Authorization

[apiKeyAuth](../../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
