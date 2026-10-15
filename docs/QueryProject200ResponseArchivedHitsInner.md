# QueryProject200ResponseArchivedHitsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**triple_key** | **str** |  | 
**text** | **str** | Verbalized cold fact, e.g. subject predicate object | 
**score** | **float** |  | 

## Example

```python
from yggy.models.query_project200_response_archived_hits_inner import QueryProject200ResponseArchivedHitsInner

# TODO update the JSON string below
json = "{}"
# create an instance of QueryProject200ResponseArchivedHitsInner from a JSON string
query_project200_response_archived_hits_inner_instance = QueryProject200ResponseArchivedHitsInner.from_json(json)
# print the JSON string representation of the object
print(QueryProject200ResponseArchivedHitsInner.to_json())

# convert the object into a dict
query_project200_response_archived_hits_inner_dict = query_project200_response_archived_hits_inner_instance.to_dict()
# create an instance of QueryProject200ResponseArchivedHitsInner from a dict
query_project200_response_archived_hits_inner_from_dict = QueryProject200ResponseArchivedHitsInner.from_dict(query_project200_response_archived_hits_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


