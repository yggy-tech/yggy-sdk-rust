# \QueryApi

All URIs are relative to *https://api.yggy.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**query_organization**](QueryApi.md#query_organization) | **POST** /api/v1/query | Find the documents that answer a question across the organization
[**query_project**](QueryApi.md#query_project) | **POST** /api/v1/projects/{projectId}/query | Find the documents that answer a question in a project



## query_organization

> models::QueryProject200Response query_organization(x_yggy_organization_id, query_project_request)
Find the documents that answer a question across the organization

Same as the project query, across every project the caller can access. Results from all those projects are ranked together.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**x_yggy_organization_id** | Option<**String**> |  |  |
**query_project_request** | Option<[**QueryProjectRequest**](QueryProjectRequest.md)> |  |  |

### Return type

[**models::QueryProject200Response**](queryProject_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## query_project

> models::QueryProject200Response query_project(project_id, x_yggy_organization_id, query_project_request)
Find the documents that answer a question in a project

Returns the documents in this project that best answer the question, best first, each with the passage that matches and a relevance score. yggy finds them through the facts it extracted (a fact found by the question leads to the document it came from) and through the document title and text. Add `include` to attach the facts of the returned documents, or the entities they mention. This route retrieves only; for a written answer use chat.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**project_id** | **String** |  | [required] |
**x_yggy_organization_id** | Option<**String**> |  |  |
**query_project_request** | Option<[**QueryProjectRequest**](QueryProjectRequest.md)> |  |  |

### Return type

[**models::QueryProject200Response**](queryProject_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

