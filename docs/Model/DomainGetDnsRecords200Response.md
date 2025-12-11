# # DomainGetDnsRecords200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | [**\UniOne\Model\SuccessStatusString**](SuccessStatusString.md) |  |
**domain** | **string** | Domain to get DNS records for. |
**verificationRecord** | **string** | Record to be added \&quot;as is\&quot; to verify ownership of this domain. |
**dkim** | **string** | DKIM signature for the domain. This property contains only the key part, you should prepend it with \&quot;k&#x3D;rsa, p&#x3D;\&quot; part for the record to be valid (see example). |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
