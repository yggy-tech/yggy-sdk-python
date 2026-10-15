# UploadDocument400Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] [default to False]
**error** | **str** |  | 
**message** | **str** |  | [optional] 

## Example

```python
from yggy.models.upload_document400_response import UploadDocument400Response

# TODO update the JSON string below
json = "{}"
# create an instance of UploadDocument400Response from a JSON string
upload_document400_response_instance = UploadDocument400Response.from_json(json)
# print the JSON string representation of the object
print(UploadDocument400Response.to_json())

# convert the object into a dict
upload_document400_response_dict = upload_document400_response_instance.to_dict()
# create an instance of UploadDocument400Response from a dict
upload_document400_response_from_dict = UploadDocument400Response.from_dict(upload_document400_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


