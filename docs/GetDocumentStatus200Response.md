# GetDocumentStatus200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**document_id** | **str** |  | 
**step** | **str** |  | [optional] 
**progress** | **float** |  | 
**message** | **str** |  | [optional] 
**paused** | **bool** |  | [optional] 
**completed** | **bool** |  | 
**failed** | **bool** |  | 
**stored** | **bool** |  | [optional] 
**awaiting_ontology_review** | **bool** |  | [optional] 
**ontology_review_id** | **str** |  | [optional] 
**ontology_proposal_count** | **float** |  | [optional] 
**error** | **str** |  | [optional] 
**code** | **str** |  | [optional] 
**failure_message** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**workflow_error** | **str** |  | [optional] 
**retryable** | **bool** |  | [optional] 
**triples_extracted** | **float** |  | [optional] 
**input_tokens** | **float** |  | [optional] 
**output_tokens** | **float** |  | [optional] 
**extraction_tier** | **str** |  | [optional] 
**extraction_mode** | **str** |  | [optional] 
**estimated_remaining_ms** | **float** |  | [optional] 
**steps** | [**List[GetDocumentStatus200ResponseStepsInner]**](GetDocumentStatus200ResponseStepsInner.md) |  | [optional] 
**stages** | [**List[GetDocumentStatus200ResponseStepsInner]**](GetDocumentStatus200ResponseStepsInner.md) |  | [optional] 
**invocation_id** | **str** |  | [optional] 
**updated_at** | **float** |  | 

## Example

```python
from yggy.models.get_document_status200_response import GetDocumentStatus200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetDocumentStatus200Response from a JSON string
get_document_status200_response_instance = GetDocumentStatus200Response.from_json(json)
# print the JSON string representation of the object
print(GetDocumentStatus200Response.to_json())

# convert the object into a dict
get_document_status200_response_dict = get_document_status200_response_instance.to_dict()
# create an instance of GetDocumentStatus200Response from a dict
get_document_status200_response_from_dict = GetDocumentStatus200Response.from_dict(get_document_status200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


