# QueryProjectRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**question** | **String** | Natural-language question to retrieve documents for | 
**top_k** | Option<**i32**> | Maximum number of ranked contexts to return | [optional][default to 5]
**mode** | Option<**String**> | hybrid combines document text with graph matches; lexical uses document text only; graph uses graph matches only | [optional][default to Hybrid]
**include** | Option<**Vec<String>**> | Optional graph fields to attach. Omit for the default retrieve body. identity alone returns only entities with an approved identity. | [optional]
**include_archived** | Option<**bool**> | Also search cold triples. Archived hits surface separately and trigger a background promote. Single-project scope only. | [optional][default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


