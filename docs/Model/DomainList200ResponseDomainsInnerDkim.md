# # DomainList200ResponseDomainsInnerDkim

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **string** | DKIM signature for the domain. This property contains only the key part, you should prepend it with \&quot;k&#x3D;rsa, p&#x3D;\&quot; part for the record to be valid (see [domain/get-dns-records](#domain-get-dns-records)). | [optional]
**status** | **string** | Only domains with \&quot;active\&quot; DKIM record are allowed as sender domains. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
