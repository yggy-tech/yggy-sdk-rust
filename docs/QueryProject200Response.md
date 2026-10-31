# QueryProject200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**answer** | **String** | The sentence from the best document that answers the question. Empty when nothing matched. | 
**contexts** | [**Vec<models::QueryProject200ResponseContextsInner>**](queryProject_200_response_contexts_inner.md) | The documents that answer the question, best first | 
**entities** | Option<[**Vec<models::QueryProject200ResponseEntitiesInner>**](queryProject_200_response_entities_inner.md)> | Present when `include` asks for entities or identity | [optional]
**triples** | Option<[**Vec<models::QueryProject200ResponseTriplesInner>**](queryProject_200_response_triples_inner.md)> | The facts of the returned documents. Present when `include` asks for facts (or triples). | [optional]
**archived_hits** | Option<[**Vec<models::QueryProject200ResponseArchivedHitsInner>**](queryProject_200_response_archivedHits_inner.md)> | Present when includeArchived was requested on a single project | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


