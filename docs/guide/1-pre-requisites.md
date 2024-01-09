# Pre-Requisite step

## Permissions

First, make sure that you have permissions `billing.resourceAssociations.create` on the billing account.

## Terraform
### How
 Apply  [this Terraform module](../terraform/setup/)  (directory `setup`). To that by changing to the `setup` directory, running `terraform init`, then `terraform apply`. You will be asked for the billing account ID and the project ID, or else you can pass this variables in using a `.tfvar` file.

### What it does

1. The TF creates a project to hold your listings and backend integration workloads. The project ID must end in `-public`. The project ID should make clear it is a marketplace project, so for example `my-isv-mp-public`.
2. It grants Google procurement user access to your listing project ([role detail](../terraform/setup/iam.tf)).
3. It creates a service account to run your integration workloads.
4. It verify that the user applying the app deploy terraform has `serviceAccountTokenCreator` role on the `doit-easily` SA created in this step


# Next Steps

[setup the listing](2-setup-the-listing.md)