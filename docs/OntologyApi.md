# \OntologyApi

All URIs are relative to *https://api.yggy.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_ontology_overview**](OntologyApi.md#get_ontology_overview) | **GET** /api/v1/projects/{projectId}/ontology/overview | Project ontology summary



## get_ontology_overview

> models::GetOntologyOverview200Response get_ontology_overview(project_id)
Project ontology summary

Returns ontology versions and totals for one project. List endpoints page the vocabulary.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**project_id** | **String** |  | [required] |

### Return type

[**models::GetOntologyOverview200Response**](getOntologyOverview_200_response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

