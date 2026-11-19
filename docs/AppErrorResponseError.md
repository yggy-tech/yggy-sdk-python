# AppErrorResponseError


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | 
**code** | **str** |  | 
**details** | **object** |  | [optional] 

## Example

```python
from yggy.models.app_error_response_error import AppErrorResponseError

# TODO update the JSON string below
json = "{}"
# create an instance of AppErrorResponseError from a JSON string
app_error_response_error_instance = AppErrorResponseError.from_json(json)
# print the JSON string representation of the object
print(AppErrorResponseError.to_json())

# convert the object into a dict
app_error_response_error_dict = app_error_response_error_instance.to_dict()
# create an instance of AppErrorResponseError from a dict
app_error_response_error_from_dict = AppErrorResponseError.from_dict(app_error_response_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


