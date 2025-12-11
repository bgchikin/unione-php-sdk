# # EmailValidationSingle200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | [**\UniOne\Model\SuccessStatusString**](SuccessStatusString.md) |  |
**email** | **string** | Email address to be checked. |
**result** | **string** | Possible statuses: &lt;ul&gt;&lt;li&gt;\&quot;valid\&quot; - the address is valid, &lt;li&gt;\&quot;invalid\&quot; - the address is invalid, &lt;li&gt;\&quot;suspicious\&quot; - the address looks suspicious, &lt;li&gt;\&quot;unknown\&quot; - could not perform validation, the domain’s mail server has not responded within the time limit.&lt;/ul&gt; |
**cause** | **string** | Possible statuses: &lt;ul&gt;&lt;li&gt;\&quot;no_mx_record\&quot; - no MX record found for the target domain, &lt;li&gt;\&quot;syntax_error\&quot; - the address syntax is invalid, &lt;li&gt;\&quot;possible_typo\&quot; - the address is likely to have a typo, &lt;li&gt;\&quot;mailbox_not_found\&quot; - the address does not exist, &lt;li&gt;\&quot;global_suppression\&quot; - the address has been marked as unreachable due to multiple previous delivery errors, &lt;li&gt;\&quot;disposable\&quot; - this is a disposable one-time email address which is usually valid for a few minutes only, &lt;li&gt;\&quot;role\&quot; - the address is not likely to belong to an actual person, but rather to a certain business staff role, &lt;li&gt;\&quot;abuse\&quot; - the address is known to be a source of a large number of complaints, sometimes issued automatically, &lt;li&gt;\&quot;spamtrap\&quot; - this email is a spam trap, it is published openly but never used for actual emails. Sending messages to such addresses has a huge negative impact on reputation score,  &lt;li&gt;\&quot;smtp_connection_failed\&quot; - the domain’s SMTP server does not respond; the address may contain a typo.&lt;/ul&gt; |
**validity** | **int** | Validity score, from 0 to 100 (0 – invalid, 100 – valid). |
**localPart** | **string** | Local part (everything preceding the @ sign). |
**domain** | **string** | Domain name part. |
**mxFound** | **bool** | True if the address’ domain does have an MX record, false if does not. |
**mxRecord** | **string** | Preferred MX record for the domain. |
**didYouMean** | **string** | For addresses which are likely to have typing errors (cause&#x3D;possible_typo), a suggested variant with a fixed typo. |
**processedAt** | **string** | Email check date and time, YYYY-MM-DD hh:mm:ss UTC. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
