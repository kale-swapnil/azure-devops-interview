# How do you deploy only if tests pass?

In Azure DevOps, This can be enforced in azure pipeline by using stages, jobs, and dependencies.

## Example 

### Pipeline YAML

[Azure Pipeline](/02_deploy_if_test_pass/azure-pipelines.yml)

### Classic Pipeline (UI)

1. Create a pipeline with 3 stages: Build, Test, Deploy.

2. Add a Post-job condition on the Deploy stage → set to Only run if all previous tasks succeed.




