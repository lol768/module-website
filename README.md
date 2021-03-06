# Template repository for (module) websites with Sitebuilder automation

This repository contains a template for automating Sitebuilder websites. Some configuration is required:

1. If you do not already have an external user account (required for Sitebuilder API access), create one
2. Give the external user account the required permissions on the Sitebuilder page you want to automate
3. Create two secrets named `SB_USER` and `SB_PASSWORD` in your fork of this repository with the username and password for the external user account, respectively
4. Modify `.github/workflows/sitebuilder.yml` to suit your needs (particularly, replace the value of `SB_PATH` with the path of the Sitebuilder page that you want to automate)

That is all the configuration that is required. Once completed, all commits you push to the `master` branch will run the GitHub workflow that will update the page indicated by `SB_PATH` with the contents of `content.html`. All files from the `files` directory will be uploaded as files under the `SB_PATH` page. 