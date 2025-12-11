# # WebhookObject

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Webhook unique identifier. |
**url** | **string** | Webhook URL. |
**status** | [**\UniOne\Model\WebhookStatusString**](WebhookStatusString.md) |  |
**eventFormat** | [**\UniOne\Model\WebhookEventFormatString**](WebhookEventFormatString.md) |  |
**deliveryInfo** | [**\UniOne\Model\WebhookDeliveryInfoInteger**](WebhookDeliveryInfoInteger.md) |  |
**singleEvent** | [**\UniOne\Model\WebhookSingleEventInteger**](WebhookSingleEventInteger.md) |  |
**maxParallel** | **int** | Maximum quantity of permitted parallel queries to your server. The more your server can handle - the better. | [default to 10]
**updatedAt** | **string** | Webhook properties last update date and time in UTC timezone in \&quot;YYYY-MM-DD hh:mm:ss\&quot; format. | [optional]
**events** | [**\UniOne\Model\WebhookEventsObject**](WebhookEventsObject.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
