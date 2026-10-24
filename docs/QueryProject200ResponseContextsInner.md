# QueryProject200ResponseContextsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable context id: source slug when present, otherwise the document id | 
**document_id** | **String** | Document id | 
**source** | Option<**String**> | Caller-supplied source id when the document has one | [optional]
**title** | **String** | Document title | 
**snippet** | **String** | Short passage used for ranking | 
**score** | **f64** | Relative rank from 0 to 1 inside this result set | 
**external_id** | Option<**String**> | Your own id for the document, as sent on upload | [optional]
**origin_system** | Option<**String**> | Business system the data originates from | [optional]
**web_url** | Option<**String**> | Link to the document in your system | [optional]
**metadata** | Option<[**std::collections::HashMap<String, models::QueryProject200ResponseContextsInnerMetadataValue>**](queryProject_200_response_contexts_inner_metadata_value.md)> | Your own key-value pairs, as sent on upload. Imported documents carry fields of their source here. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


