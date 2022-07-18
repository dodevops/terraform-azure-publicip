# Public IP for Azure

## Introduction

This module manages a public IP for Azure

## Usage

Instantiate the module by calling it from Terraform like this:

```hcl
module "azure-basics" {
  source  = "dodevops/publicip/azure"
  version = "<version>"
}
```

<!-- BEGIN_TF_DOCS -->
## Requirements

No requirements.

## Providers

The following providers are used by this module:

- azurerm

## Modules

No modules.

## Resources

The following resources are used by this module:

- [azurerm_public_ip.public-ip](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/public_ip) (resource)

## Required Inputs

The following input variables are required:

### location

Description: Azure location to use

Type: `string`

### project

Description: Three letter project key

Type: `string`

### resource\_group

Description: Azure Resource Group to use

Type: `string`

### stage

Description: Stage for this ip

Type: `string`

## Optional Inputs

The following input variables are optional (have default values):

### sku

Description: The SKU used for this ip

Type: `string`

Default: `"Standard"`

### suffix

Description: ip address name suffix

Type: `string`

Default: `""`

## Outputs

The following outputs are exported:

### id

Description: n/a

### ip

Description: n/a

### resource\_group

Description: n/a
<!-- END_TF_DOCS -->


## Development

Use [terraform-docs](https://terraform-docs.io/) to generate the API documentation by running

    terraform fmt .
    terraform-docs .