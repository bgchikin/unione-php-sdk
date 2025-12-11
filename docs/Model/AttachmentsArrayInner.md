# # AttachmentsArrayInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | Attachment type, see [MIME](https://en.wikipedia.org/wiki/MIME). If unsure, use \&quot;application/octet-stream\&quot;. |
**name** | **string** | Attachment name in the format: \&quot;name.extension\&quot;. When multiple attachments are passed, their names must be unique. The symbol ‘/’ is not allowed in attachment names. |
**content** | **string** | File contents in [base64](https://en.wikipedia.org/wiki/Base64). Maximum file size 7MB (9786710 bytes in base64). |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
