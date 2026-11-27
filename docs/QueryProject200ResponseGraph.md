# QueryProject200ResponseGraph

How yggy followed relations for this question. Present unless `hops` is 0.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**hops** | **int** | Hops followed. 0 in &#x60;lexical&#x60; mode. | 
**seeds** | **int** | Entities the walk started from | 
**reached** | [**QueryProject200ResponseGraphReached**](QueryProject200ResponseGraphReached.md) |  | 
**truncated** | **bool** | True when a limit or the time budget stopped the walk early. The result is still returned. | 

## Example

```python
from yggy.models.query_project200_response_graph import QueryProject200ResponseGraph

# TODO update the JSON string below
json = "{}"
# create an instance of QueryProject200ResponseGraph from a JSON string
query_project200_response_graph_instance = QueryProject200ResponseGraph.from_json(json)
# print the JSON string representation of the object
print(QueryProject200ResponseGraph.to_json())

# convert the object into a dict
query_project200_response_graph_dict = query_project200_response_graph_instance.to_dict()
# create an instance of QueryProject200ResponseGraph from a dict
query_project200_response_graph_from_dict = QueryProject200ResponseGraph.from_dict(query_project200_response_graph_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


