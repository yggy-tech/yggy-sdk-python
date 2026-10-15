# Chat200ResponseDataUsage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**input_tokens** | **float** |  | [optional] 
**output_tokens** | **float** |  | [optional] 
**total_tokens** | **float** |  | [optional] 

## Example

```python
from yggy.models.chat200_response_data_usage import Chat200ResponseDataUsage

# TODO update the JSON string below
json = "{}"
# create an instance of Chat200ResponseDataUsage from a JSON string
chat200_response_data_usage_instance = Chat200ResponseDataUsage.from_json(json)
# print the JSON string representation of the object
print(Chat200ResponseDataUsage.to_json())

# convert the object into a dict
chat200_response_data_usage_dict = chat200_response_data_usage_instance.to_dict()
# create an instance of Chat200ResponseDataUsage from a dict
chat200_response_data_usage_from_dict = Chat200ResponseDataUsage.from_dict(chat200_response_data_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


