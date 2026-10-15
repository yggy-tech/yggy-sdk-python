# yggy.GraphApi

All URIs are relative to *https://api.yggy.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_entity_by_identity**](GraphApi.md#get_entity_by_identity) | **GET** /api/v1/projects/{projectId}/graph/entities/by-identity | Read an organization entity and this project&#39;s facts about it


# **get_entity_by_identity**
> EntityRead get_entity_by_identity(project_id, uri)

Read an organization entity and this project's facts about it

### Example

* Api Key Authentication (apiKeyAuth):
* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.models.entity_read import EntityRead
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
    api_instance = yggy.GraphApi(api_client)
    project_id = 'project_id_example' # str | 
    uri = 'uri_example' # str | Stable identity URI of the organization entity

    try:
        # Read an organization entity and this project's facts about it
        api_response = api_instance.get_entity_by_identity(project_id, uri)
        print("The response of GraphApi->get_entity_by_identity:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GraphApi->get_entity_by_identity: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **uri** | **str**| Stable identity URI of the organization entity | 

### Return type

[**EntityRead**](EntityRead.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Entity read |  -  |
**404** | Entity not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

