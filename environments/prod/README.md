## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | n/a |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_bastion"></a> [bastion](#module\_bastion) | git::https://github.com/Tynchtyk642/TerraformChildModules.git//instance | nazim |
| <a name="module_eks"></a> [eks](#module\_eks) | git::https://github.com/Tynchtyk642/TerraformChildModules.git//eks | nazim |
| <a name="module_vpc"></a> [vpc](#module\_vpc) | git::https://github.com/Tynchtyk642/TerraformChildModules.git//vpc | nazim |

## Resources

| Name | Type |
|------|------|
| [aws_key_pair.deployer](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/key_pair) | resource |
| [aws_ami.ubuntu](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/ami) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_env"></a> [env](#input\_env) | n/a | `string` | `"prod"` | no |
| <a name="input_prefix"></a> [prefix](#input\_prefix) | n/a | `string` | `"prod"` | no |
| <a name="input_pub_key"></a> [pub\_key](#input\_pub\_key) | your pub key | `string` | n/a | yes |

## Outputs

No outputs.
