# EntityReadEntity


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**label** | **str** |  | 
**type** | **str** |  | 
**aliases** | **List[str]** |  | 
**canonical_id** | **str** |  | 
**identity** | [**EntityReadEntityIdentity**](EntityReadEntityIdentity.md) |  | 
**home_project_external_id** | **str** |  | 

## Example

```python
from yggy.models.entity_read_entity import EntityReadEntity

# TODO update the JSON string below
json = "{}"
# create an instance of EntityReadEntity from a JSON string
entity_read_entity_instance = EntityReadEntity.from_json(json)
# print the JSON string representation of the object
print(EntityReadEntity.to_json())

# convert the object into a dict
entity_read_entity_dict = entity_read_entity_instance.to_dict()
# create an instance of EntityReadEntity from a dict
entity_read_entity_from_dict = EntityReadEntity.from_dict(entity_read_entity_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


