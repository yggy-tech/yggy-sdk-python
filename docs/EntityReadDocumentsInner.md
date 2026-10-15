# EntityReadDocumentsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**document_id** | **str** |  | 
**title** | **str** |  | 
**facts** | [**List[EntityReadDocumentsInnerFactsInner]**](EntityReadDocumentsInnerFactsInner.md) |  | 
**literals** | [**List[EntityReadDocumentsInnerLiteralsInner]**](EntityReadDocumentsInnerLiteralsInner.md) |  | 

## Example

```python
from yggy.models.entity_read_documents_inner import EntityReadDocumentsInner

# TODO update the JSON string below
json = "{}"
# create an instance of EntityReadDocumentsInner from a JSON string
entity_read_documents_inner_instance = EntityReadDocumentsInner.from_json(json)
# print the JSON string representation of the object
print(EntityReadDocumentsInner.to_json())

# convert the object into a dict
entity_read_documents_inner_dict = entity_read_documents_inner_instance.to_dict()
# create an instance of EntityReadDocumentsInner from a dict
entity_read_documents_inner_from_dict = EntityReadDocumentsInner.from_dict(entity_read_documents_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


