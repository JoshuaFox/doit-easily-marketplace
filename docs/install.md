# DoiT-Easily Installation Guide


## Terraform modules

There are two Terraform modules here, under `docs/terraform`, `setup` and `app_deploy`, to be used at the steps as stated below.

When you  apply the modules with `terraform apply` in the relevant subdirectory, you must provide variable values, either:

1. By default, you will have to manually enter variables like billing account ID or project ID.
2. Or you can provide a `.tfvars` file with variables.

As an alternative to `terraform apply` in the modules (subdirs) of this project, you can also copy the pertinent files to your own terraform modules and apply them there. You can also integrate these Terraform modules into your CI/CD system. While we strive to not make breaking changes the Terraform modules, we can't promise we won't.

## The Install Process

This process is the distilled instructions found [here][3], plus information to deploy Doit-Easily.

1. [pre-requisites](guide/1-pre-requisites.md); use Terraform `docs/terraform/setup`.
1. [setup the listing](guide/2-setup-the-listing.md)
1. [deploy app](guide/3-deploy-app.md); use Terraform `docs/terraform/app_deploy`.
1. [test the deployment](guide/4-test-deployment.md)
1. [publish](guide/5-publish-listing.md)

## FAQ

See the [faq](faq.md)

## Testing

See the [testing doc](testing.md)



[3]: https://cloud.google.com/marketplace/docs/partners/integrated-saas#checklist
[5]: install-cloudrun.md
[6]: terraform/setup
[7]: gcloud/setup
[8]: terraform/app_deploy
[9]: terraform/setup/iam.tf
[10]: testing.md
[11]: terraform/app_deploy/README.md
[12]: ../api/README.md
