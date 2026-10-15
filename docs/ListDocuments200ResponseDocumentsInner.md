# ListDocuments200ResponseDocumentsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**document_id** | **str** |  | 
**invocation_id** | **str** |  | [optional] 
**title** | **str** |  | 
**content** | **str** |  | [optional] 
**source** | **str** |  | [optional] 
**source_kind** | **str** |  | [optional] 
**origin_system** | **str** |  | [optional] 
**owner_external_id** | **str** |  | [optional] 
**owner_display_name** | **str** |  | [optional] 
**content_type** | **str** |  | 
**status** | **str** |  | 
**created_at** | **str** |  | 
**updated_at** | **str** |  | 
**triple_count** | **float** |  | [optional] 
**error** | **str** |  | [optional] 
**code** | **str** |  | [optional] 
**failure_message** | **str** |  | [optional] 
**storage_url** | **str** |  | [optional] 
**deleted_at** | **str** |  | [optional] 
**extraction_method** | **str** |  | [optional] 
**structured_regions** | **str** |  | [optional] 
**provenance_chain** | **str** |  | [optional] 
**extraction_stats** | **str** |  | [optional] 
**processing_summary** | **str** |  | [optional] 
**model_used** | **str** |  | [optional] 
**ocr_strategy** | **str** |  | [optional] 
**inference_mode** | **str** |  | [optional] 
**extraction_guidance_revision** | **int** |  | [optional] 
**guidance_recommendations** | **str** |  | [optional] 
**source_created_at** | **str** |  | [optional] 
**source_modified_at** | **str** |  | [optional] 
**source_author** | **str** |  | [optional] 
**source_metadata** | **str** |  | [optional] 
**project_external_id** | **str** |  | [optional] 

## Example

```python
from yggy.models.list_documents200_response_documents_inner import ListDocuments200ResponseDocumentsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListDocuments200ResponseDocumentsInner from a JSON string
list_documents200_response_documents_inner_instance = ListDocuments200ResponseDocumentsInner.from_json(json)
# print the JSON string representation of the object
print(ListDocuments200ResponseDocumentsInner.to_json())

# convert the object into a dict
list_documents200_response_documents_inner_dict = list_documents200_response_documents_inner_instance.to_dict()
# create an instance of ListDocuments200ResponseDocumentsInner from a dict
list_documents200_response_documents_inner_from_dict = ListDocuments200ResponseDocumentsInner.from_dict(list_documents200_response_documents_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


