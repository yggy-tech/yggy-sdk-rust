# QueryProjectRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**question** | **String** | The question in plain language. yggy finds the documents that answer it. | 
**top_k** | Option<**i32**> | How many documents to return, best first. | [optional][default to 5]
**mode** | Option<**String**> | How documents are found and ranked. `hybrid` (default) uses the facts yggy extracted and the document text; `lexical` uses the document text only; `graph` returns only documents the extracted facts point to. | [optional][default to Hybrid]
**include** | Option<**Vec<String>**> | Extra knowledge to attach to the answer. `facts` (also accepted as `triples`) adds the facts extracted from the returned documents; `entities` adds the people, organizations and things they mention; `identity` adds only entities with an approved identity, such as a register number. | [optional]
**include_archived** | Option<**bool**> | Also search archived facts. They are returned in `archivedHits` and brought back into the live graph in the background. Project queries only. | [optional][default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


