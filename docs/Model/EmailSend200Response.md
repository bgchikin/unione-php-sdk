# # EmailSend200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | [**\UniOne\Model\SuccessStatusString**](SuccessStatusString.md) |  |
**jobId** | **string** | Job identifier, might be useful for investigating errors. |
**emails** | **string[]** | Array of recipients emails successfully accepted for sending. | [optional]
**failedEmails** | **array<string,string>[]** | Object with emails rejected for sending as property names and their statuses as property values, e.g.: {\&quot;email1@gmail.com\&quot;: \&quot;temporary_unavailable\&quot;}. Possible statuses:&lt;ul&gt;&lt;li&gt;__unsubscribed__ - specified email is unsubscribed;&lt;li&gt;__invalid__ - the email does not exist or has been entered incorrectly;&lt;li&gt;__duplicate__ - the email already exists in the request, email duplicating is prevented;&lt;li&gt;__temporary_unavailable__ - the email address is unavailable. This means that over the next three days sending to this address will return an error. Email may be temporarily unavailable due to several reasons, e.g.: &lt;ol&gt;&lt;li&gt;a previous email has been rejected by the recipient&#39;s server for spam;&lt;li&gt;the recipient&#39;s mailbox is full or is not used;&lt;li&gt;recipient&#39;s domain does not accept mail;&lt;li&gt;sending server was rejected due to blacklisting;&lt;/ol&gt;&lt;li&gt;__permanent_unavailable__ - the email address is permanently unavailable or unsubscribed globally.&lt;li&gt;__complained__ -  the recipient reported spam in the previous emails;&lt;li&gt;__blocked__ -  sending to the email is prohibited by administration of UniOne.&lt;/ul&gt;We may added new statuses in the future. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
