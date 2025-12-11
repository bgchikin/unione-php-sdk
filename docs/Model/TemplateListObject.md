# # TemplateListObject

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Template unique identifier. |
**name** | **string** | Template name. |
**editorType** | [**\UniOne\Model\EditorTypeString**](EditorTypeString.md) |  | [optional]
**templateEngine** | [**\UniOne\Model\TemplateEngineString**](TemplateEngineString.md) |  | [optional]
**globalSubstitutions** | **array<string,string>** | Object for passing the substitutions(merge tags) common for all recipients - e.g., company name. If the substitution names are duplicated in object \&quot;substitutions\&quot;, the values of the variables will be taken from the object \&quot;substitutions\&quot;. The substitutions can be used in the following parameters: &lt;ul&gt;&lt;li&gt;body.html &lt;li&gt;body.plaintext &lt;li&gt;body.amp &lt;li&gt;subject &lt;li&gt;from_name &lt;li&gt;options.unsubscribe_url&lt;/ul&gt;A substitution name can consist from latin characeters, numbers and \&quot;_\&quot; symbol, and should start with the letter. | [optional]
**globalMetadata** | **array<string,string>** | Object for passing the metadata common for all the recipients, such as \&quot;key\&quot;: \&quot;value\&quot;. Max key quantity: 10. Max key length: 64 symbols. Max value length: 1024 symbols. The metadata is returned by [webhook](#webhook). To group single emails into a campaign, you can use the system key &#39;campaign_id&#39; with a value in the form of a non-negative decimal integer up to 128 bits or a UUID in the format &#39;c7703772-453e-4c77-a9ae-9a1b94051b5a&#39;. Incorrect values will be treated as &#39;0&#39;. | [optional]
**body** | [**\UniOne\Model\BodyObject**](BodyObject.md) |  |
**subject** | **string** | Email subject. | [optional]
**fromEmail** | **string** | Sender&#39;s email. |
**fromName** | **string** | Sender&#39;s name. | [optional]
**replyTo** | **string** | Optional Reply-To email (in case it&#39;s different to sender&#39;s email) | [optional]
**replyToName** | **string** | Optional Reply-To name (if reply_to email is specified and you want to display not only this email but also the name) | [optional]
**trackLinks** | [**\UniOne\Model\TrackLinksInteger**](TrackLinksInteger.md) |  | [optional]
**trackRead** | [**\UniOne\Model\TrackReadInteger**](TrackReadInteger.md) |  | [optional]
**headers** | [**\UniOne\Model\HeadersObject**](HeadersObject.md) |  | [optional]
**attachments** | [**\UniOne\Model\AttachmentsArrayInner[]**](AttachmentsArrayInner.md) | Optional array of attachments | [optional]
**inlineAttachments** | [**\UniOne\Model\InlineAttachmentsArrayInner[]**](InlineAttachmentsArrayInner.md) | Optional array of inline attachments, e.g. for including images in email instead of loading them from external URL. | [optional]
**created** | **string** | Template creation date and time in UTC timezone in format \&quot;YYYY-MM-DD hh:mm:ss\&quot; |
**userId** | **int** | Unique user identifier. |
**projectId** | **string** | Unqiue project identifier, ASCII string up to 36 characters long. | [optional]
**projectName** | **string** | Project name, unique for user account. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
