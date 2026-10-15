# Chat200ResponseDataCitationsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**document_id** | **str** | Document that grounded the answer | 
**source** | **str** | Caller-supplied source id when present | [optional] 
**snippet** | **str** | Evidence text when the tool returned it | [optional] 

## Example

```python
from yggy.models.chat200_response_data_citations_inner import Chat200ResponseDataCitationsInner

# TODO update the JSON string below
json = "{}"
# create an instance of Chat200ResponseDataCitationsInner from a JSON string
chat200_response_data_citations_inner_instance = Chat200ResponseDataCitationsInner.from_json(json)
# print the JSON string representation of the object
print(Chat200ResponseDataCitationsInner.to_json())

# convert the object into a dict
chat200_response_data_citations_inner_dict = chat200_response_data_citations_inner_instance.to_dict()
# create an instance of Chat200ResponseDataCitationsInner from a dict
chat200_response_data_citations_inner_from_dict = Chat200ResponseDataCitationsInner.from_dict(chat200_response_data_citations_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


