# # MessageObject

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**recipients** | [**\UniOne\Model\MessageObjectRecipientsInner[]**](MessageObjectRecipientsInner.md) | Contains recipient emails, substitutions(merge tags) and metadata. |
**templateId** | **string** | Optional identifier of the template that had been created by [template/set](#template-set) method. If template_id is passed then fields from the template are used instead of missed email/send parameters. E.g. if \&quot;body\&quot; parameter in email/send is omitted, \&quot;body\&quot; from template will be used. If \&quot;subject\&quot; in email/send is omitted, \&quot;subject\&quot; from template will be used. | [optional]
**tags** | **string[]** | An array of strings. The maximum string length is 50 characters. You can include up to 4 strings which must be unique. No more than 10 000 tags are allowed per project; if you try to add more, email/send will return an error. You may use tags to categorize emails by your own criteria, and they will be passed along by event-dump methods. | [optional]
**skipUnsubscribe** | **int** | Whether to skip or not appending default unsubscribe footer. 1&#x3D;skip, 0&#x3D;append, default is 0. You should [ask support](https://cp.unione.io/en/support) to approve usage of skip_unsubscribe&#x3D;1. [Read more](https://docs.unione.io/en/unsubscribe-link). | [optional]
**globalLanguage** | **string** | The language of the unsubscribe footer and unsubscribe page. Languages supported are: \&quot;be\&quot;, \&quot;de\&quot;, \&quot;en\&quot;, \&quot;es\&quot;, \&quot;fr\&quot;, \&quot;it\&quot;, \&quot;pl\&quot;, \&quot;pt\&quot;, \&quot;ru\&quot;, \&quot;ua\&quot;, \&quot;kz\&quot;. | [optional]
**templateEngine** | [**\UniOne\Model\TemplateEngineString**](TemplateEngineString.md) |  | [optional]
**globalSubstitutions** | **array<string,string>** | Object for passing the substitutions(merge tags) common for all recipients - e.g., company name. If the substitution names are duplicated in object \&quot;substitutions\&quot;, the values of the variables will be taken from the object \&quot;substitutions\&quot;. The substitutions can be used in the following parameters: &lt;ul&gt;&lt;li&gt;body.html &lt;li&gt;body.plaintext &lt;li&gt;body.amp &lt;li&gt;subject &lt;li&gt;from_name &lt;li&gt;options.unsubscribe_url&lt;/ul&gt;A substitution name can consist from latin characeters, numbers and \&quot;_\&quot; symbol, and should start with the letter. | [optional]
**globalMetadata** | **array<string,string>** | Object for passing the metadata common for all the recipients, such as \&quot;key\&quot;: \&quot;value\&quot;. Max key quantity: 10. Max key length: 64 symbols. Max value length: 1024 symbols. The metadata is returned by [webhook](#webhook). To group single emails into a campaign, you can use the system key &#39;campaign_id&#39; with a value in the form of a non-negative decimal integer up to 128 bits or a UUID in the format &#39;c7703772-453e-4c77-a9ae-9a1b94051b5a&#39;. Incorrect values will be treated as &#39;0&#39;. | [optional]
**body** | [**\UniOne\Model\BodyObject**](BodyObject.md) |  |
**subject** | **string** | Email subject. |
**fromEmail** | **string** | Sender&#39;s email. Required only if template_id parameter is empty. | [optional]
**fromName** | **string** | Sender&#39;s name. | [optional]
**replyTo** | **string** | Optional Reply-To email (in case it&#39;s different to sender&#39;s email) | [optional]
**replyToName** | **string** | Optional Reply-To name (if reply_to email is specified and you want to display not only this email but also the name) | [optional]
**trackLinks** | [**\UniOne\Model\TrackLinksInteger**](TrackLinksInteger.md) |  | [optional]
**trackRead** | [**\UniOne\Model\TrackReadInteger**](TrackReadInteger.md) |  | [optional]
**bypassGlobal** | [**\UniOne\Model\BypassGlobalInteger**](BypassGlobalInteger.md) |  | [optional]
**bypassUnavailable** | [**\UniOne\Model\BypassUnavailableInteger**](BypassUnavailableInteger.md) |  | [optional]
**bypassUnsubscribed** | [**\UniOne\Model\BypassUnsubscribedInteger**](BypassUnsubscribedInteger.md) |  | [optional]
**bypassComplained** | [**\UniOne\Model\BypassComplainedInteger**](BypassComplainedInteger.md) |  | [optional]
**idempotenceKey** | **string** | A string of up to 64 characters containing a unique message key. This can be used to prevent occasional message duplicates. If you send another API request with the same message key within the next minute, it will be declined. We can generate a message key for each letter automatically; to enable this option, please contact our [tech support](https://cp.unione.io/en/support). | [optional]
**headers** | [**\UniOne\Model\HeadersObject**](HeadersObject.md) |  | [optional]
**attachments** | [**\UniOne\Model\AttachmentsArrayInner[]**](AttachmentsArrayInner.md) | Optional array of attachments | [optional]
**inlineAttachments** | [**\UniOne\Model\InlineAttachmentsArrayInner[]**](InlineAttachmentsArrayInner.md) | Optional array of inline attachments, e.g. for including images in email instead of loading them from external URL. | [optional]
**options** | [**\UniOne\Model\MessageObjectOptions**](MessageObjectOptions.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
