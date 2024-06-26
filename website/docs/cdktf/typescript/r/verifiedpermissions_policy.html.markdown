---
subcategory: "Verified Permissions"
layout: "aws"
page_title: "AWS: aws_verifiedpermissions_policy"
description: |-
  Terraform resource for managing an AWS Verified Permissions Policy.
---


<!-- Please do not edit this file, it is generated. -->
# Resource: aws_verifiedpermissions_policy

Terraform resource for managing an AWS Verified Permissions Policy.

## Example Usage

### Basic Usage

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { VerifiedpermissionsPolicy } from "./.gen/providers/aws/";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    new VerifiedpermissionsPolicy(this, "test", {
      definition: [
        {
          static: [
            {
              statement:
                'permit (principal, action == Action::\\"view\\", resource in Album:: \\"test_album\\");',
            },
          ],
        },
      ],
      policy_store_id: awsVerifiedpermissionsPolicyStoreTest.id,
    });
  }
}

```

## Argument Reference

The following arguments are required:

* `policyStoreId` - (Required) The Policy Store ID of the policy store.
* `definition`- (Required) The definition of the policy. See [Definition](#definition) below.

The following arguments are optional:

* `optional_arg` - (Optional) Concise argument description. Do not begin the description with "An", "The", "Defines", "Indicates", or "Specifies," as these are verbose. In other words, "Indicates the amount of storage," can be rewritten as "Amount of storage," without losing any information.

### Definition

* `static` - (Optional) The static policy statement. See [Static](#static) below.
* `template_linked` - (Optional) The template linked policy. See [Template Linked](#template-linked) below.

#### Static

* `description` - (Optional) The description of the static policy.
* `statement` - (Required) The statement of the static policy.

#### Template Linked

* `policyTemplateId` - (Required) The ID of the template.
* `principal` - (Optional) The principal of the template linked policy.
    * `entityId` - (Required) The entity ID of the principal.
    * `entity_type` - (Required) The entity type of the principal.
* `resource` - (Optional) The resource of the template linked policy.
    * `entityId` - (Required) The entity ID of the resource.
    * `entity_type` - (Required) The entity type of the resource.

## Attribute Reference

This resource exports the following attributes in addition to the arguments above:

* `arn` - ARN of the Policy. Do not begin the description with "An", "The", "Defines", "Indicates", or "Specifies," as these are verbose. In other words, "Indicates the amount of storage," can be rewritten as "Amount of storage," without losing any information.
* `example_attribute` - Concise description. Do not begin the description with "An", "The", "Defines", "Indicates", or "Specifies," as these are verbose. In other words, "Indicates the amount of storage," can be rewritten as "Amount of storage," without losing any information.

## Import

In Terraform v1.5.0 and later, use an [`import` block](https://developer.hashicorp.com/terraform/language/import) to import Verified Permissions Policy using the `policy_id,policy_store_id`. For example:

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { VerifiedpermissionsPolicy } from "./.gen/providers/aws/";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    VerifiedpermissionsPolicy.generateConfigForImport(
      this,
      "example",
      "policy-id-12345678,policy-store-id-12345678"
    );
  }
}

```

Using `terraform import`, import Verified Permissions Policy using the `policy_id,policy_store_id`. For example:

```console
% terraform import aws_verifiedpermissions_policy.example policy-id-12345678,policy-store-id-12345678
```

<!-- cache-key: cdktf-0.20.1 input-7a5f5dea17f06f1f84a754f0e6e8701e7b76925aba65613982002d2fb8f3dce0 -->