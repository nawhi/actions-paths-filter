# Github Actions Monorepo Setup with Paths Filter

This is a very basic example of setting up Github Actions to handle a monorepo setup. 

If you have a lot of packages in your monorepo, but you rarely work on them all at the same time, you don't want GitHub to spend lots of time unnecessarily building code that you haven't changed. Thankfully, the `paths` and `paths-ignore` key in the workflow spec can be configured to help.

When the `client` module is edited, then only the `client` CI will run.
When the `server` module is edited, then `server` will run.
When the `common` module is edited then both pipelines will run.


For more information see https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions#onpushpull_requestpull_request_targetpathspaths-ignore
