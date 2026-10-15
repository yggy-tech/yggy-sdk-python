# QueryProject200ResponseEntitiesInnerIdentity


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**namespace_uri** | **str** | Approved identity namespace, for example a Wikidata entity prefix | 
**value** | **str** | Value in that namespace | 

## Example

```python
from yggy.models.query_project200_response_entities_inner_identity import QueryProject200ResponseEntitiesInnerIdentity

# TODO update the JSON string below
json = "{}"
# create an instance of QueryProject200ResponseEntitiesInnerIdentity from a JSON string
query_project200_response_entities_inner_identity_instance = QueryProject200ResponseEntitiesInnerIdentity.from_json(json)
# print the JSON string representation of the object
print(QueryProject200ResponseEntitiesInnerIdentity.to_json())

# convert the object into a dict
query_project200_response_entities_inner_identity_dict = query_project200_response_entities_inner_identity_instance.to_dict()
# create an instance of QueryProject200ResponseEntitiesInnerIdentity from a dict
query_project200_response_entities_inner_identity_from_dict = QueryProject200ResponseEntitiesInnerIdentity.from_dict(query_project200_response_entities_inner_identity_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


