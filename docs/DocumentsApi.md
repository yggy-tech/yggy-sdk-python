# yggy.DocumentsApi

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


# **delete_document**
> DeleteDocument200Response delete_document(project_id, id, x_yggy_organization_id=x_yggy_organization_id)

Delete a document and its extracted triples (project-scoped)

Soft-delete a document by its ID, scoped to the project.

### Example

* Api Key Authentication (apiKeyAuth):
* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.models.delete_document200_response import DeleteDocument200Response
from yggy.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.yggy.tech
# See configuration.py for a list of all supported configuration parameters.
configuration = yggy.Configuration(
    host = "https://api.yggy.tech"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: apiKeyAuth
configuration.api_key['apiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKeyAuth'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = yggy.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with yggy.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = yggy.DocumentsApi(api_client)
    project_id = 'project_id_example' # str | 
    id = 'id_example' # str | 
    x_yggy_organization_id = 'x_yggy_organization_id_example' # str |  (optional)

    try:
        # Delete a document and its extracted triples (project-scoped)
        api_response = api_instance.delete_document(project_id, id, x_yggy_organization_id=x_yggy_organization_id)
        print("The response of DocumentsApi->delete_document:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DocumentsApi->delete_document: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **id** | **str**|  | 
 **x_yggy_organization_id** | **str**|  | [optional] 

### Return type

[**DeleteDocument200Response**](DeleteDocument200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Document deleted |  -  |
**404** | Document not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **download_document**
> str download_document(project_id, id, x_yggy_organization_id=x_yggy_organization_id)

Download original document (project-scoped)

Download the original file that was uploaded, scoped to the project.

### Example

* Api Key Authentication (apiKeyAuth):
* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.yggy.tech
# See configuration.py for a list of all supported configuration parameters.
configuration = yggy.Configuration(
    host = "https://api.yggy.tech"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: apiKeyAuth
configuration.api_key['apiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKeyAuth'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = yggy.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with yggy.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = yggy.DocumentsApi(api_client)
    project_id = 'project_id_example' # str | 
    id = 'id_example' # str | 
    x_yggy_organization_id = 'x_yggy_organization_id_example' # str |  (optional)

    try:
        # Download original document (project-scoped)
        api_response = api_instance.download_document(project_id, id, x_yggy_organization_id=x_yggy_organization_id)
        print("The response of DocumentsApi->download_document:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DocumentsApi->download_document: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **id** | **str**|  | 
 **x_yggy_organization_id** | **str**|  | [optional] 

### Return type

**str**

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream, application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | File content |  -  |
**404** | Document or file not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_document**
> ListDocuments200ResponseDocumentsInner get_document(project_id, id, x_yggy_organization_id=x_yggy_organization_id)

Get a document by ID (project-scoped)

Retrieve the details of a specific document by its ID, scoped to the project.

### Example

* Api Key Authentication (apiKeyAuth):
* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.models.list_documents200_response_documents_inner import ListDocuments200ResponseDocumentsInner
from yggy.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.yggy.tech
# See configuration.py for a list of all supported configuration parameters.
configuration = yggy.Configuration(
    host = "https://api.yggy.tech"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: apiKeyAuth
configuration.api_key['apiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKeyAuth'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = yggy.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with yggy.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = yggy.DocumentsApi(api_client)
    project_id = 'project_id_example' # str | 
    id = 'id_example' # str | 
    x_yggy_organization_id = 'x_yggy_organization_id_example' # str |  (optional)

    try:
        # Get a document by ID (project-scoped)
        api_response = api_instance.get_document(project_id, id, x_yggy_organization_id=x_yggy_organization_id)
        print("The response of DocumentsApi->get_document:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DocumentsApi->get_document: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **id** | **str**|  | 
 **x_yggy_organization_id** | **str**|  | [optional] 

### Return type

[**ListDocuments200ResponseDocumentsInner**](ListDocuments200ResponseDocumentsInner.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Document details |  -  |
**404** | Document not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_document_status**
> GetDocumentStatus200Response get_document_status(project_id, id, x_yggy_organization_id=x_yggy_organization_id)

Get document processing status (project-scoped)

Get the current processing status of a document, including progress and any errors.

### Example

* Api Key Authentication (apiKeyAuth):
* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.models.get_document_status200_response import GetDocumentStatus200Response
from yggy.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.yggy.tech
# See configuration.py for a list of all supported configuration parameters.
configuration = yggy.Configuration(
    host = "https://api.yggy.tech"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: apiKeyAuth
configuration.api_key['apiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKeyAuth'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = yggy.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with yggy.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = yggy.DocumentsApi(api_client)
    project_id = 'project_id_example' # str | 
    id = 'id_example' # str | 
    x_yggy_organization_id = 'x_yggy_organization_id_example' # str |  (optional)

    try:
        # Get document processing status (project-scoped)
        api_response = api_instance.get_document_status(project_id, id, x_yggy_organization_id=x_yggy_organization_id)
        print("The response of DocumentsApi->get_document_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DocumentsApi->get_document_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **id** | **str**|  | 
 **x_yggy_organization_id** | **str**|  | [optional] 

### Return type

[**GetDocumentStatus200Response**](GetDocumentStatus200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Document processing status |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_document_triples**
> ListDocumentTriples200Response list_document_triples(project_id, id, x_yggy_organization_id=x_yggy_organization_id)

Get triples extracted from a document (project-scoped)

Retrieve all triples that have been extracted from the specified document.

### Example

* Api Key Authentication (apiKeyAuth):
* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.models.list_document_triples200_response import ListDocumentTriples200Response
from yggy.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.yggy.tech
# See configuration.py for a list of all supported configuration parameters.
configuration = yggy.Configuration(
    host = "https://api.yggy.tech"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: apiKeyAuth
configuration.api_key['apiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKeyAuth'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = yggy.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with yggy.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = yggy.DocumentsApi(api_client)
    project_id = 'project_id_example' # str | 
    id = 'id_example' # str | 
    x_yggy_organization_id = 'x_yggy_organization_id_example' # str |  (optional)

    try:
        # Get triples extracted from a document (project-scoped)
        api_response = api_instance.list_document_triples(project_id, id, x_yggy_organization_id=x_yggy_organization_id)
        print("The response of DocumentsApi->list_document_triples:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DocumentsApi->list_document_triples: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **id** | **str**|  | 
 **x_yggy_organization_id** | **str**|  | [optional] 

### Return type

[**ListDocumentTriples200Response**](ListDocumentTriples200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Extracted triples |  -  |
**404** | Document not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_documents**
> ListDocuments200Response list_documents(project_id, project_id2=project_id2, status=status, archived=archived, limit=limit, offset=offset, sort_by=sort_by, sort_dir=sort_dir, q=q, folder_id=folder_id, note_kind=note_kind, x_yggy_organization_id=x_yggy_organization_id)

List documents for a project

Retrieve a list of documents scoped to the project, with optional filtering and pagination.

### Example

* Api Key Authentication (apiKeyAuth):
* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.models.list_documents200_response import ListDocuments200Response
from yggy.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.yggy.tech
# See configuration.py for a list of all supported configuration parameters.
configuration = yggy.Configuration(
    host = "https://api.yggy.tech"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: apiKeyAuth
configuration.api_key['apiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKeyAuth'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = yggy.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with yggy.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = yggy.DocumentsApi(api_client)
    project_id = 'project_id_example' # str | 
    project_id2 = 'project_id_example' # str | Filter documents by project ID. When omitted, returns all of the organization's documents. (optional)
    status = 'status_example' # str |  (optional)
    archived = false # str | Filter by archive state: false (default) excludes archived, true includes all, only shows archived only (optional) (default to false)
    limit = 20 # float |  (optional) (default to 20)
    offset = 0 # float |  (optional) (default to 0)
    sort_by = createdAt # str |  (optional) (default to createdAt)
    sort_dir = desc # str |  (optional) (default to desc)
    q = 'q_example' # str | Case-insensitive substring search over title and source filename/path. (optional)
    folder_id = 'folder_id_example' # str | Browse documents in this folder (externalId). Use the literal value `root` for unfiled documents only. Omit to list all documents (legacy). (optional)
    note_kind = 'note_kind_example' # str | When set, only documents of this note kind (capture, daily, or note). (optional)
    x_yggy_organization_id = 'x_yggy_organization_id_example' # str |  (optional)

    try:
        # List documents for a project
        api_response = api_instance.list_documents(project_id, project_id2=project_id2, status=status, archived=archived, limit=limit, offset=offset, sort_by=sort_by, sort_dir=sort_dir, q=q, folder_id=folder_id, note_kind=note_kind, x_yggy_organization_id=x_yggy_organization_id)
        print("The response of DocumentsApi->list_documents:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DocumentsApi->list_documents: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **project_id2** | **str**| Filter documents by project ID. When omitted, returns all of the organization&#39;s documents. | [optional] 
 **status** | **str**|  | [optional] 
 **archived** | **str**| Filter by archive state: false (default) excludes archived, true includes all, only shows archived only | [optional] [default to false]
 **limit** | **float**|  | [optional] [default to 20]
 **offset** | **float**|  | [optional] [default to 0]
 **sort_by** | **str**|  | [optional] [default to createdAt]
 **sort_dir** | **str**|  | [optional] [default to desc]
 **q** | **str**| Case-insensitive substring search over title and source filename/path. | [optional] 
 **folder_id** | **str**| Browse documents in this folder (externalId). Use the literal value &#x60;root&#x60; for unfiled documents only. Omit to list all documents (legacy). | [optional] 
 **note_kind** | **str**| When set, only documents of this note kind (capture, daily, or note). | [optional] 
 **x_yggy_organization_id** | **str**|  | [optional] 

### Return type

[**ListDocuments200Response**](ListDocuments200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of documents |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **re_extract_document**
> RetryDocument202Response re_extract_document(project_id, id, x_yggy_organization_id=x_yggy_organization_id)

Re-extract triples from a document (project-scoped)

Delete existing triples and re-trigger extraction. Structured documents reuse a stored mapping when it still validates against the current ontology and identity contract; otherwise a new mapping is generated. Unstructured documents re-run the full extraction pipeline.

### Example

* Api Key Authentication (apiKeyAuth):
* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.models.retry_document202_response import RetryDocument202Response
from yggy.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.yggy.tech
# See configuration.py for a list of all supported configuration parameters.
configuration = yggy.Configuration(
    host = "https://api.yggy.tech"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: apiKeyAuth
configuration.api_key['apiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKeyAuth'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = yggy.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with yggy.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = yggy.DocumentsApi(api_client)
    project_id = 'project_id_example' # str | 
    id = 'id_example' # str | 
    x_yggy_organization_id = 'x_yggy_organization_id_example' # str |  (optional)

    try:
        # Re-extract triples from a document (project-scoped)
        api_response = api_instance.re_extract_document(project_id, id, x_yggy_organization_id=x_yggy_organization_id)
        print("The response of DocumentsApi->re_extract_document:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DocumentsApi->re_extract_document: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **id** | **str**|  | 
 **x_yggy_organization_id** | **str**|  | [optional] 

### Return type

[**RetryDocument202Response**](RetryDocument202Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Re-extraction started |  -  |
**400** | Document cannot be re-extracted |  -  |
**404** | Document not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retry_document**
> RetryDocument202Response retry_document(project_id, id, x_yggy_organization_id=x_yggy_organization_id)

Retry document processing (project-scoped)

Re-trigger processing for a document. Purges the old invocation, resets the document status to PENDING, and re-triggers the workflow using the already-stored file.

### Example

* Api Key Authentication (apiKeyAuth):
* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.models.retry_document202_response import RetryDocument202Response
from yggy.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.yggy.tech
# See configuration.py for a list of all supported configuration parameters.
configuration = yggy.Configuration(
    host = "https://api.yggy.tech"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: apiKeyAuth
configuration.api_key['apiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKeyAuth'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = yggy.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with yggy.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = yggy.DocumentsApi(api_client)
    project_id = 'project_id_example' # str | 
    id = 'id_example' # str | 
    x_yggy_organization_id = 'x_yggy_organization_id_example' # str |  (optional)

    try:
        # Retry document processing (project-scoped)
        api_response = api_instance.retry_document(project_id, id, x_yggy_organization_id=x_yggy_organization_id)
        print("The response of DocumentsApi->retry_document:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DocumentsApi->retry_document: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **id** | **str**|  | 
 **x_yggy_organization_id** | **str**|  | [optional] 

### Return type

[**RetryDocument202Response**](RetryDocument202Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Document requeued for processing |  -  |
**400** | No stored file available for retry |  -  |
**404** | Document not found |  -  |
**409** | Document is already being processed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stream_document_status**
> str stream_document_status(project_id, id)

Stream document processing status (project-scoped)

Subscribe to real-time document processing status updates via Server-Sent Events (SSE).

### Example

* Api Key Authentication (apiKeyAuth):
* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.yggy.tech
# See configuration.py for a list of all supported configuration parameters.
configuration = yggy.Configuration(
    host = "https://api.yggy.tech"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: apiKeyAuth
configuration.api_key['apiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKeyAuth'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = yggy.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with yggy.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = yggy.DocumentsApi(api_client)
    project_id = 'project_id_example' # str | 
    id = 'id_example' # str | 

    try:
        # Stream document processing status (project-scoped)
        api_response = api_instance.stream_document_status(project_id, id)
        print("The response of DocumentsApi->stream_document_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DocumentsApi->stream_document_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **id** | **str**|  | 

### Return type

**str**

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/event-stream

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | SSE stream of status updates |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_document**
> UploadDocument202Response upload_document(project_id, x_yggy_organization_id=x_yggy_organization_id, file=file, text=text, note_kind=note_kind, parent_note_id=parent_note_id, for_link_id=for_link_id, title=title, source=source, origin_system=origin_system, external_id=external_id, metadata=metadata, project_id2=project_id2, desired_tier=desired_tier, inference_mode=inference_mode)

Upload and queue a document for async processing (project-scoped)

Uploads a document to storage, binds it to the project from the path, and queues it for processing.

### Example

* Api Key Authentication (apiKeyAuth):
* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.models.upload_document202_response import UploadDocument202Response
from yggy.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.yggy.tech
# See configuration.py for a list of all supported configuration parameters.
configuration = yggy.Configuration(
    host = "https://api.yggy.tech"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: apiKeyAuth
configuration.api_key['apiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKeyAuth'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = yggy.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with yggy.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = yggy.DocumentsApi(api_client)
    project_id = 'project_id_example' # str | 
    x_yggy_organization_id = 'x_yggy_organization_id_example' # str |  (optional)
    file = None # bytearray | The document file to upload. Optional when text is set. (optional)
    text = 'text_example' # str | Plain text or markdown body. Used when no file is uploaded. (optional)
    note_kind = 'note_kind_example' # str | Note kind. When set, the upload is stored on the caller's personal organization. (optional)
    parent_note_id = 'parent_note_id_example' # str | yggy notes: attach the file to this note. The file becomes a document of its own that belongs to the note, and needs a file. (optional)
    for_link_id = 'for_link_id_example' # str | yggy Notes: the link attachment of the same note this file was uploaded for (its audio, for a transcript). Needs parentNoteId. (optional)
    title = 'title_example' # str | Document title (optional)
    source = 'source_example' # str | Source identifier (optional)
    origin_system = 'origin_system_example' # str | Business system the data originates from (optional)
    external_id = 'external_id_example' # str | Your own id for the document. Returned as externalId in query results and chat citations. (optional)
    metadata = 'metadata_example' # str | JSON object of your own key-value pairs for the document, for example {\\\"region\\\":\\\"EU\\\",\\\"priority\\\":2}. Values are strings, numbers or booleans; at most 50 keys and 8192 bytes. Returned as metadata in query results and chat citations. (optional)
    project_id2 = 'project_id_example' # str | Project ID to bind the document to at upload time (optional)
    desired_tier = 'desired_tier_example' # str | Model tier for extraction. Defaults to auto. (optional)
    inference_mode = 'inference_mode_example' # str | Inference routing for extraction. Defaults to org settings. (optional)

    try:
        # Upload and queue a document for async processing (project-scoped)
        api_response = api_instance.upload_document(project_id, x_yggy_organization_id=x_yggy_organization_id, file=file, text=text, note_kind=note_kind, parent_note_id=parent_note_id, for_link_id=for_link_id, title=title, source=source, origin_system=origin_system, external_id=external_id, metadata=metadata, project_id2=project_id2, desired_tier=desired_tier, inference_mode=inference_mode)
        print("The response of DocumentsApi->upload_document:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DocumentsApi->upload_document: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **x_yggy_organization_id** | **str**|  | [optional] 
 **file** | **bytearray**| The document file to upload. Optional when text is set. | [optional] 
 **text** | **str**| Plain text or markdown body. Used when no file is uploaded. | [optional] 
 **note_kind** | **str**| Note kind. When set, the upload is stored on the caller&#39;s personal organization. | [optional] 
 **parent_note_id** | **str**| yggy notes: attach the file to this note. The file becomes a document of its own that belongs to the note, and needs a file. | [optional] 
 **for_link_id** | **str**| yggy Notes: the link attachment of the same note this file was uploaded for (its audio, for a transcript). Needs parentNoteId. | [optional] 
 **title** | **str**| Document title | [optional] 
 **source** | **str**| Source identifier | [optional] 
 **origin_system** | **str**| Business system the data originates from | [optional] 
 **external_id** | **str**| Your own id for the document. Returned as externalId in query results and chat citations. | [optional] 
 **metadata** | **str**| JSON object of your own key-value pairs for the document, for example {\\\&quot;region\\\&quot;:\\\&quot;EU\\\&quot;,\\\&quot;priority\\\&quot;:2}. Values are strings, numbers or booleans; at most 50 keys and 8192 bytes. Returned as metadata in query results and chat citations. | [optional] 
 **project_id2** | **str**| Project ID to bind the document to at upload time | [optional] 
 **desired_tier** | **str**| Model tier for extraction. Defaults to auto. | [optional] 
 **inference_mode** | **str**| Inference routing for extraction. Defaults to org settings. | [optional] 

### Return type

[**UploadDocument202Response**](UploadDocument202Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Document queued for processing |  -  |
**400** | Invalid request |  -  |
**500** | Failed to queue document |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

