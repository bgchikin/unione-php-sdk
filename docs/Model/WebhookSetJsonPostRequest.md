# # WebhookSetJsonPostRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**auth** | **string** | MD5-hash of the message body, in which the value \&quot;auth\&quot; is replaced by api key of the user/project; with this field the recipient of the notification can both authenticate and verify the notification integrity |
**eventsByUser** | [**\UniOne\Model\WebhookSetJsonPostRequestEventsByUserInner[]**](WebhookSetJsonPostRequestEventsByUserInner.md) | Array with only one element, containing events of a user/project. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
