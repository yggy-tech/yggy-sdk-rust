# \DocumentsApi

All URIs are relative to *https://api.yggy.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_document**](DocumentsApi.md#delete_document) | **DELETE** /api/v1/projects/{projectId}/documents/{id} | Delete a document and its extracted triples (project-scoped)
[**download_document**](DocumentsApi.md#download_document) | **GET** /api/v1/projects/{projectId}/documents/{id}/download | Download original document (project-scoped)
[**get_document**](DocumentsApi.md#get_document) | **GET** /api/v1/projects/{projectId}/documents/{id} | Get a document by ID (project-scoped)
[**get_document_status**](DocumentsApi.md#get_document_status) | **GET** /api/v1/projects/{projectId}/documents/{id}/status | Get document processing status (project-scoped)
[**list_document_triples**](DocumentsApi.md#list_document_triples) | **GET** /api/v1/projects/{projectId}/documents/{id}/triples | Get triples extracted from a document (project-scoped)
[**list_documents**](DocumentsApi.md#list_documents) | **GET** /api/v1/projects/{projectId}/documents | List documents for a project
[**re_extract_document**](DocumentsApi.md#re_extract_document) | **POST** /api/v1/projects/{projectId}/documents/{id}/re-extract | Re-extract triples from a document (project-scoped)
[**retry_document**](DocumentsApi.md#retry_document) | **POST** /api/v1/projects/{projectId}/documents/{id}/retry | Retry document processing (project-scoped)
[**stream_document_status**](DocumentsApi.md#stream_document_status) | **GET** /api/v1/projects/{projectId}/documents/{id}/status/stream | Stream document processing status (project-scoped)
[**upload_document**](DocumentsApi.md#upload_document) | **POST** /api/v1/projects/{projectId}/documents/upload | Upload and queue a document for async processing (project-scoped)



## delete_document

> models::DeleteDocument200Response delete_document(project_id, id, x_yggy_organization_id)
Delete a document and its extracted triples (project-scoped)

Soft-delete a document by its ID, scoped to the project.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**project_id** | **String** |  | [required] |
**id** | **String** |  | [required] |
**x_yggy_organization_id** | Option<**String**> |  |  |

### Return type

[**models::DeleteDocument200Response**](deleteDocument_200_response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## download_document

> String download_document(project_id, id, x_yggy_organization_id)
Download original document (project-scoped)

Download the original file that was uploaded, scoped to the project.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**project_id** | **String** |  | [required] |
**id** | **String** |  | [required] |
**x_yggy_organization_id** | Option<**String**> |  |  |

### Return type

**String**

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/octet-stream, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_document

> models::ListDocuments200ResponseDocumentsInner get_document(project_id, id, x_yggy_organization_id)
Get a document by ID (project-scoped)

Retrieve the details of a specific document by its ID, scoped to the project.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**project_id** | **String** |  | [required] |
**id** | **String** |  | [required] |
**x_yggy_organization_id** | Option<**String**> |  |  |

### Return type

[**models::ListDocuments200ResponseDocumentsInner**](listDocuments_200_response_documents_inner.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_document_status

> models::GetDocumentStatus200Response get_document_status(project_id, id, x_yggy_organization_id)
Get document processing status (project-scoped)

Get the current processing status of a document, including progress and any errors.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**project_id** | **String** |  | [required] |
**id** | **String** |  | [required] |
**x_yggy_organization_id** | Option<**String**> |  |  |

### Return type

[**models::GetDocumentStatus200Response**](getDocumentStatus_200_response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_document_triples

> models::ListDocumentTriples200Response list_document_triples(project_id, id, x_yggy_organization_id)
Get triples extracted from a document (project-scoped)

Retrieve all triples that have been extracted from the specified document.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**project_id** | **String** |  | [required] |
**id** | **String** |  | [required] |
**x_yggy_organization_id** | Option<**String**> |  |  |

### Return type

[**models::ListDocumentTriples200Response**](listDocumentTriples_200_response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_documents

> models::ListDocuments200Response list_documents(project_id, project_id2, status, archived, limit, offset, sort_by, sort_dir, q, folder_id, note_kind, x_yggy_organization_id)
List documents for a project

Retrieve a list of documents scoped to the project, with optional filtering and pagination.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**project_id** | **String** |  | [required] |
**project_id2** | Option<**String**> | Filter documents by project ID. When omitted, returns all of the organization's documents. |  |
**status** | Option<**String**> |  |  |
**archived** | Option<**String**> | Filter by archive state: false (default) excludes archived, true includes all, only shows archived only |  |[default to false]
**limit** | Option<**f64**> |  |  |[default to 20]
**offset** | Option<**f64**> |  |  |[default to 0]
**sort_by** | Option<**String**> |  |  |[default to createdAt]
**sort_dir** | Option<**String**> |  |  |[default to desc]
**q** | Option<**String**> | Case-insensitive substring search over title and source filename/path. |  |
**folder_id** | Option<**String**> | Browse documents in this folder (externalId). Use the literal value `root` for unfiled documents only. Omit to list all documents (legacy). |  |
**note_kind** | Option<**String**> | When set, only documents of this note kind (capture, daily, or note). |  |
**x_yggy_organization_id** | Option<**String**> |  |  |

### Return type

[**models::ListDocuments200Response**](listDocuments_200_response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## re_extract_document

> models::RetryDocument202Response re_extract_document(project_id, id, x_yggy_organization_id)
Re-extract triples from a document (project-scoped)

Delete existing triples and re-trigger extraction. Structured documents reuse a stored mapping when it still validates against the current ontology and identity contract; otherwise a new mapping is generated. Unstructured documents re-run the full extraction pipeline.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**project_id** | **String** |  | [required] |
**id** | **String** |  | [required] |
**x_yggy_organization_id** | Option<**String**> |  |  |

### Return type

[**models::RetryDocument202Response**](retryDocument_202_response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## retry_document

> models::RetryDocument202Response retry_document(project_id, id, x_yggy_organization_id)
Retry document processing (project-scoped)

Re-trigger processing for a document. Purges the old invocation, resets the document status to PENDING, and re-triggers the workflow using the already-stored file.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**project_id** | **String** |  | [required] |
**id** | **String** |  | [required] |
**x_yggy_organization_id** | Option<**String**> |  |  |

### Return type

[**models::RetryDocument202Response**](retryDocument_202_response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## stream_document_status

> String stream_document_status(project_id, id)
Stream document processing status (project-scoped)

Subscribe to real-time document processing status updates via Server-Sent Events (SSE).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**project_id** | **String** |  | [required] |
**id** | **String** |  | [required] |

### Return type

**String**

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/event-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upload_document

> models::UploadDocument202Response upload_document(project_id, x_yggy_organization_id, file, text, note_kind, parent_note_id, for_link_id, title, source, origin_system, project_id2, desired_tier, inference_mode)
Upload and queue a document for async processing (project-scoped)

Uploads a document to storage, binds it to the project from the path, and queues it for processing.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**project_id** | **String** |  | [required] |
**x_yggy_organization_id** | Option<**String**> |  |  |
**file** | Option<**std::path::PathBuf**> | The document file to upload. Optional when text is set. |  |
**text** | Option<**String**> | Plain text or markdown body. Used when no file is uploaded. |  |
**note_kind** | Option<**String**> | Note kind. When set, the upload is stored on the caller's personal organization. |  |
**parent_note_id** | Option<**String**> | yggy notes: attach the file to this note. The file becomes a document of its own that belongs to the note, and needs a file. |  |
**for_link_id** | Option<**String**> | yggy Notes: the link attachment of the same note this file was uploaded for (its audio, for a transcript). Needs parentNoteId. |  |
**title** | Option<**String**> | Document title |  |
**source** | Option<**String**> | Source identifier |  |
**origin_system** | Option<**String**> | Business system the data originates from |  |
**project_id2** | Option<**String**> | Project ID to bind the document to at upload time |  |
**desired_tier** | Option<**String**> | Model tier for extraction. Defaults to auto. |  |
**inference_mode** | Option<**String**> | Inference routing for extraction. Defaults to org settings. |  |

### Return type

[**models::UploadDocument202Response**](uploadDocument_202_response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

