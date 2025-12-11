# # EventDumpObject

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**dumpId** | **string** | Dump ID received by the method [event-dump/create](#event-dump-create). |
**dumpStatus** | **string** | Task status, possible values are:&lt;ul&gt;&lt;li&gt;__queued__ - the task is in the queue, processing is not started yet;&lt;li&gt;__in_process__ - the request is being processed;&lt;li&gt;__ready__ - the task is finished, dump file is ready for download;&lt;li&gt;__failed__ -  processing failed due to an internal error.&lt;/ul&gt; |
**files** | [**\UniOne\Model\EventDumpFilesObject[]**](EventDumpFilesObject.md) | An array of objects, each representing a file, ready for download. You may start downloading everything listed in “files” even if \&quot;dump_status\&quot; is still \&quot;in_process\&quot;. If there are no events, according to the specified parameters, an empty array will be returned. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
