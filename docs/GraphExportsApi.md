# yggy.GraphExportsApi

All URIs are relative to *https://api.yggy.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_graph_export**](GraphExportsApi.md#create_graph_export) | **POST** /api/v1/projects/{projectId}/graph-exports | Start a project graph export
[**download_graph_export**](GraphExportsApi.md#download_graph_export) | **GET** /api/v1/projects/{projectId}/graph-exports/{exportId}/download | Download a ready project graph export
[**list_graph_exports**](GraphExportsApi.md#list_graph_exports) | **GET** /api/v1/projects/{projectId}/graph-exports | List project graph exports from the last 7 days


# **create_graph_export**
> ListGraphExports200ResponseExportsInner create_graph_export(project_id, create_graph_export_request)

Start a project graph export

### Example

* Api Key Authentication (apiKeyAuth):
* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.models.create_graph_export_request import CreateGraphExportRequest
from yggy.models.list_graph_exports200_response_exports_inner import ListGraphExports200ResponseExportsInner
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
    api_instance = yggy.GraphExportsApi(api_client)
    project_id = 'project_id_example' # str | 
    create_graph_export_request = yggy.CreateGraphExportRequest() # CreateGraphExportRequest | 

    try:
        # Start a project graph export
        api_response = api_instance.create_graph_export(project_id, create_graph_export_request)
        print("The response of GraphExportsApi->create_graph_export:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GraphExportsApi->create_graph_export: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **create_graph_export_request** | [**CreateGraphExportRequest**](CreateGraphExportRequest.md)|  | 

### Return type

[**ListGraphExports200ResponseExportsInner**](ListGraphExports200ResponseExportsInner.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Export queued |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |
**404** | Project not found |  -  |
**409** | An export is already running |  -  |
**429** | Too many exports |  -  |
**503** | Export could not be started |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **download_graph_export**
> str download_graph_export(project_id, export_id)

Download a ready project graph export

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
    api_instance = yggy.GraphExportsApi(api_client)
    project_id = 'project_id_example' # str | 
    export_id = 'export_id_example' # str | 

    try:
        # Download a ready project graph export
        api_response = api_instance.download_graph_export(project_id, export_id)
        print("The response of GraphExportsApi->download_graph_export:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GraphExportsApi->download_graph_export: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **export_id** | **str**|  | 

### Return type

**str**

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/zip, application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Zip archive |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |
**404** | Export not found |  -  |
**409** | Export is not ready |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_graph_exports**
> ListGraphExports200Response list_graph_exports(project_id)

List project graph exports from the last 7 days

### Example

* Api Key Authentication (apiKeyAuth):
* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.models.list_graph_exports200_response import ListGraphExports200Response
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
    api_instance = yggy.GraphExportsApi(api_client)
    project_id = 'project_id_example' # str | 

    try:
        # List project graph exports from the last 7 days
        api_response = api_instance.list_graph_exports(project_id)
        print("The response of GraphExportsApi->list_graph_exports:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GraphExportsApi->list_graph_exports: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

### Return type

[**ListGraphExports200Response**](ListGraphExports200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Exports that have not expired |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |
**404** | Project not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

