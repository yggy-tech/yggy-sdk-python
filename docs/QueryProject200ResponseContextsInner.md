# QueryProject200ResponseContextsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Stable context id: source slug when present, otherwise the document id | 
**document_id** | **str** | Document id | 
**source** | **str** | Caller-supplied source id when the document has one | [optional] 
**title** | **str** | Document title | 
**snippet** | **str** | Short passage used for ranking | 
**score** | **float** | Relative rank from 0 to 1 inside this result set | 

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


