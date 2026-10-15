# UploadDocument202Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**document_id** | **str** |  | 
**internal_id** | **str** |  | 
**invocation_id** | **str** |  | 
**status** | **str** | stored: saved without analysis because the account has no credits | 
**storage_path** | **str** |  | 
**storage_url** | **str** |  | 
**message** | **str** |  | 

## Example

```python
from yggy.models.upload_document202_response import UploadDocument202Response

# TODO update the JSON string below
json = "{}"
# create an instance of UploadDocument202Response from a JSON string
upload_document202_response_instance = UploadDocument202Response.from_json(json)
# print the JSON string representation of the object
print(UploadDocument202Response.to_json())

# convert the object into a dict
upload_document202_response_dict = upload_document202_response_instance.to_dict()
# create an instance of UploadDocument202Response from a dict
upload_document202_response_from_dict = UploadDocument202Response.from_dict(upload_document202_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


