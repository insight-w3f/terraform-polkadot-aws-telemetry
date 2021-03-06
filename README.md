# terraform-polkadot-aws-telemetry

[![open-issues](https://img.shields.io/github/issues-raw/insight-w3f/terraform-polkadot-aws-telemetry?style=for-the-badge)](https://github.com/insight-w3f/terraform-polkadot-aws-telemetry/issues)
[![open-pr](https://img.shields.io/github/issues-pr-raw/insight-w3f/terraform-polkadot-aws-telemetry?style=for-the-badge)](https://github.com/insight-w3f/terraform-polkadot-aws-telemetry/pulls)

This module deploys a [Substrate telemetry server](https://github.com/paritytech/substrate-telemetry) for use in your Substrate/Polkadot deployment.
You only require one server per deployment.

## Terraform Versions

For Terraform v0.12.0+

## Usage

```
module "this" {
    source = "github.com/insight-w3f/terraform-polkadot-aws-telemetry"

}
```
## Examples

- [defaults](https://github.com/insight-w3f/terraform-polkadot-aws-telemetry/tree/master/examples/defaults)

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

No requirements.

## Providers

No provider.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| create\_dns | Boolean to enable DNS record creation | `bool` | `false` | no |
| domain\_name | Root domain name for deployment (as is present in Route53) | `string` | `""` | no |
| host\_name | Hostname for server (i.e. "telemetry") | `string` | `"telemetry"` | no |
| name | A unique id for the deployment | `string` | `""` | no |
| private\_key\_path | Path to private key | `string` | `""` | no |
| public\_key\_path | Path to public key | `string` | `""` | no |
| subnet\_id | ID for the subnet to deploy into | `string` | `null` | no |
| vpc\_id | ID for the VPC to deploy into | `string` | `null` | no |

## Outputs

| Name | Description |
|------|-------------|
| endpoint\_ip | n/a |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

## Testing
This module has been packaged with terratest tests

To run them:

1. Install Go
2. Run `make test-init` from the root of this repo
3. Run `make test` again from root

## Authors

Module managed by [Richard Mah](https://github.com/shinyfoil)

## Credits

- [Anton Babenko](https://github.com/antonbabenko)

## License

Apache 2 Licensed. See LICENSE for full details.