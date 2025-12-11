# # WebhookSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **string** | URL that will receive the notification when an event occurs. The URL should be unique for a user or a project. Only ASCII characters are supported for now in URL, please convert to [Punycode](https://en.wikipedia.org/wiki/Punycode) if you need to use non-ASCII characters. |
**status** | [**\UniOne\Model\WebhookStatusString**](WebhookStatusString.md) |  | [optional]
**eventFormat** | [**\UniOne\Model\WebhookEventFormatString**](WebhookEventFormatString.md) |  | [optional]
**deliveryInfo** | [**\UniOne\Model\WebhookDeliveryInfoInteger**](WebhookDeliveryInfoInteger.md) |  | [optional]
**singleEvent** | [**\UniOne\Model\WebhookSingleEventInteger**](WebhookSingleEventInteger.md) |  | [optional]
**maxParallel** | **int** | Maximum quantity of permitted parallel queries to your server. The more your server can handle - the better. | [optional] [default to 10]
**events** | [**\UniOne\Model\WebhookEventsObject**](WebhookEventsObject.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
