# 🔐 Managing Secrets Securely in Azure DevOps Pipelines

Azure DevOps provides multiple secure methods to manage secrets (like passwords, API keys, tokens, certificates) in your CI/CD pipelines. 

---

## Example 

### Pipeline YAML

[Azure Pipeline](/04_manage_secret_ado_pipeline/azure-pipeline.yml)


Below are the supported approaches to handle secrets **securely**.


## 🔑 Using Azure DevOps Pipeline Secrets/Variables
Pipeline Variables (UI or YAML)
You can define variables and mark them as secret in the UI.
These are encrypted and masked in logs by default.

To set secrets via the UI:

Go to Pipelines > Library > Variable Groups

Add variables and check "Keep this value secret"


## 🔑 Using Variable Groups

1. Go to your Azure DevOps project.
2. Navigate to: `Pipelines > Library`.
3. Click **"Add Variable Group"**.
4. Give the group a name (e.g., `MySecretsGroup`).
5. Add variables:
    - Enter key-value pairs.
    - Check **"Keep this value secret"** for sensitive data.
6. (Optional) Link secrets from **Azure Key Vault**.
7. Click **Save**.
8. Use the variable group in the yaml pipeline


## 🛡️ Using Azure Key Vault Integration

Azure DevOps supports native integration with Azure Key Vault for secure and centralized secret management.

1. Create a Key Vault in Azure.
2. Add secrets to it.
3. Grant Azure DevOps access (via Service Principal).
4. Link Key Vault via a Variable Group in DevOps.
