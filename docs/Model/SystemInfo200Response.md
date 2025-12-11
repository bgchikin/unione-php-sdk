# # SystemInfo200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | [**\UniOne\Model\SuccessStatusString**](SuccessStatusString.md) |  |
**userId** | **int** | Unique user identifier. |
**email** | **string** | Email of the user. |
**projectId** | **string** | Unqiue project identifier, ASCII string up to 36 characters long. Present only if the API key used for request is the project API key. | [optional]
**projectName** | **string** | Project name, unique for user account. Present only if the API key used for request is the project API key. | [optional]
**projectAccounting** | [**\UniOne\Model\ProjectAccountingObject**](ProjectAccountingObject.md) |  | [optional]
**accounting** | [**\UniOne\Model\SystemInfo200ResponseAccounting**](SystemInfo200ResponseAccounting.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
