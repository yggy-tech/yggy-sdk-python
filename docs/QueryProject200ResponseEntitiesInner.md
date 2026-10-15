# QueryProject200ResponseEntitiesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uri** | **str** | Public entity URI. Never a graph uid. | [optional] 
**label** | **str** |  | 
**type** | **str** | Public class URI | [optional] 
**score** | **float** |  | 
**document_ids** | **List[str]** | Ranked context document ids this entity matched | 
**identity** | [**QueryProject200ResponseEntitiesInnerIdentity**](QueryProject200ResponseEntitiesInnerIdentity.md) |  | [optional] 

## Example

```python
from yggy.models.query_project200_response_entities_inner import QueryProject200ResponseEntitiesInner

# TODO update the JSON string below
json = "{}"
# create an instance of QueryProject200ResponseEntitiesInner from a JSON string
query_project200_response_entities_inner_instance = QueryProject200ResponseEntitiesInner.from_json(json)
# print the JSON string representation of the object
print(QueryProject200ResponseEntitiesInner.to_json())

# convert the object into a dict
query_project200_response_entities_inner_dict = query_project200_response_entities_inner_instance.to_dict()
# create an instance of QueryProject200ResponseEntitiesInner from a dict
query_project200_response_entities_inner_from_dict = QueryProject200ResponseEntitiesInner.from_dict(query_project200_response_entities_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


