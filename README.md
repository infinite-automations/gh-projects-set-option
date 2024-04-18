# gh-projects-set-select-option

[![Test & Release](https://github.com/infinite-automations/gh-projects-set-select-option/actions/workflows/test-release.yml/badge.svg?branch=main)](https://github.com/infinite-automations/gh-projects-set-select-option/actions/workflows/test-release.yml)

Sets the value for a select field in GitHub Projects based on the text value.

# Usage

```yaml
- uses: infinite-automations/gh-projects-set-option@v1.0.0
  with:
    # Token which is used to access the project data via GitHub CLI
    token: ''
    # Number of the project. Value is integer and can be found in the url of the project view. Example url: https://github.com/orgs/infinite-automations/projects/1/settings
    project-number: ''
    # owner of the project
    # Normally a organization
    project-owner: ''
    # Name of the field to get the id from.
    # Camel Case is important!
    field-name: ''
    # Name of the selection option to get the id from.
    # Camel Case is important!
    select-option-name: ''
    # Technical Id for the item to perform the update
    item-id: ''
```

# Inputs

| Key                | Description                                                                  | Type    | Required |
| ------------------ | ---------------------------------------------------------------------------- | ------- | -------- |
| token              | Token to access the project via API                                          | String  | Yes      |
| project-number     | Number of the project                                                        | Integer | Yes      |
| project-owner      | The owner of the project. This is normally an organization.                  | String  | Yes      |
| item-id            | The Id of the item which should be edited.                                   | Integer | Yes      |
| field-name         | The name of the select field.                                                | String  | False    |
| select-option-name | The Name for the option of the select field. It has to be an existing value. | String  | False    |

# License

The scripts and documentation in this project are released under the MIT License.
