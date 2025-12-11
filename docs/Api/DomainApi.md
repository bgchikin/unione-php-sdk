# UniOne\DomainApi

All URIs are relative to https://us1.unione.io/en/transactional/api/v1.

Method | HTTP request | Description
------------- | ------------- | -------------
[**domainDelete()**](DomainApi.md#domainDelete) | **POST** /domain/delete.json | Deletes a domain. Attention: you should use project&#39;s API key to delete a project&#39;s domain.
[**domainGetDnsRecords()**](DomainApi.md#domainGetDnsRecords) | **POST** /domain/get-dns-records.json | Returns info on domain DNS setup for using with UniOne.
[**domainList()**](DomainApi.md#domainList) | **POST** /domain/list.json | Returns a list of all registered domains for user or project, together with statuses of last validations.
[**domainValidateDkim()**](DomainApi.md#domainValidateDkim) | **POST** /domain/validate-dkim.json | Validates DKIM record for domain.
[**domainValidateVerificationRecord()**](DomainApi.md#domainValidateVerificationRecord) | **POST** /domain/validate-verification-record.json | Triggers verification record validation for domain.


## `domainDelete()`

```php
domainDelete($domainDeleteRequest): \UniOne\Model\DomainDelete200Response
```

Deletes a domain. Attention: you should use project's API key to delete a project's domain.

Deletes a domain.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKeyAuth
$config = UniOne\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UniOne\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new UniOne\Api\DomainApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$domainDeleteRequest = new \UniOne\Model\DomainDeleteRequest(); // \UniOne\Model\DomainDeleteRequest

try {
    $result = $apiInstance->domainDelete($domainDeleteRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DomainApi->domainDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domainDeleteRequest** | [**\UniOne\Model\DomainDeleteRequest**](../Model/DomainDeleteRequest.md)|  |

### Return type

[**\UniOne\Model\DomainDelete200Response**](../Model/DomainDelete200Response.md)

### Authorization

[apiKeyAuth](../../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `domainGetDnsRecords()`

```php
domainGetDnsRecords($domainGetDnsRecordsRequest): \UniOne\Model\DomainGetDnsRecords200Response
```

Returns info on domain DNS setup for using with UniOne.

In order to send emails you have to confirm that you own the domain that you are going to send emails from and setup DKIM signature for the domain. This method allows you to register your domain in UniOne and generate verification record and DKIM key, or return previously generated ones if domain is already registered. You should add then DNS records like this to all of the domains you want to confirm:  `@             IN TXT \"unione-validate-hash=483bb362ebdbeedd755cfb1d4d661\"`<br> `us._domainkey IN TXT \"k=rsa; p=MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQDo7\"`<br> `@             IN TXT  \"v=spf1 include:spf.unione.io ~all\"`<br>  - First record value should contain \"verification-record\" field returned by get-dns-records method \"as is\". - Second record value should contain \"dkim\" field value after \"p=\". Mind the name of this record! \"us._domainkey.\" prefix is important for DKIM selector of UniOne to work properly. - Third record contains optional, but very recommended SPF entry. Probably you already have one, then just add append include:spf.unione.io right after v=spf1.  Syntax requirements of different DNS providers may differ: - sometimes it's necesarry to put full domain name instead of @ sign. - some providers require add TTL value (like 3600) - some providers don't require quotes for enclosing values Please check requirements of your provider and advice your users to do it.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKeyAuth
$config = UniOne\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UniOne\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new UniOne\Api\DomainApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$domainGetDnsRecordsRequest = new \UniOne\Model\DomainGetDnsRecordsRequest(); // \UniOne\Model\DomainGetDnsRecordsRequest

try {
    $result = $apiInstance->domainGetDnsRecords($domainGetDnsRecordsRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DomainApi->domainGetDnsRecords: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domainGetDnsRecordsRequest** | [**\UniOne\Model\DomainGetDnsRecordsRequest**](../Model/DomainGetDnsRecordsRequest.md)|  |

### Return type

[**\UniOne\Model\DomainGetDnsRecords200Response**](../Model/DomainGetDnsRecords200Response.md)

### Authorization

[apiKeyAuth](../../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `domainList()`

```php
domainList($domainListRequest): \UniOne\Model\DomainList200Response
```

Returns a list of all registered domains for user or project, together with statuses of last validations.

Returns last status of ownership validation and DKIM validation for each domain. Read more [here](#domain).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKeyAuth
$config = UniOne\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UniOne\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new UniOne\Api\DomainApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$domainListRequest = new \UniOne\Model\DomainListRequest(); // \UniOne\Model\DomainListRequest

try {
    $result = $apiInstance->domainList($domainListRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DomainApi->domainList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domainListRequest** | [**\UniOne\Model\DomainListRequest**](../Model/DomainListRequest.md)|  |

### Return type

[**\UniOne\Model\DomainList200Response**](../Model/DomainList200Response.md)

### Authorization

[apiKeyAuth](../../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `domainValidateDkim()`

```php
domainValidateDkim($domainValidateDkimRequest): \UniOne\Model\DomainValidateVerificationRecord200Response
```

Validates DKIM record for domain.

If you get 200 OK then it means the validation process started succesfully, but it doesn't mean the DKIM record is valid. You should check later dkim.status field returned by [domain/list](#domain-list) method to get the result. Please read more [here](#domain).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKeyAuth
$config = UniOne\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UniOne\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new UniOne\Api\DomainApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$domainValidateDkimRequest = new \UniOne\Model\DomainValidateDkimRequest(); // \UniOne\Model\DomainValidateDkimRequest

try {
    $result = $apiInstance->domainValidateDkim($domainValidateDkimRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DomainApi->domainValidateDkim: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domainValidateDkimRequest** | [**\UniOne\Model\DomainValidateDkimRequest**](../Model/DomainValidateDkimRequest.md)|  |

### Return type

[**\UniOne\Model\DomainValidateVerificationRecord200Response**](../Model/DomainValidateVerificationRecord200Response.md)

### Authorization

[apiKeyAuth](../../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `domainValidateVerificationRecord()`

```php
domainValidateVerificationRecord($domainValidateVerificationRecordRequest): \UniOne\Model\DomainValidateVerificationRecord200Response
```

Triggers verification record validation for domain.

If you get 200 OK then it means the validation process started succesfully, but it doesn't mean the verification record is valid. You should check later verification-record.status field returned by [domain/list](#domain-list) method to get the result. Please read more [here](#domain).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKeyAuth
$config = UniOne\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UniOne\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new UniOne\Api\DomainApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$domainValidateVerificationRecordRequest = new \UniOne\Model\DomainValidateVerificationRecordRequest(); // \UniOne\Model\DomainValidateVerificationRecordRequest

try {
    $result = $apiInstance->domainValidateVerificationRecord($domainValidateVerificationRecordRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DomainApi->domainValidateVerificationRecord: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domainValidateVerificationRecordRequest** | [**\UniOne\Model\DomainValidateVerificationRecordRequest**](../Model/DomainValidateVerificationRecordRequest.md)|  |

### Return type

[**\UniOne\Model\DomainValidateVerificationRecord200Response**](../Model/DomainValidateVerificationRecord200Response.md)

### Authorization

[apiKeyAuth](../../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
