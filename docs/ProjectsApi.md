# yggy.ProjectsApi

All URIs are relative to *https://api.yggy.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_project**](ProjectsApi.md#create_project) | **POST** /api/v1/projects | Create a new project
[**list_projects**](ProjectsApi.md#list_projects) | **GET** /api/v1/projects | List organization projects


# **create_project**
> CreateProject201Response create_project(create_project_request=create_project_request)

Create a new project

Create a new project within the active organization. Projects organize workloads and isolate tokens and integrations.

### Example

* Api Key Authentication (apiKeyAuth):
* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.models.create_project201_response import CreateProject201Response
from yggy.models.create_project_request import CreateProjectRequest
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
    api_instance = yggy.ProjectsApi(api_client)
    create_project_request = yggy.CreateProjectRequest() # CreateProjectRequest |  (optional)

    try:
        # Create a new project
        api_response = api_instance.create_project(create_project_request=create_project_request)
        print("The response of ProjectsApi->create_project:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectsApi->create_project: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_project_request** | [**CreateProjectRequest**](CreateProjectRequest.md)|  | [optional] 

### Return type

[**CreateProject201Response**](CreateProject201Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Project created successfully |  -  |
**400** | Invalid request body |  -  |
**401** | Unauthorized - no active session |  -  |
**403** | Forbidden - insufficient permissions |  -  |
**409** | Conflict - project slug already exists |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_projects**
> ListProjects200Response list_projects(limit=limit, offset=offset, q=q, sort_by=sort_by, sort_dir=sort_dir)

List organization projects

List projects in the active organization with pagination, search, and sort. Default sort is recentlyViewed (last-viewed desc, falling back to createdAt desc), so a user with no views yet gets creation-time order. name orders by project name. Search is a case-insensitive substring over project name and slug.

### Example

* Api Key Authentication (apiKeyAuth):
* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.models.list_projects200_response import ListProjects200Response
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
    api_instance = yggy.ProjectsApi(api_client)
    limit = 20 # int | Page size, from 1 to 100. (optional) (default to 20)
    offset = 0 # int | Zero-based offset for pagination. (optional) (default to 0)
    q = 'q_example' # str | Case-insensitive substring search over project name and slug. Omit or leave blank to list every project. (optional)
    sort_by = recentlyViewed # str | recentlyViewed orders by the caller's last-viewed timestamp (falls back to createdAt desc when no views exist), createdAt orders by creation time, name orders by project name (case-insensitive). (optional) (default to recentlyViewed)
    sort_dir = desc # str |  (optional) (default to desc)

    try:
        # List organization projects
        api_response = api_instance.list_projects(limit=limit, offset=offset, q=q, sort_by=sort_by, sort_dir=sort_dir)
        print("The response of ProjectsApi->list_projects:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectsApi->list_projects: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Page size, from 1 to 100. | [optional] [default to 20]
 **offset** | **int**| Zero-based offset for pagination. | [optional] [default to 0]
 **q** | **str**| Case-insensitive substring search over project name and slug. Omit or leave blank to list every project. | [optional] 
 **sort_by** | **str**| recentlyViewed orders by the caller&#39;s last-viewed timestamp (falls back to createdAt desc when no views exist), createdAt orders by creation time, name orders by project name (case-insensitive). | [optional] [default to recentlyViewed]
 **sort_dir** | **str**|  | [optional] [default to desc]

### Return type

[**ListProjects200Response**](ListProjects200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Projects retrieved successfully |  -  |
**400** | Bad request - no active organization |  -  |
**401** | Unauthorized - no active session |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

