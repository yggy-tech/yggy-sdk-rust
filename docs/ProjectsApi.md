# \ProjectsApi

All URIs are relative to *https://api.yggy.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_project**](ProjectsApi.md#create_project) | **POST** /api/v1/projects | Create a new project
[**list_projects**](ProjectsApi.md#list_projects) | **GET** /api/v1/projects | List organization projects



## create_project

> models::CreateProject201Response create_project(create_project_request)
Create a new project

Create a new project within the active organization. Projects organize workloads and isolate tokens and integrations.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_project_request** | Option<[**CreateProjectRequest**](CreateProjectRequest.md)> |  |  |

### Return type

[**models::CreateProject201Response**](createProject_201_response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_projects

> models::ListProjects200Response list_projects(limit, offset, q, sort_by, sort_dir)
List organization projects

List projects in the active organization with pagination, search, and sort. Organization owners and admins and organization API keys see every shared project. Other members see the projects they are a member of, plus public projects, which come back with isMember false and no counts. Private projects they are not a member of are not listed and not counted in total. Default sort is recentlyViewed (last-viewed desc, falling back to createdAt desc), so a user with no views yet gets creation-time order. name orders by project name. Search is a case-insensitive substring over project name and slug.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**limit** | Option<**i32**> | Page size, from 1 to 100. |  |[default to 20]
**offset** | Option<**i32**> | Zero-based offset for pagination. |  |[default to 0]
**q** | Option<**String**> | Case-insensitive substring search over project name and slug. Omit or leave blank to list every project. |  |
**sort_by** | Option<**String**> | recentlyViewed orders by the caller's last-viewed timestamp (falls back to createdAt desc when no views exist), createdAt orders by creation time, name orders by project name (case-insensitive). |  |[default to recentlyViewed]
**sort_dir** | Option<**String**> |  |  |[default to desc]

### Return type

[**models::ListProjects200Response**](listProjects_200_response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

