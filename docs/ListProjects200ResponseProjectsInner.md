# ListProjects200ResponseProjectsInner


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
**visibility** | **str** | Who in the organization can see that this project exists. &#x60;private&#x60; (the default): only project members and organization owners and admins. &#x60;public&#x60;: every organization member sees its name in the project list, but only members can open it. A personal project (My files) is always &#x60;private&#x60;. | 
**extraction_purpose** | **str** |  | [optional] 
**extraction_include** | **List[str]** |  | [optional] 
**extraction_skip** | **List[str]** |  | [optional] 
**extraction_guidance_revision** | **int** |  | [optional] 
**entity_merge_mode** | **str** |  | [optional] 
**created_at** | **str** |  | [optional] 
**updated_at** | **str** |  | [optional] 
**document_count** | **int** | Documents in the project. Null when &#x60;isMember&#x60; is false: a public project&#39;s numbers are for its members only. | 
**triple_count** | **int** | Relations (triples) in the project. Null when &#x60;isMember&#x60; is false: a public project&#39;s numbers are for its members only. | 
**entity_count** | **int** | Entities in the project. Null when &#x60;isMember&#x60; is false: a public project&#39;s numbers are for its members only. | 
**is_member** | **bool** | True when the caller can open the project: a project member, an organization owner or admin, or an organization API key. False for a public project the caller is not a member of. | 

## Example

```python
from yggy.models.list_projects200_response_projects_inner import ListProjects200ResponseProjectsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListProjects200ResponseProjectsInner from a JSON string
list_projects200_response_projects_inner_instance = ListProjects200ResponseProjectsInner.from_json(json)
# print the JSON string representation of the object
print(ListProjects200ResponseProjectsInner.to_json())

# convert the object into a dict
list_projects200_response_projects_inner_dict = list_projects200_response_projects_inner_instance.to_dict()
# create an instance of ListProjects200ResponseProjectsInner from a dict
list_projects200_response_projects_inner_from_dict = ListProjects200ResponseProjectsInner.from_dict(list_projects200_response_projects_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


