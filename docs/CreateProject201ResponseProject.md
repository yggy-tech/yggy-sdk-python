# CreateProject201ResponseProject


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**slug** | **str** |  | 
**name** | **str** |  | 
**color** | **str** |  | 
**organization_id** | **str** |  | 
**external_id** | **str** |  | [optional] 
**kind** | **str** |  | [optional] 
**extraction_purpose** | **str** |  | [optional] 
**extraction_include** | **List[str]** |  | [optional] 
**extraction_skip** | **List[str]** |  | [optional] 
**extraction_guidance_revision** | **int** |  | [optional] 
**entity_merge_mode** | **str** |  | [optional] 
**created_at** | **str** |  | [optional] 
**updated_at** | **str** |  | [optional] 

## Example

```python
from yggy.models.create_project201_response_project import CreateProject201ResponseProject

# TODO update the JSON string below
json = "{}"
# create an instance of CreateProject201ResponseProject from a JSON string
create_project201_response_project_instance = CreateProject201ResponseProject.from_json(json)
# print the JSON string representation of the object
print(CreateProject201ResponseProject.to_json())

# convert the object into a dict
create_project201_response_project_dict = create_project201_response_project_instance.to_dict()
# create an instance of CreateProject201ResponseProject from a dict
create_project201_response_project_from_dict = CreateProject201ResponseProject.from_dict(create_project201_response_project_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


