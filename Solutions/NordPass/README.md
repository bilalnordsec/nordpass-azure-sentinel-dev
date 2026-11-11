## Automated Installation

Installing the NordPass Solution for Microsoft Sentinel is easy and can be completed in only a few minutes. 
Just click the button below to get started with the deployment wizard. <br>

[![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fbilalnordsec%2Fnordpass-azure-sentinel-dev%2Frefs%2Fheads%2Fstaging%2FSolutions%2FNordPass%2FData%2520Connectors%2Fazuredeploy_NordPass_API_FunctionApp.json)

> NOTE: To deploy the solution, the Azure user account executing the deployment needs to have `Owner` permissions on the Microsoft Sentinel `Resource Group` in Azure.<br>
> This is required to assign the correct RBAC role to the managed identity of the FunctionApp!

---

## Step 2 — Content (TEST BUILDS ONLY)

**This step does not exist for customers.** Real deployments receive the analytic rules and parser
through **Content Hub**, once the package is published via Partner Center. This button
exists only because the 3.1.0 package has not been published yet, so there is nothing in Content Hub
to install.

Deploy into the **same workspace** used above:

[![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fbilalnordsec%2Fnordpass-azure-sentinel-dev%2Frefs%2Fheads%2Fstaging%2FSolutions%2FNordPass%2FPackage%2FmainTemplate.json)

Installs 9 analytic rule templates and the `NordPassActivities` parser (version 3.1.0).
The workbook is no longer part of the solution — it only ever supported Activity Log v1.

> NOTE: Analytic rules install as **templates**. Nothing fires until a rule is created from one:
> Microsoft Sentinel → Analytics → Rule templates → select → Create rule.
  

