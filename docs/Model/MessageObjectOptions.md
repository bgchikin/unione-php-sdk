# # MessageObjectOptions

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sendAt** | **string** | Date and time in \&quot;YYYY-MM-DD hh:mm:ss\&quot; format in the UTC timezone. Allows schedule sending up to 24 hours in advance. | [optional]
**unsubscribeUrl** | **string** | Custom unsubscribe link. Read more [here](https://docs.unione.io/en/unsubscribe-link). | [optional]
**customBackendId** | **int** | Backend-domain identifier to send message with. If custom_backend_id is not set, default one for your account/project will be used. You can pay for one or more dedicated IPs and use this option. | [optional]
**smtpPoolId** | **string** | SMTP pool identifier to send message with. Usually you don&#39;t need to pass this parameter because correct smtp_pool_id is selected automatically based on the default one for your account/project or according to custom_backend_id parameter. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
