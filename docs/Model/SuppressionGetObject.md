# # SuppressionGetObject

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**projectId** | **string** | Unqiue project identifier, ASCII string up to 36 characters long. | [optional]
**cause** | **string** | Cause of email being suppressed. One of:&lt;ul&gt;&lt;li&gt;__unsubscribed__ - email is unsubscribed;&lt;li&gt;__temporary_unavailable__ - the email address is unavailable. This means that over the next three days sending to this address will return an error. Email may be temporarily unavailable due to several reasons, e.g.:&lt;ol&gt;&lt;li&gt;a previous email has been rejected by the recipient&#39;s server for spam;&lt;li&gt;the recipient&#39;s mailbox is full or is not used;&lt;li&gt;recipient&#39;s domain does not accept mail;&lt;li&gt;sending server was rejected due to blacklisting;&lt;/ol&gt;&lt;li&gt;__permanent_unavailable__ - the email address is permanently unavailable due to multiple hard bounces; &lt;li&gt;__complained__ -  the recipient reported spam in the previous emails;&lt;li&gt;__blocked__ -  sending to the email is prohibited by administration of UniOne.&lt;/ul&gt;We may add some new causes in the future. |
**source** | **string** | Source of email being suppressed. One of:&lt;ul&gt;&lt;li&gt;__user__ - suppressed by user with    [suppression/set](#suppression-set);&lt;li&gt;__system__ - sending to the email is prohibited by system, for example due to multiple hard bounces;&lt;li&gt;__subscriber__ - the recipient reported spam or unsubscribed in the previous emails.&lt;/ul&gt; |
**isDeletable** | **bool** | Is it possible to delete this suppression by calling suppression/delete method. |
**created** | **string** | When suppression was created, in UTC timezone in \&quot;YYYY-MM-DD hh:mm:ss\&quot; format. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
