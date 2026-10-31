# yggy.QueryApi

All URIs are relative to *https://api.yggy.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**query_organization**](QueryApi.md#query_organization) | **POST** /api/v1/query | Find the documents that answer a question across the organization
[**query_project**](QueryApi.md#query_project) | **POST** /api/v1/projects/{projectId}/query | Find the documents that answer a question in a project


# **query_organization**
> QueryProject200Response query_organization(x_yggy_organization_id=x_yggy_organization_id, query_project_request=query_project_request)

Find the documents that answer a question across the organization

Same as the project query, across every project the caller can access. Results from all those projects are ranked together.

### Example

* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.models.query_project200_response import QueryProject200Response
from yggy.models.query_project_request import QueryProjectRequest
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

# Configure Bearer authorization: bearerAuth
configuration = yggy.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with yggy.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = yggy.QueryApi(api_client)
    x_yggy_organization_id = 'x_yggy_organization_id_example' # str |  (optional)
    query_project_request = yggy.QueryProjectRequest() # QueryProjectRequest |  (optional)

    try:
        # Find the documents that answer a question across the organization
        api_response = api_instance.query_organization(x_yggy_organization_id=x_yggy_organization_id, query_project_request=query_project_request)
        print("The response of QueryApi->query_organization:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling QueryApi->query_organization: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_yggy_organization_id** | **str**|  | [optional] 
 **query_project_request** | [**QueryProjectRequest**](QueryProjectRequest.md)|  | [optional] 

### Return type

[**QueryProject200Response**](QueryProject200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Ranked contexts and an extractive answer |  -  |
**400** | Invalid request or usage limit exceeded |  -  |
**401** | Authentication required |  -  |
**403** | Project access denied |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **query_project**
> QueryProject200Response query_project(project_id, x_yggy_organization_id=x_yggy_organization_id, query_project_request=query_project_request)

Find the documents that answer a question in a project

Returns the documents in this project that best answer the question, best first, each with the passage that matches and a relevance score. yggy finds them through the facts it extracted (a fact found by the question leads to the document it came from) and through the document title and text. Add `include` to attach the facts of the returned documents, or the entities they mention. This route retrieves only; for a written answer use chat.

### Example

* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.models.query_project200_response import QueryProject200Response
from yggy.models.query_project_request import QueryProjectRequest
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

# Configure Bearer authorization: bearerAuth
configuration = yggy.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with yggy.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = yggy.QueryApi(api_client)
    project_id = 'project_id_example' # str | 
    x_yggy_organization_id = 'x_yggy_organization_id_example' # str |  (optional)
    query_project_request = yggy.QueryProjectRequest() # QueryProjectRequest |  (optional)

    try:
        # Find the documents that answer a question in a project
        api_response = api_instance.query_project(project_id, x_yggy_organization_id=x_yggy_organization_id, query_project_request=query_project_request)
        print("The response of QueryApi->query_project:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling QueryApi->query_project: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **x_yggy_organization_id** | **str**|  | [optional] 
 **query_project_request** | [**QueryProjectRequest**](QueryProjectRequest.md)|  | [optional] 

### Return type

[**QueryProject200Response**](QueryProject200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Ranked contexts and an extractive answer |  -  |
**400** | Invalid request or usage limit exceeded |  -  |
**401** | Authentication required |  -  |
**403** | Project access denied |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

