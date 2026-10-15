# \GraphExportsApi

All URIs are relative to *https://api.yggy.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_graph_export**](GraphExportsApi.md#create_graph_export) | **POST** /api/v1/projects/{projectId}/graph-exports | Start a project graph export
[**download_graph_export**](GraphExportsApi.md#download_graph_export) | **GET** /api/v1/projects/{projectId}/graph-exports/{exportId}/download | Download a ready project graph export
[**list_graph_exports**](GraphExportsApi.md#list_graph_exports) | **GET** /api/v1/projects/{projectId}/graph-exports | List project graph exports from the last 7 days



## create_graph_export

> models::ListGraphExports200ResponseExportsInner create_graph_export(project_id, create_graph_export_request)
Start a project graph export

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**project_id** | **String** |  | [required] |
**create_graph_export_request** | [**CreateGraphExportRequest**](CreateGraphExportRequest.md) |  | [required] |

### Return type

[**models::ListGraphExports200ResponseExportsInner**](listGraphExports_200_response_exports_inner.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## download_graph_export

> String download_graph_export(project_id, export_id)
Download a ready project graph export

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**project_id** | **String** |  | [required] |
**export_id** | **String** |  | [required] |

### Return type

**String**

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/zip, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_graph_exports

> models::ListGraphExports200Response list_graph_exports(project_id)
List project graph exports from the last 7 days

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**project_id** | **String** |  | [required] |

### Return type

[**models::ListGraphExports200Response**](listGraphExports_200_response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

