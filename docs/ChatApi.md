# yggy.ChatApi

All URIs are relative to *https://api.yggy.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chat**](ChatApi.md#chat) | **POST** /api/v1/projects/{projectId}/chat | Chat with Knowledge Graph


# **chat**
> Chat200Response chat(project_id, chat_request=chat_request)

Chat with Knowledge Graph

Ask questions about your documents using the knowledge graph.

The AI agent will search the graph, find relevant entities and relationships, and synthesize an answer.

Examples of questions you can ask:
- "Who founded Acme Corp?"
- "What topics are discussed in my documents?"
- "How is John Smith related to the AI project?"
- "What are the main entities mentioned?"

### Example

* Bearer Authentication (bearerAuth):

```python
import yggy
from yggy.models.chat200_response import Chat200Response
from yggy.models.chat_request import ChatRequest
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
    api_instance = yggy.ChatApi(api_client)
    project_id = 'project_id_example' # str | 
    chat_request = yggy.ChatRequest() # ChatRequest |  (optional)

    try:
        # Chat with Knowledge Graph
        api_response = api_instance.chat(project_id, chat_request=chat_request)
        print("The response of ChatApi->chat:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ChatApi->chat: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **chat_request** | [**ChatRequest**](ChatRequest.md)|  | [optional] 

### Return type

[**Chat200Response**](Chat200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Chat response |  -  |
**401** | Unauthorized |  -  |
**403** | Project access denied |  -  |
**500** | Internal server error |  -  |
**504** | The answer took longer than the chat budget; try again |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

