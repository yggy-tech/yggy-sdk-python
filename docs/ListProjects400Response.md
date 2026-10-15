# ListProjects400Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**error** | [**ListProjects400ResponseError**](ListProjects400ResponseError.md) |  | 

## Example

```python
from yggy.models.list_projects400_response import ListProjects400Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListProjects400Response from a JSON string
list_projects400_response_instance = ListProjects400Response.from_json(json)
# print the JSON string representation of the object
print(ListProjects400Response.to_json())

# convert the object into a dict
list_projects400_response_dict = list_projects400_response_instance.to_dict()
# create an instance of ListProjects400Response from a dict
list_projects400_response_from_dict = ListProjects400Response.from_dict(list_projects400_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


