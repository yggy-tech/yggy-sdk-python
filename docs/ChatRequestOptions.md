# ChatRequestOptions


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tier** | **str** | Model tier for response quality | [optional] [default to 'balanced']

## Example

```python
from yggy.models.chat_request_options import ChatRequestOptions

# TODO update the JSON string below
json = "{}"
# create an instance of ChatRequestOptions from a JSON string
chat_request_options_instance = ChatRequestOptions.from_json(json)
# print the JSON string representation of the object
print(ChatRequestOptions.to_json())

# convert the object into a dict
chat_request_options_dict = chat_request_options_instance.to_dict()
# create an instance of ChatRequestOptions from a dict
chat_request_options_from_dict = ChatRequestOptions.from_dict(chat_request_options_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


