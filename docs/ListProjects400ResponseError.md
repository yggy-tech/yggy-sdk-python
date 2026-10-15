# ListProjects400ResponseError


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | 
**code** | **str** |  | 
**details** | **object** |  | [optional] 

## Example

```python
from yggy.models.list_projects400_response_error import ListProjects400ResponseError

# TODO update the JSON string below
json = "{}"
# create an instance of ListProjects400ResponseError from a JSON string
list_projects400_response_error_instance = ListProjects400ResponseError.from_json(json)
# print the JSON string representation of the object
print(ListProjects400ResponseError.to_json())

# convert the object into a dict
list_projects400_response_error_dict = list_projects400_response_error_instance.to_dict()
# create an instance of ListProjects400ResponseError from a dict
list_projects400_response_error_from_dict = ListProjects400ResponseError.from_dict(list_projects400_response_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


