# ListDocumentTriples200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**triples** | [**List[ListDocumentTriples200ResponseTriplesInner]**](ListDocumentTriples200ResponseTriplesInner.md) |  | 
**count** | **float** |  | 

## Example

```python
from yggy.models.list_document_triples200_response import ListDocumentTriples200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListDocumentTriples200Response from a JSON string
list_document_triples200_response_instance = ListDocumentTriples200Response.from_json(json)
# print the JSON string representation of the object
print(ListDocumentTriples200Response.to_json())

# convert the object into a dict
list_document_triples200_response_dict = list_document_triples200_response_instance.to_dict()
# create an instance of ListDocumentTriples200Response from a dict
list_document_triples200_response_from_dict = ListDocumentTriples200Response.from_dict(list_document_triples200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


