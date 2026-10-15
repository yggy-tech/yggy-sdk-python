# EntityRead


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**entity** | [**EntityReadEntity**](EntityReadEntity.md) |  | 
**projects** | **List[str]** | Projects the caller can see that hold a fact or literal about the entity (also on the project route) | 
**documents** | [**List[EntityReadDocumentsInner]**](EntityReadDocumentsInner.md) |  | 
**truncated** | **bool** | True when a fact or literal list hit the read cap; the read is partial | 

## Example

```python
from yggy.models.entity_read import EntityRead

# TODO update the JSON string below
json = "{}"
# create an instance of EntityRead from a JSON string
entity_read_instance = EntityRead.from_json(json)
# print the JSON string representation of the object
print(EntityRead.to_json())

# convert the object into a dict
entity_read_dict = entity_read_instance.to_dict()
# create an instance of EntityRead from a dict
entity_read_from_dict = EntityRead.from_dict(entity_read_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


