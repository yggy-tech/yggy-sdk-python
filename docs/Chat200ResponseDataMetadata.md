# Chat200ResponseDataMetadata


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**processing_time_ms** | **float** |  | 
**tier_applied** | **str** |  | 

## Example

```python
from yggy.models.chat200_response_data_metadata import Chat200ResponseDataMetadata

# TODO update the JSON string below
json = "{}"
# create an instance of Chat200ResponseDataMetadata from a JSON string
chat200_response_data_metadata_instance = Chat200ResponseDataMetadata.from_json(json)
# print the JSON string representation of the object
print(Chat200ResponseDataMetadata.to_json())

# convert the object into a dict
chat200_response_data_metadata_dict = chat200_response_data_metadata_instance.to_dict()
# create an instance of Chat200ResponseDataMetadata from a dict
chat200_response_data_metadata_from_dict = Chat200ResponseDataMetadata.from_dict(chat200_response_data_metadata_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


