# EntityReadEntityIdentity


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uri** | **str** |  | 
**namespace_uri** | **str** |  | 
**authority_approved** | **bool** |  | 
**source_field** | **str** |  | 
**source_value** | **str** |  | 

## Example

```python
from yggy.models.entity_read_entity_identity import EntityReadEntityIdentity

# TODO update the JSON string below
json = "{}"
# create an instance of EntityReadEntityIdentity from a JSON string
entity_read_entity_identity_instance = EntityReadEntityIdentity.from_json(json)
# print the JSON string representation of the object
print(EntityReadEntityIdentity.to_json())

# convert the object into a dict
entity_read_entity_identity_dict = entity_read_entity_identity_instance.to_dict()
# create an instance of EntityReadEntityIdentity from a dict
entity_read_entity_identity_from_dict = EntityReadEntityIdentity.from_dict(entity_read_entity_identity_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


