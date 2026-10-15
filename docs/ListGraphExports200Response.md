# ListGraphExports200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**exports** | [**List[ListGraphExports200ResponseExportsInner]**](ListGraphExports200ResponseExportsInner.md) |  | 

## Example

```python
from yggy.models.list_graph_exports200_response import ListGraphExports200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListGraphExports200Response from a JSON string
list_graph_exports200_response_instance = ListGraphExports200Response.from_json(json)
# print the JSON string representation of the object
print(ListGraphExports200Response.to_json())

# convert the object into a dict
list_graph_exports200_response_dict = list_graph_exports200_response_instance.to_dict()
# create an instance of ListGraphExports200Response from a dict
list_graph_exports200_response_from_dict = ListGraphExports200Response.from_dict(list_graph_exports200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


