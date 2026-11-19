# QueryProject200ResponseContextsInnerPathInner

One relation on the way from what the question found to this document

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subject** | **str** | What the relation starts from | 
**predicate** | **str** | The relation, for example &#x60;blocked_by&#x60; | 
**object** | **str** | What the relation points to | 

## Example

```python
from yggy.models.query_project200_response_contexts_inner_path_inner import QueryProject200ResponseContextsInnerPathInner

# TODO update the JSON string below
json = "{}"
# create an instance of QueryProject200ResponseContextsInnerPathInner from a JSON string
query_project200_response_contexts_inner_path_inner_instance = QueryProject200ResponseContextsInnerPathInner.from_json(json)
# print the JSON string representation of the object
print(QueryProject200ResponseContextsInnerPathInner.to_json())

# convert the object into a dict
query_project200_response_contexts_inner_path_inner_dict = query_project200_response_contexts_inner_path_inner_instance.to_dict()
# create an instance of QueryProject200ResponseContextsInnerPathInner from a dict
query_project200_response_contexts_inner_path_inner_from_dict = QueryProject200ResponseContextsInnerPathInner.from_dict(query_project200_response_contexts_inner_path_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


