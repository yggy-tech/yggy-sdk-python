# QueryProject200ResponseContextsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Stable id of the result: the document&#39;s &#x60;source&#x60; when it has one, otherwise its id | 
**document_id** | **str** | yggy document id | 
**source** | **str** | The &#x60;source&#x60; you set on upload, when the document has one | [optional] 
**title** | **str** | Document title | 
**snippet** | **str** | The passage of the document that best matches the question, up to 400 characters. The title when yggy has no text for the document. | 
**score** | **float** | Relevance from 0 to 1, relative to the best document in this response | 
**external_id** | **str** | Your own id for the document, as sent on upload | [optional] 
**origin_system** | **str** | Business system the data originates from | [optional] 
**web_url** | **str** | Link to the document in your system | [optional] 
**metadata** | [**Dict[str, QueryProject200ResponseContextsInnerMetadataValue]**](QueryProject200ResponseContextsInnerMetadataValue.md) | Your own key-value pairs, as sent on upload. Imported documents carry fields of their source here. | [optional] 

## Example

```python
from yggy.models.query_project200_response_contexts_inner import QueryProject200ResponseContextsInner

# TODO update the JSON string below
json = "{}"
# create an instance of QueryProject200ResponseContextsInner from a JSON string
query_project200_response_contexts_inner_instance = QueryProject200ResponseContextsInner.from_json(json)
# print the JSON string representation of the object
print(QueryProject200ResponseContextsInner.to_json())

# convert the object into a dict
query_project200_response_contexts_inner_dict = query_project200_response_contexts_inner_instance.to_dict()
# create an instance of QueryProject200ResponseContextsInner from a dict
query_project200_response_contexts_inner_from_dict = QueryProject200ResponseContextsInner.from_dict(query_project200_response_contexts_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


