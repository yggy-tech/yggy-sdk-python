# ListGraphExports200ResponseExportsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**format** | **str** |  | 
**status** | **str** |  | 
**created_at** | **datetime** |  | 
**expires_at** | **datetime** |  | 
**created_by_name** | **str** |  | 
**asserted_count** | **int** |  | 
**history_count** | **int** |  | 
**notes** | **List[str]** |  | 

## Example

```python
from yggy.models.list_graph_exports200_response_exports_inner import ListGraphExports200ResponseExportsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListGraphExports200ResponseExportsInner from a JSON string
list_graph_exports200_response_exports_inner_instance = ListGraphExports200ResponseExportsInner.from_json(json)
# print the JSON string representation of the object
print(ListGraphExports200ResponseExportsInner.to_json())

# convert the object into a dict
list_graph_exports200_response_exports_inner_dict = list_graph_exports200_response_exports_inner_instance.to_dict()
# create an instance of ListGraphExports200ResponseExportsInner from a dict
list_graph_exports200_response_exports_inner_from_dict = ListGraphExports200ResponseExportsInner.from_dict(list_graph_exports200_response_exports_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


