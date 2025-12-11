# # SuppressionListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cause** | **string** | Cause of email being suppressed. One of:&lt;ul&gt;&lt;li&gt;__unsubscribed__ - email is unsubscribed;&lt;li&gt;__temporary_unavailable__ - the email address is unavailable. This means that over the next three days sending to this address will return an error. Email may be temporarily unavailable due to several reasons, e.g.:&lt;ol&gt;&lt;li&gt;a previous email has been rejected by the recipient&#39;s server for spam;&lt;li&gt;the recipient&#39;s mailbox is full or is not used;&lt;li&gt;recipient&#39;s domain does not accept mail;&lt;li&gt;sending server was rejected due to blacklisting;&lt;/ol&gt;&lt;li&gt;__permanent_unavailable__ - the email address is permanently unavailable due to multiple hard bounces; &lt;li&gt;__complained__ -  the recipient reported spam in the previous emails;&lt;li&gt;__blocked__ -  sending to the email is prohibited by administration of UniOne.&lt;/ul&gt;We may add some new causes in the future. | [optional]
**source** | **string** | Source of email being suppressed. One of:&lt;ul&gt;&lt;li&gt;__user__ - suppressed by user with    [suppression/set](#suppression-set);&lt;li&gt;__system__ - sending to the email is prohibited by system, for example due to multiple hard bounces;&lt;li&gt;__subscriber__ - the recipient reported spam or unsubscribed in the previous emails.&lt;/ul&gt; | [optional]
**startTime** | **string** | Date in the format YYYY-MM-DD hh:mm:ss to get suppression list from the \&quot;start_time\&quot; to the present day. Ignored if \&quot;cursor\&quot; is not empty. | [optional]
**cursor** | **string** | The parameter indicates from which position the selection is to be started. Must be empty or omitted for the first data chunk. In order to get subsequent chunks, you must set the \&quot;cursor\&quot; parameter in your request, using the value received in response to the previous request. | [optional]
**limit** | **int** | Limits the number of records to be returned at one time, default is 50. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
