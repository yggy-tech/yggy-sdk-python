# RetryDocument202Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**document_id** | **str** |  | 
**invocation_id** | **str** |  | 
**status** | **str** |  | 
**message** | **str** |  | 

## Example

```python
from yggy.models.retry_document202_response import RetryDocument202Response

# TODO update the JSON string below
json = "{}"
# create an instance of RetryDocument202Response from a JSON string
retry_document202_response_instance = RetryDocument202Response.from_json(json)
# print the JSON string representation of the object
print(RetryDocument202Response.to_json())

# convert the object into a dict
retry_document202_response_dict = retry_document202_response_instance.to_dict()
# create an instance of RetryDocument202Response from a dict
retry_document202_response_from_dict = RetryDocument202Response.from_dict(retry_document202_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


