# QueryProject200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**answer** | **str** | The sentence from the best document that answers the question. Empty when nothing matched. | 
**contexts** | [**List[QueryProject200ResponseContextsInner]**](QueryProject200ResponseContextsInner.md) | The documents that answer the question, best first | 
**entities** | [**List[QueryProject200ResponseEntitiesInner]**](QueryProject200ResponseEntitiesInner.md) | Present when &#x60;include&#x60; asks for entities or identity | [optional] 
**triples** | [**List[QueryProject200ResponseTriplesInner]**](QueryProject200ResponseTriplesInner.md) | The facts of the returned documents. Present when &#x60;include&#x60; asks for facts (or triples). | [optional] 
**archived_hits** | [**List[QueryProject200ResponseArchivedHitsInner]**](QueryProject200ResponseArchivedHitsInner.md) | Present when includeArchived was requested on a single project | [optional] 

## Example

```python
from yggy.models.query_project200_response import QueryProject200Response

# TODO update the JSON string below
json = "{}"
# create an instance of QueryProject200Response from a JSON string
query_project200_response_instance = QueryProject200Response.from_json(json)
# print the JSON string representation of the object
print(QueryProject200Response.to_json())

# convert the object into a dict
query_project200_response_dict = query_project200_response_instance.to_dict()
# create an instance of QueryProject200Response from a dict
query_project200_response_from_dict = QueryProject200Response.from_dict(query_project200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


