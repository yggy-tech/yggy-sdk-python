# yggy.OntologyApi

All URIs are relative to *https://api.yggy.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_ontology_overview**](OntologyApi.md#get_ontology_overview) | **GET** /api/v1/projects/{projectId}/ontology/overview | Project ontology summary


# **get_ontology_overview**
> GetOntologyOverview200Response get_ontology_overview(project_id)

Project ontology summary

Returns ontology versions and totals for one project. List endpoints page the vocabulary.

### Example

* Api Key Authentication (apiKeyAuth):
* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.models.get_ontology_overview200_response import GetOntologyOverview200Response
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
    api_instance = yggy.OntologyApi(api_client)
    project_id = 'project_id_example' # str | 

    try:
        # Project ontology summary
        api_response = api_instance.get_ontology_overview(project_id)
        print("The response of OntologyApi->get_ontology_overview:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OntologyApi->get_ontology_overview: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

### Return type

[**GetOntologyOverview200Response**](GetOntologyOverview200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Ontology summary |  -  |
**401** | Unauthorized |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

