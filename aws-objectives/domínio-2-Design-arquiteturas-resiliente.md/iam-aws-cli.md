# IAM & AWS CLI
## IAM:  users and groups

- IAM = identity and acess management, global service.
- root account created by default shouldn't be used os shared.
- ssers are people inside the organization, and can be grouped.
- groups onlye contain users, not other groups.
- users don't have to belong to a group, and user can belong to multiple groups.

![aws-image](https://github.com/aws-expert/learning-aws-solutions-architect/blob/main/images/aws1.png)

## IAM Permissions
- users and groups can be assigned JSON documents called policies.

```json
policy  = {
     <version_block?>
     <id_block?>
     <statement_block>
}

<version_block> = "Version" : ("2008-10-17" | "2012-10-17")

<id_block> = "Id" : <policy_id_string>

<statement_block> = "Statement" : [ <statement>, <statement>, ... ]

<statement> = { 
    <sid_block?>,
    <principal_block?>,
    <effect_block>,
    <action_block>,
    <resource_block>,
    <condition_block?>
}

<sid_block> = "Sid" : <sid_string>

<effect_block> = "Effect" : ("Allow" | "Deny")  

<principal_block> = ("Principal" | "NotPrincipal") : ("*" | <principal_map>)

<principal_map> = { <principal_map_entry>, <principal_map_entry>, ... }

<principal_map_entry> = ("AWS" | "Federated" | "Service" | "CanonicalUser") :   
    [<principal_id_string>, <principal_id_string>, ...]

<action_block> = ("Action" | "NotAction") : 
    ("*" | [<action_string>, <action_string>, ...])

<resource_block> = ("Resource" | "NotResource") : 
    : ("*" | <resource_string> | [<resource_string>, <resource_string>, ...])

<condition_block> = "Condition" : { <condition_map> }
<condition_map> = { 
  <condition_type_string> : { <condition_key_string> : <condition_value_list> },
  <condition_type_string> : { <condition_key_string> : <condition_value_list> }, ...
}  
<condition_value_list> = [<condition_value>, <condition_value>, ...]
<condition_value> = (<condition_value_string> | <condition_value_string> | <condition_value_string>)
```



