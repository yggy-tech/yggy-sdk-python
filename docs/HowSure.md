# HowSure

How well the fact is backed, decided from its evidence, with the reasons

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**level** | **str** |  | 
**reasons** | [**List[HowSureReasonsInner]**](HowSureReasonsInner.md) |  | 

## Example

```python
from yggy.models.how_sure import HowSure

# TODO update the JSON string below
json = "{}"
# create an instance of HowSure from a JSON string
how_sure_instance = HowSure.from_json(json)
# print the JSON string representation of the object
print(HowSure.to_json())

# convert the object into a dict
how_sure_dict = how_sure_instance.to_dict()
# create an instance of HowSure from a dict
how_sure_from_dict = HowSure.from_dict(how_sure_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


