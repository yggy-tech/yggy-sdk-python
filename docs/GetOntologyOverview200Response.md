# GetOntologyOverview200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**totals** | [**GetOntologyOverview200ResponseTotals**](GetOntologyOverview200ResponseTotals.md) |  | 
**version** | **str** |  | 
**base_version** | **str** |  | 
**project_version** | **str** |  | 
**overlay_version** | **str** |  | 

## Example

```python
from yggy.models.get_ontology_overview200_response import GetOntologyOverview200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetOntologyOverview200Response from a JSON string
get_ontology_overview200_response_instance = GetOntologyOverview200Response.from_json(json)
# print the JSON string representation of the object
print(GetOntologyOverview200Response.to_json())

# convert the object into a dict
get_ontology_overview200_response_dict = get_ontology_overview200_response_instance.to_dict()
# create an instance of GetOntologyOverview200Response from a dict
get_ontology_overview200_response_from_dict = GetOntologyOverview200Response.from_dict(get_ontology_overview200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


