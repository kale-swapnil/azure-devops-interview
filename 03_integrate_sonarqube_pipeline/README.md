# How do you integrate SonarQube and security scans into your Azure DevOps pipeline??

SonarQube is used to perform **static code analysis** and maintain **code quality**. The integration is done via the Azure DevOps pipeline using the **SonarQube Azure DevOps extension**.

## 📌 Prerequisites

Before running the pipeline with SonarQube, ensure the following are set up:

1. **SonarQube Server** (self-hosted or SonarCloud).
2. **SonarQube Project** created with a unique key.
3. **Azure DevOps Service Connection** to SonarQube:
   - Go to: `Project Settings > Service connections > New service connection > SonarQube`.
4. **SonarQube Extension** installed in Azure DevOps from the Azure DevOps Marketplace.



## ⚙️ Pipeline Integration

The Azure DevOps pipeline performs the following SonarQube-related steps:

1. **Prepare Analysis Configuration** (`SonarCloudPrepare@3`)
2. **Build the project** (using MSBuild or .NET Core CLI)
3. **Run Tests** (optional: with code coverage)
4. **Run SonarQube Analysis** (`SonarCloudAnalyze@3`)
5. **Publish Results to SonarQube** (`SonarCloudPublish@3`)


## Example 

### Pipeline YAML

[Azure Pipeline](/03_integrate_sonarqube_pipeline/azure-pipeline.yml)



## ✅ Benefits of SonarQube

- Detects bugs, vulnerabilities, and code smells early in CI.
- Enforces quality gates to prevent merging low-quality code.
- Supports various languages: C#, Java, JavaScript, TypeScript, etc.
- Visual reports on technical debt and test coverage.