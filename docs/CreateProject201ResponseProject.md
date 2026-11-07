# CreateProject201ResponseProject

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**slug** | **String** |  | 
**name** | **String** |  | 
**color** | **String** |  | 
**organization_id** | **String** |  | 
**external_id** | Option<**String**> |  | [optional]
**kind** | Option<**String**> |  | [optional]
**visibility** | **String** | Who in the organization can see that this project exists. `private` (the default): only project members and organization owners and admins. `public`: every organization member sees its name in the project list, but only members can open it. A personal project (My files) is always `private`. | 
**extraction_purpose** | Option<**String**> |  | [optional]
**extraction_include** | Option<**Vec<String>**> |  | [optional]
**extraction_skip** | Option<**Vec<String>**> |  | [optional]
**extraction_guidance_revision** | Option<**i32**> |  | [optional]
**entity_merge_mode** | Option<**String**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


