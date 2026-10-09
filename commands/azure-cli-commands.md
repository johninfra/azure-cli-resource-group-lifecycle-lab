# Azure CLI Commands

This file contains the Azure CLI commands used in the lab.

## Create the Resource Group

```bash
az group create \
  --name rg-demo \
  --location westus2
```

### What the command does

- `az group create` — creates or updates an Azure Resource Group.
- `--name rg-demo` — sets the Resource Group name.
- `--location westus2` — stores the Resource Group metadata in the West US 2 Azure region.

## Delete the Resource Group

```bash
az group delete --name rg-demo
```

Azure CLI prompts for confirmation before deleting the Resource Group:

```text
Are you sure you want to perform this operation? (y/n): y
```

## Optional Verification Commands

These are useful commands for confirming the Resource Group state directly from the CLI.

### Show the Resource Group

```bash
az group show --name rg-demo
```

### List Resource Groups

```bash
az group list --output table
```

### Delete Without Interactive Confirmation

```bash
az group delete --name rg-demo --yes
```

> Use `--yes` only when you are certain the target Resource Group is correct. Resource Group deletion can remove all resources contained within the group.
