# Chat401Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**error** | [**Chat401ResponseError**](Chat401ResponseError.md) |  | 

## Example

```python
from yggy.models.chat401_response import Chat401Response

# TODO update the JSON string below
json = "{}"
# create an instance of Chat401Response from a JSON string
chat401_response_instance = Chat401Response.from_json(json)
# print the JSON string representation of the object
print(Chat401Response.to_json())

# convert the object into a dict
chat401_response_dict = chat401_response_instance.to_dict()
# create an instance of Chat401Response from a dict
chat401_response_from_dict = Chat401Response.from_dict(chat401_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


