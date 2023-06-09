## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | 4.54.0 |

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
| <a name="input_env"></a> [env](#input\_env) | n/a | `string` | `"dev"` | no |
| <a name="input_prefix"></a> [prefix](#input\_prefix) | n/a | `string` | `"dev"` | no |
| <a name="input_pub_key"></a> [pub\_key](#input\_pub\_key) | your pub key | `string` | `"ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQC1wyx8VOviYGZ4oeaAgG3uAWMTe15ylT83aNoH6yoq9iRMzMKuVaMDDI9AzIOelu1DNDF4J2CqW5DhUdiwS3OuXxjhuEq9FRXuadZIyh4UA1TbJW2XI4PGj1FuGOU2OCl4I1R4TFiVjsj2FtAIVrkjQrex6TQfNVso6UTINtAszkPTDP00vLhLapQWiW8+R0zMhju+4tuOngsetbsVn5Zo6hMD6UHomhkQiyOsrjHwcYohjlveyICpNNBjnvhrEUxilZRha90XCYdvdqUk+3K1SsnZZmpjUB2N3sXAYfcd8ecOYr5e9NWau6MEM2GSE/YI3WC2VxmRaOaPx5gi80ndUqD9BSIvghA8okXuaJxkQtrj9qgLUEAWlHEZ7SgQ9njrcMrbooE1cWmgx7fygnfDqc1imdlxV590IxDWf2TIEAtgtAz4jVLHyIvrt3ba1L6d7ZLfRISpuIHQJL5Dg2LDgFXXvILUtQWsEa79OJCTYKtD5Id1JpPQB96GMa/E7/E= user@WIN-OKNFOMRMI02"` | no |

## Outputs

No outputs.
