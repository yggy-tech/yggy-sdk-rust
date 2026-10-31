# QueryProject200ResponseContextsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable id of the result: the document's `source` when it has one, otherwise its id | 
**document_id** | **String** | yggy document id | 
**source** | Option<**String**> | The `source` you set on upload, when the document has one | [optional]
**title** | **String** | Document title | 
**snippet** | **String** | The passage of the document that best matches the question, up to 400 characters. The title when yggy has no text for the document. | 
**score** | **f64** | Relevance from 0 to 1, relative to the best document in this response | 
**external_id** | Option<**String**> | Your own id for the document, as sent on upload | [optional]
**origin_system** | Option<**String**> | Business system the data originates from | [optional]
**web_url** | Option<**String**> | Link to the document in your system | [optional]
**metadata** | Option<[**std::collections::HashMap<String, models::QueryProject200ResponseContextsInnerMetadataValue>**](queryProject_200_response_contexts_inner_metadata_value.md)> | Your own key-value pairs, as sent on upload. Imported documents carry fields of their source here. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


