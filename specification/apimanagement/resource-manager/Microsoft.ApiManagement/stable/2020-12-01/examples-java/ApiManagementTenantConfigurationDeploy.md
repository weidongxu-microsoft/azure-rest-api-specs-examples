Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.ConfigurationIdName;
import com.azure.resourcemanager.apimanagement.models.DeployConfigurationParameters;

/** Samples for TenantConfiguration Deploy. */
public final class Main {
    /*
     * operationId: TenantConfiguration_Deploy
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementTenantConfigurationDeploy
     */
    /**
     * Sample code: ApiManagementTenantConfigurationDeploy.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementTenantConfigurationDeploy(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .tenantConfigurations()
            .deploy(
                "rg1",
                "apimService1",
                ConfigurationIdName.CONFIGURATION,
                new DeployConfigurationParameters().withBranch("master"),
                Context.NONE);
    }
}
```
