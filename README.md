# .github Repository Documentation

## Overview

This repository contains the community health files used at Mole Street. Currently, it hosts our default Pull Request (PR) template, making it automatically accessible across all internal Mole Street projects.

Centralizing updates to the default PR template in this repository ensures consistency and eliminates the need to maintain duplicate versions across multiple repositories. Updates to the default PR template can be made in one place and will propagate to all internal projects. 

For more information about GitHub's community health files, refer to the [GitHub documentation]((https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file#about-default-community-health-files). ).

## Contribution Guidelines

### Repository Visibility

This is a *public* repository, meaning it is visible to anyone on the internet. GitHub requires this public status to enable private repositories within the Mole Street Organization to access the default PR template.

⚠️ ** Do not commit sensitive information to this repository.**
Ensure no internal data, personal identifiers, client information, or project details are included in any changes.

### Making Changes

- Only **Mole Street Organization Members** are permitted to make updates to this repository
- Changes are limited to the pull_request_template.md file
All changes must:
  - Adhere to Mole Street's internal standards
  - Apply to all repositories at Mole Street
  - Be reviewed and approved by at least one other team member before merging

## Default PR Template

The `pull_request_template.md` file is applied to all pull requests within the Mole Street Organization. This ensures a consistent workflow and helps maintain quality standards.

### Requirements

- All pull requests must use this template
- Developers are required to complete the template fully and appropriately for every PR

## Code Owners

The `CODEOWNERS` file is located in this repository so that it acts as the global code owners file for the organization——meaning that it applies to all repos in the organization. The primary benefit of this is that we don't have to maintain multiple copies of this file across every repository we own.

Code owners are automatically requested for review when someone opens a pull request that modifies code that they own. Code owners are not automatically requested to review draft pull requests.

GitHub CODEOWNERS documentation can be found (here)[https://help.github.com/articles/about-codeowners/]

### Who Owns What

Ownership is determined by file path matching:
- Front end developers are assigned to review changes made to all `/frontend ` directories
- Back end developers are assigned to review changes made to all `/backend ` directories
- All developers are assigned to review changes that do not match the file patterns above. This is to ensure review coverage for older repositories that do not follow the current repo structure standard (e.g., the monorepo-template structure). 

### To Add New Code Owners

Code Owners should only be internal, full-time Mole Street developers. Anyone with a different role within Mole Street or outside of the organization are not eligible to be code owners. 

To add a new code owner, you'll need to add the user's GitHub handle to the `CODEOWNERS` file, following the existing pattern there. They must also have write permissions for all repositories. 

### To Remove and Existing Code Owner

Simply delete the user's GitHub handle from the `CODEOWNERS` file.

### Why Do We Have Code Owners? 

As part of our SOC2 compliance efforts, we need to ensure that code changes merged into the main branch of our repositories must be reviewed by someone other than the person committing the change. The code owners file + the corresponding GitHub settings will ensure that we're meeting this requirement and it automates PR review requests for us. 