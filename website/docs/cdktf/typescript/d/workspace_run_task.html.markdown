---
layout: "tfe"
page_title: "Terraform Enterprise: tfe_workspace_task"
description: |-
  Get information on a Workspace Run task.
---


<!-- Please do not edit this file, it is generated. -->
# Data Source: tfe_workspace_task

[Run tasks](https://developer.hashicorp.com/terraform/cloud-docs/workspaces/settings/run-tasks) allow HCP Terraform to interact with external systems at specific points in the HCP Terraform run lifecycle. Run tasks are reusable configurations that you can attach to any workspace in an organization.

Use this data source to get information about a [Workspace Run tasks](https://developer.hashicorp.com/terraform/cloud-docs/workspaces/settings/run-tasks#associating-run-tasks-with-a-workspace).

## Example Usage

```typescript
import * as constructs from "constructs";
import * as cdktf from "cdktf";
/*Provider bindings are generated by running cdktf get.
See https://cdk.tf/provider-generation for more details.*/
import * as tfe from "./.gen/providers/tfe";
class MyConvertedCode extends cdktf.TerraformStack {
  constructor(scope: constructs.Construct, name: string) {
    super(scope, name);
    new tfe.dataTfeWorkspaceRunTask.DataTfeWorkspaceRunTask(this, "foobar", {
      taskId: "task-def456",
      workspaceId: "ws-abc123",
    });
  }
}

```

## Argument Reference

The following arguments are supported:

* `taskId` - (Required) The id of the run task.
* `workspaceId` - (Required) The id of the workspace.

## Attributes Reference

In addition to all arguments above, the following attributes are exported:

* `enforcementLevel` - The enforcement level of the task.
* `id` - The ID of the Workspace Run task.
* `stage` - **Deprecated** Use `stages` instead.
* `stages` - Which stages the task will run in.

<!-- cache-key: cdktf-0.17.0-pre.15 input-7fbd90d138dd4a2dc68a0f3441cd300ba07517660e0b7b4fdab7dbddd51d71b5 -->