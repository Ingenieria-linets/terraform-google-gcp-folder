# Google Cloud Platform folder Terraform module

This terraform module provisions a Google Cloud Platform folder

## Usage

```hcl
module "gcp_folder" {
  source  = "nephosolutions/gcp-folder/google"
  version = "~> 1.0.0"
}
```

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| display\_name | The folder's display name. A folder's display name must be unique amongst its siblings, e.g. no two folders with the same parent can share the same display name. The display name must start and end with a letter or digit, may contain letters, digits, spaces, hyphens and underscores and can be no longer than 30 characters. | string | n/a | yes |
| iam\_bindings | Updates the IAM policy to grant a role to a list of members. Authoritative for a given role. Other roles within the IAM policy for the folder are preserved. | map(list(string)) | `{}` | no |
| parent | The resource name of the parent Folder or Organization. Must be of the form `folders/{folder_id}` or `organizations/{org_id}`. | string | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| name | The resource name of the Folder. Its format is `folders/{folder_id}`. |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
