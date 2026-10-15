# Chat401ResponseError


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | 
**code** | **str** |  | [optional] 

## Example

```python
from yggy.models.chat401_response_error import Chat401ResponseError

# TODO update the JSON string below
json = "{}"
# create an instance of Chat401ResponseError from a JSON string
chat401_response_error_instance = Chat401ResponseError.from_json(json)
# print the JSON string representation of the object
print(Chat401ResponseError.to_json())

# convert the object into a dict
chat401_response_error_dict = chat401_response_error_instance.to_dict()
# create an instance of Chat401ResponseError from a dict
chat401_response_error_from_dict = Chat401ResponseError.from_dict(chat401_response_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


