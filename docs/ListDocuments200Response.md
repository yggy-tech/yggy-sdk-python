# ListDocuments200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**documents** | [**List[ListDocuments200ResponseDocumentsInner]**](ListDocuments200ResponseDocumentsInner.md) |  | 
**total** | **float** |  | 
**limit** | **float** |  | 
**offset** | **float** |  | 

## Example

```python
from yggy.models.list_documents200_response import ListDocuments200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListDocuments200Response from a JSON string
list_documents200_response_instance = ListDocuments200Response.from_json(json)
# print the JSON string representation of the object
print(ListDocuments200Response.to_json())

# convert the object into a dict
list_documents200_response_dict = list_documents200_response_instance.to_dict()
# create an instance of ListDocuments200Response from a dict
list_documents200_response_from_dict = ListDocuments200Response.from_dict(list_documents200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


