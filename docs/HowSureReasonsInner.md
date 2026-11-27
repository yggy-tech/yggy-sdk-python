# HowSureReasonsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **str** |  | 
**review_id** | **str** | The open review item that holds both facts | 
**other_value** | **str** | What the other fact says, null when you cannot read it | 
**count** | **int** | Documents behind the fact | 

## Example

```python
from yggy.models.how_sure_reasons_inner import HowSureReasonsInner

# TODO update the JSON string below
json = "{}"
# create an instance of HowSureReasonsInner from a JSON string
how_sure_reasons_inner_instance = HowSureReasonsInner.from_json(json)
# print the JSON string representation of the object
print(HowSureReasonsInner.to_json())

# convert the object into a dict
how_sure_reasons_inner_dict = how_sure_reasons_inner_instance.to_dict()
# create an instance of HowSureReasonsInner from a dict
how_sure_reasons_inner_from_dict = HowSureReasonsInner.from_dict(how_sure_reasons_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


