# Setup Terraform

Installs [Terraform](https://www.terraform.io) for use in [Buildkite](https://buildkite.com) builds.

## Example

```yaml
steps:
- name: Terraform plan
  plugins:
  - sj26/setup-terraform
  command: |
    terraform init
    terraform plan
```

## Select terraform version to install

By default, the latest released version of terraform will be installed.

You can select a version with the version parameter:

```yaml
steps:
- plugins:
  - sj26/setup-terraform:
      version: 0.12.31
  command: terraform version
```
