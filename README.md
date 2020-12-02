# terraform-aws-iam_instance_profile
This module creates an `iam_instance_profile` based on provided allowed actions and resources. The module is built for Terraform version 0.12

## Examples
See also [/examples/default] a complete working example.


## Usages
```
module "iam_instance_profile" {
    source = "DTherHtun/iip/aws
    name = var.name
    actions = [
        "s3:*",
        "rds:*",
        "logs:*",
    ]
}

##
```

## Outputs:
The name of the iam_instance_profile: `module.iam_instance_profile.name`

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| terraform | >= 0.12.0 |

## Providers

| Name | Version |
|------|---------|
| aws | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| actions | Actions allowed for this instance profile. | `list(string)` | <pre>[<br>  "logs:*"<br>]</pre> | no |
| name | Name used for created resources. | `string` | `null` | no |
| resources | Resources allowed to access by this instance profile. | `list(string)` | <pre>[<br>  "*"<br>]</pre> | no |

## Outputs

| Name | Description |
|------|-------------|
| name | Name of create instance profile |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
