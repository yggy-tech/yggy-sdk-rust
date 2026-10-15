# GetDocumentStatus200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**document_id** | **String** |  | 
**step** | Option<**String**> |  | [optional]
**progress** | **f64** |  | 
**message** | Option<**String**> |  | [optional]
**paused** | Option<**bool**> |  | [optional]
**completed** | **bool** |  | 
**failed** | **bool** |  | 
**stored** | Option<**bool**> |  | [optional]
**awaiting_ontology_review** | Option<**bool**> |  | [optional]
**ontology_review_id** | Option<**String**> |  | [optional]
**ontology_proposal_count** | Option<**f64**> |  | [optional]
**error** | Option<**String**> |  | [optional]
**code** | Option<**String**> |  | [optional]
**failure_message** | Option<**String**> |  | [optional]
**status** | Option<**String**> |  | [optional]
**workflow_error** | Option<**String**> |  | [optional]
**retryable** | Option<**bool**> |  | [optional]
**triples_extracted** | Option<**f64**> |  | [optional]
**input_tokens** | Option<**f64**> |  | [optional]
**output_tokens** | Option<**f64**> |  | [optional]
**extraction_tier** | Option<**String**> |  | [optional]
**extraction_mode** | Option<**String**> |  | [optional]
**estimated_remaining_ms** | Option<**f64**> |  | [optional]
**steps** | Option<[**Vec<models::GetDocumentStatus200ResponseStepsInner>**](getDocumentStatus_200_response_steps_inner.md)> |  | [optional]
**stages** | Option<[**Vec<models::GetDocumentStatus200ResponseStepsInner>**](getDocumentStatus_200_response_steps_inner.md)> |  | [optional]
**invocation_id** | Option<**String**> |  | [optional]
**updated_at** | **f64** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


