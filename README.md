# module-ixload-app/azurerm

## Description
Terraform module for IxLoad application deployment on Microsoft Azure

## Deployment
This module creates a single instance having a single network interface.

## Usage
```tf
module "App" {
	source  = "armdupre/module-ixload-app/azurerm"
	AdminPassword = local.AppAdminPassword
	Eth0SubnetId = module.Vnet.PublicSubnet.id
	ResourceGroupName = azurerm_resource_group.ResourceGroup.name
}
```