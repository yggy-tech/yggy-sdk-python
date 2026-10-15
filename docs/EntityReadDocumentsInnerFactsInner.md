# EntityReadDocumentsInnerFactsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**direction** | **str** |  | 
**predicate** | **str** |  | 
**status** | **str** |  | 
**project_external_id** | **str** |  | 
**other** | [**EntityReadDocumentsInnerFactsInnerOther**](EntityReadDocumentsInnerFactsInnerOther.md) |  | 

## Example

```python
from yggy.models.entity_read_documents_inner_facts_inner import EntityReadDocumentsInnerFactsInner

# TODO update the JSON string below
json = "{}"
# create an instance of EntityReadDocumentsInnerFactsInner from a JSON string
entity_read_documents_inner_facts_inner_instance = EntityReadDocumentsInnerFactsInner.from_json(json)
# print the JSON string representation of the object
print(EntityReadDocumentsInnerFactsInner.to_json())

# convert the object into a dict
entity_read_documents_inner_facts_inner_dict = entity_read_documents_inner_facts_inner_instance.to_dict()
# create an instance of EntityReadDocumentsInnerFactsInner from a dict
entity_read_documents_inner_facts_inner_from_dict = EntityReadDocumentsInnerFactsInner.from_dict(entity_read_documents_inner_facts_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


