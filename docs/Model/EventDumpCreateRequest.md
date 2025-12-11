# # EventDumpCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**startTime** | **string** | Date and time in YYYY-MM-DD hh:mm:ss format, specifying period start time. Data is stored for up to 32 days, depending on your tariff. |
**endTime** | **string** | Date and time in YYYY-MM-DD hh:mm:ss format, specifying period end time (non-inclusive). | [optional]
**limit** | **int** | Maximum number of events returned (default is 50). If this value is over 100 000, several files will be created, each having 100 000 events maximum. | [optional]
**allProjects** | **bool** | For accounts with projects enabled, the value all_projects&#x3D;true allows to fetch data for all existing projects. | [optional] [default to false]
**filter** | [**\UniOne\Model\FilterObject**](FilterObject.md) |  | [optional]
**dumpFields** | **string[]** | An array of strings containing the names of columns you need in your report, in your preferred order. If the &#39;dump_fields&#39; array is missing or empty, a default field list and order will be applied. Allowed values, in their default order, are - &#39;project_id&#39;, &#39;event_time&#39;, &#39;job_id&#39;, &#39;from_email&#39;, &#39;email&#39;, &#39;status&#39;, &#39;delivery_status&#39;, &#39;metadata&#39;, &#39;destination_response&#39;, &#39;user_agent&#39;, &#39;url&#39;, &#39;ip&#39;, &#39;tags&#39;. For maximum security, the &#39;subject&#39; field is not included by default, but you can add it by explicitly including in the &#39;dump_fields&#39; array. | [optional]
**aggregate** | **string** | Allows you to obtain aggregated statistics for a given time period. The two allowed values are:&lt;ul&gt;&lt;li&gt;__day_status__ - fetch aggregated statistics (the filter value must be missing or empty, as filters are not allowed with this option); &lt;li&gt;__an empty string__ - used by default, event_dump/create works as if the aggregate parameter is omitted. | [optional]
**delimiter** | **string** | Field delimiter, can be set to either  &#39;,&#39; or &#39;;&#39;, defaults to  &#39;,&#39;. | [optional]
**format** | **string** | File format, either “csv” (default) or “csv_gzip”. | [optional] [default to 'csv']

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
