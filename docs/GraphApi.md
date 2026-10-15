# \GraphApi

All URIs are relative to *https://api.yggy.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_entity_by_identity**](GraphApi.md#get_entity_by_identity) | **GET** /api/v1/projects/{projectId}/graph/entities/by-identity | Read an organization entity and this project's facts about it



## get_entity_by_identity

> models::EntityRead get_entity_by_identity(project_id, uri)
Read an organization entity and this project's facts about it

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**project_id** | **String** |  | [required] |
**uri** | **String** | Stable identity URI of the organization entity | [required] |

### Return type

[**models::EntityRead**](EntityRead.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

