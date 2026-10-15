# \ChatApi

All URIs are relative to *https://api.yggy.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chat**](ChatApi.md#chat) | **POST** /api/v1/projects/{projectId}/chat | Chat with Knowledge Graph



## chat

> models::Chat200Response chat(project_id, chat_request)
Chat with Knowledge Graph

Ask questions about your documents using the knowledge graph.  The AI agent will search the graph, find relevant entities and relationships, and synthesize an answer.  Examples of questions you can ask: - \"Who founded Acme Corp?\" - \"What topics are discussed in my documents?\" - \"How is John Smith related to the AI project?\" - \"What are the main entities mentioned?\"

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**project_id** | **String** |  | [required] |
**chat_request** | Option<[**ChatRequest**](ChatRequest.md)> |  |  |

### Return type

[**models::Chat200Response**](chat_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

