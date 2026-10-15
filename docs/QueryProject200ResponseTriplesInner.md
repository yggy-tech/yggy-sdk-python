# QueryProject200ResponseTriplesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subject** | [**QueryProject200ResponseTriplesInnerSubject**](QueryProject200ResponseTriplesInnerSubject.md) |  | 
**predicate** | [**QueryProject200ResponseTriplesInnerSubject**](QueryProject200ResponseTriplesInnerSubject.md) |  | 
**object** | [**QueryProject200ResponseTriplesInnerSubject**](QueryProject200ResponseTriplesInnerSubject.md) |  | 
**evidence** | **str** | Stored hit text. Omitted when the graph hit has none. | [optional] 
**document_id** | **str** |  | [optional] 

## Example

```python
from yggy.models.query_project200_response_triples_inner import QueryProject200ResponseTriplesInner

# TODO update the JSON string below
json = "{}"
# create an instance of QueryProject200ResponseTriplesInner from a JSON string
query_project200_response_triples_inner_instance = QueryProject200ResponseTriplesInner.from_json(json)
# print the JSON string representation of the object
print(QueryProject200ResponseTriplesInner.to_json())

# convert the object into a dict
query_project200_response_triples_inner_dict = query_project200_response_triples_inner_instance.to_dict()
# create an instance of QueryProject200ResponseTriplesInner from a dict
query_project200_response_triples_inner_from_dict = QueryProject200ResponseTriplesInner.from_dict(query_project200_response_triples_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


