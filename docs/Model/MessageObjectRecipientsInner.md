# # MessageObjectRecipientsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **string** | Recipient email |
**substitutions** | **array<string,string>** | Object to pass the substitutions(merge tags) for the recipient (e.g. recipient name, discount code, password change link, etc. See [Template engines](https://docs.unione.io/en/template-engines)). The substitutions can be used in the following parameters:&lt;ul&gt;&lt;li&gt;body.html &lt;li&gt;body.plaintext &lt;li&gt;body.amp &lt;li&gt;subject &lt;li&gt;from_name &lt;li&gt;headers[\&quot;List-Unsubscribe\&quot;] &lt;li&gt;options.unsubscribe_url &lt;/ul&gt;  A substitution name can consist from latin characters, numbers and \&quot;_\&quot; symbol, and should start with the letter. There&#39;s a special substitution \&quot;to_name\&quot; which is used to put recipent&#39;s name like \&quot;Name Surname\&quot; to include it to SMTP header \&quot;To\&quot; in the form \&quot;Name Surname &amp;lt;email@example.com&amp;gt;\&quot;. The \&quot;to_name\&quot; length is limited to 78 symbols. | [optional]
**metadata** | **array<string,string>** | Object for passing the metadata, such as \&quot;key\&quot;: \&quot;value\&quot;. Max key quantity: 10. Max key length: 64 symbols. Max value length: 1024 symbols. The metadata is returned by [webhook](#webhook) and [event-dump](#event-dump) methods. If you pass strign up to 128 bit with \&quot;campaign_id\&quot; field name (name is configurable thru support), it will be considered as campaign identifier in statistics. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
