# \QueryApi

All URIs are relative to *https://api.yggy.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**query_organization**](QueryApi.md#query_organization) | **POST** /api/v1/query | Retrieve ranked documents across the organization
[**query_project**](QueryApi.md#query_project) | **POST** /api/v1/projects/{projectId}/query | Retrieve ranked documents for a project



## query_organization

> models::QueryProject200Response query_organization(x_yggy_organization_id, query_project_request)
Retrieve ranked documents across the organization

Return ranked document contexts for a question across every project the caller can access. Same body as the project query, including optional include.

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
Retrieve ranked documents for a project

Return ranked document contexts for a question in one project. Chat remains the conversational surface. This route is retrieve-only. Add include to attach matching entities, triples, or approved identity.

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

