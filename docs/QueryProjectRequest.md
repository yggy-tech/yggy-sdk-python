# QueryProjectRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**question** | **str** | The question in plain language. yggy finds the documents that answer it. | 
**top_k** | **int** | How many documents to return, best first. | [optional] [default to 5]
**mode** | **str** | How documents are found and ranked. &#x60;hybrid&#x60; (default) uses the facts yggy extracted and the document text; &#x60;lexical&#x60; uses the document text only; &#x60;graph&#x60; returns only documents the extracted facts point to. | [optional] [default to 'hybrid']
**include** | **List[str]** | Extra knowledge to attach to the answer. &#x60;facts&#x60; (also accepted as &#x60;triples&#x60;) adds the facts extracted from the returned documents; &#x60;entities&#x60; adds the people, organizations and things they mention; &#x60;identity&#x60; adds only entities with an approved identity, such as a register number. | [optional] 
**include_archived** | **bool** | Also search archived facts. They are returned in &#x60;archivedHits&#x60; and brought back into the live graph in the background. Project queries only. | [optional] [default to False]

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


