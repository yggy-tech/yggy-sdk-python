# QueryProjectRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**question** | **str** | Natural-language question to retrieve documents for | 
**top_k** | **int** | Maximum number of ranked contexts to return | [optional] [default to 5]
**mode** | **str** | hybrid combines document text with graph matches; lexical uses document text only; graph uses graph matches only | [optional] [default to 'hybrid']
**include** | **List[str]** | Optional graph fields to attach. Omit for the default retrieve body. identity alone returns only entities with an approved identity. | [optional] 
**include_archived** | **bool** | Also search cold triples. Archived hits surface separately and trigger a background promote. Single-project scope only. | [optional] [default to False]

## Example

```python
from yggy.models.query_project_request import QueryProjectRequest

# TODO update the JSON string below
json = "{}"
# create an instance of QueryProjectRequest from a JSON string
query_project_request_instance = QueryProjectRequest.from_json(json)
# print the JSON string representation of the object
print(QueryProjectRequest.to_json())

# convert the object into a dict
query_project_request_dict = query_project_request_instance.to_dict()
# create an instance of QueryProjectRequest from a dict
query_project_request_from_dict = QueryProjectRequest.from_dict(query_project_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


