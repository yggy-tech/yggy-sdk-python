# ListDocumentTriples200ResponseTriplesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**subject** | **str** |  | 
**predicate** | **str** |  | 
**object** | **str** |  | 
**subject_identity** | [**ListDocumentTriples200ResponseTriplesInnerSubjectIdentity**](ListDocumentTriples200ResponseTriplesInnerSubjectIdentity.md) |  | [optional] 
**subject_id** | **str** |  | [optional] 
**subject_type** | **str** |  | [optional] 
**subject_identity_uri** | **str** |  | [optional] 
**object_id** | **str** |  | [optional] 
**object_type** | **str** |  | [optional] 
**object_identity_uri** | **str** |  | [optional] 
**qualifiers** | [**ListDocumentTriples200ResponseTriplesInnerQualifiers**](ListDocumentTriples200ResponseTriplesInnerQualifiers.md) |  | [optional] 
**source** | **str** |  | [optional] 
**extraction_method** | **str** |  | [optional] 
**evidence** | **List[str]** |  | [optional] 
**evidence_region_id** | **str** |  | [optional] 
**note** | **str** |  | [optional] 
**created_at** | **str** |  | [optional] 
**status** | **str** |  | [optional] 

## Example

```python
from yggy.models.list_document_triples200_response_triples_inner import ListDocumentTriples200ResponseTriplesInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListDocumentTriples200ResponseTriplesInner from a JSON string
list_document_triples200_response_triples_inner_instance = ListDocumentTriples200ResponseTriplesInner.from_json(json)
# print the JSON string representation of the object
print(ListDocumentTriples200ResponseTriplesInner.to_json())

# convert the object into a dict
list_document_triples200_response_triples_inner_dict = list_document_triples200_response_triples_inner_instance.to_dict()
# create an instance of ListDocumentTriples200ResponseTriplesInner from a dict
list_document_triples200_response_triples_inner_from_dict = ListDocumentTriples200ResponseTriplesInner.from_dict(list_document_triples200_response_triples_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


