# # SuppressionList200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | [**\UniOne\Model\SuccessStatusString**](SuccessStatusString.md) |  |
**suppressions** | [**\UniOne\Model\SuppressionListObject[]**](SuppressionListObject.md) | Array of suppression objects. |
**cursor** | **string** | The parameter indicates from which position the selection is to be started. Must be empty or omitted for the first data chunk. In order to get subsequent chunks, you must set the \&quot;cursor\&quot; parameter in your request, using the value received in response to the previous request. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
