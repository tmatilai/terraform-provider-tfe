---
layout: "tfe"
page_title: "Terraform Enterprise: tfe_variable_set"
description: |-
  Get information on organization variable sets.
---


<!-- Please do not edit this file, it is generated. -->
# Data Source: tfe_variable_set

This data source is used to retrieve a named variable set

## Example Usage

For workspace variables:

```python
import constructs as constructs
import cdktf as cdktf
# Provider bindings are generated by running cdktf get.
# See https://cdk.tf/provider-generation for more details.
import ...gen.providers.tfe as tfe
class MyConvertedCode(cdktf.TerraformStack):
    def __init__(self, scope, name):
        super().__init__(scope, name)
        tfe.data_tfe_variable_set.DataTfeVariableSet(self, "test",
            name="my-variable-set-name",
            organization="my-org-name"
        )
```

## Argument Reference

The following arguments are supported:

* `name` - (Required) Name of the variable set.
* `organization` - (Required) Name of the organization.

## Attributes Reference

* `id` - The ID of the variable.
* `organization` - Name of the organization.
* `name` - Name of the variable set.
* `description` - Description of the variable set.
* `global` - Whether the variable set applies to all workspaces in the organization.
* `priority` - Whether the variables in this set are able to be over-written.
* `workspace_ids` - IDs of the workspaces that use the variable set.
* `variable_ids` - IDs of the variables attached to the variable set.
* `project_ids` - IDs of the projects that use the variable set.
* `parent_project_id` - ID of the project that owns the variable set.

<!-- cache-key: cdktf-0.17.0-pre.15 input-bf1bfbd6988140f428db72c174b6b91d124e83198e36d64ed719ce367b5f38fe -->