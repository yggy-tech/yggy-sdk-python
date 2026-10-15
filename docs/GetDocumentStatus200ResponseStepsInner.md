# GetDocumentStatus200ResponseStepsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | 
**status** | **str** |  | 
**started_at** | **float** |  | [optional] 
**completed_at** | **float** |  | [optional] 
**duration_ms** | **float** |  | [optional] 
**message** | **str** |  | [optional] 
**current** | **float** |  | [optional] 
**total** | **float** |  | [optional] 
**unit** | **str** |  | [optional] 

## Example

```python
from yggy.models.get_document_status200_response_steps_inner import GetDocumentStatus200ResponseStepsInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetDocumentStatus200ResponseStepsInner from a JSON string
get_document_status200_response_steps_inner_instance = GetDocumentStatus200ResponseStepsInner.from_json(json)
# print the JSON string representation of the object
print(GetDocumentStatus200ResponseStepsInner.to_json())

# convert the object into a dict
get_document_status200_response_steps_inner_dict = get_document_status200_response_steps_inner_instance.to_dict()
# create an instance of GetDocumentStatus200ResponseStepsInner from a dict
get_document_status200_response_steps_inner_from_dict = GetDocumentStatus200ResponseStepsInner.from_dict(get_document_status200_response_steps_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


