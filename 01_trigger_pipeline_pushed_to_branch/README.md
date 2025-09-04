# How do you trigger a pipeline when code is pushed to a specific branch?

In Azure DevOps, a pipeline can be triggered on code push to a specific branch by configuring triggers in the pipeline YAML file (or in the classic pipeline UI).

## Example 

### Pipeline YAML

[Azure Pipeline](/trigger_pipeline_pushed_to_branch/azure-pipelines.yml)

### Classic Pipeline (UI)

1. Go to your pipeline in Azure DevOps.

2. Click Edit.

3. Click on more actions.

4. Click on Triggers.

5. Enable Continuous integration (CI).

6. Specify the branch(es) you want to trigger the pipeline on (e.g., main, dev).

