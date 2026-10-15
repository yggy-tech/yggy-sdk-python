# Chat200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**response** | **str** | The AI&#39;s answer to your question | 
**citations** | [**List[Chat200ResponseDataCitationsInner]**](Chat200ResponseDataCitationsInner.md) | Documents referenced by graph tools | [optional] 
**tool_calls** | [**List[Chat200ResponseDataToolCallsInner]**](Chat200ResponseDataToolCallsInner.md) |  | [optional] 
**usage** | [**Chat200ResponseDataUsage**](Chat200ResponseDataUsage.md) |  | [optional] 
**metadata** | [**Chat200ResponseDataMetadata**](Chat200ResponseDataMetadata.md) |  | 

## Example

```python
from yggy.models.chat200_response_data import Chat200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of Chat200ResponseData from a JSON string
chat200_response_data_instance = Chat200ResponseData.from_json(json)
# print the JSON string representation of the object
print(Chat200ResponseData.to_json())

# convert the object into a dict
chat200_response_data_dict = chat200_response_data_instance.to_dict()
# create an instance of Chat200ResponseData from a dict
chat200_response_data_from_dict = Chat200ResponseData.from_dict(chat200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


