# AppErrorResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**error** | [**AppErrorResponseError**](AppErrorResponseError.md) |  | 

## Example

```python
from yggy.models.app_error_response import AppErrorResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AppErrorResponse from a JSON string
app_error_response_instance = AppErrorResponse.from_json(json)
# print the JSON string representation of the object
print(AppErrorResponse.to_json())

# convert the object into a dict
app_error_response_dict = app_error_response_instance.to_dict()
# create an instance of AppErrorResponse from a dict
app_error_response_from_dict = AppErrorResponse.from_dict(app_error_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


