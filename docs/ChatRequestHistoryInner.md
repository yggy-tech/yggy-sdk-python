# ChatRequestHistoryInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** | Message role | 
**content** | **str** | Message content | 

## Example

```python
from yggy.models.chat_request_history_inner import ChatRequestHistoryInner

# TODO update the JSON string below
json = "{}"
# create an instance of ChatRequestHistoryInner from a JSON string
chat_request_history_inner_instance = ChatRequestHistoryInner.from_json(json)
# print the JSON string representation of the object
print(ChatRequestHistoryInner.to_json())

# convert the object into a dict
chat_request_history_inner_dict = chat_request_history_inner_instance.to_dict()
# create an instance of ChatRequestHistoryInner from a dict
chat_request_history_inner_from_dict = ChatRequestHistoryInner.from_dict(chat_request_history_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


