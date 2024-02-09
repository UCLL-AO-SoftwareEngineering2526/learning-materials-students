# Limit the amount of ZIP files

## 1. Acceptance Criteria

Only one frontend ZIP file is retained when a new deployment is done to Azure.

## 2. Implementation Details

Every time the front-end is deployed a new ZIP archive is pushed to disk on Azure (see [this task, section 2.1](./4-build-a-cd-pipeline.md)). This will fill-up the disk over time.

You will need to tackle the growing disk usage, especially if your apps [share a free App Service Plan](<../../../../reference/cicd/azure/1 - note on app service plan.md>).

As long as your app is running you can manually clean-up the previous deploys via SSH. This is cumbersome to do.

The amount of ZIP files can be limited with the
`SCM_MAX_ZIP_PACKAGE_COUNT` environment variable,
see [Environment variables and app settings in Azure App Service](https://learn.microsoft.com/en-us/azure/app-service/reference-app-settings?tabs=kudu%2Cdotnet#deployment).
