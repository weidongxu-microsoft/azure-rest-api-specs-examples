Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.ConfigurationIdName;
import com.azure.resourcemanager.apimanagement.models.SaveConfigurationParameter;

/** Samples for TenantConfiguration Save. */
public final class Main {
    /*
     * operationId: TenantConfiguration_Save
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementTenantConfigurationSave
     */
    /**
     * Sample code: ApiManagementTenantConfigurationSave.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementTenantConfigurationSave(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .tenantConfigurations()
            .save(
                "rg1",
                "apimService1",
                ConfigurationIdName.CONFIGURATION,
                new SaveConfigurationParameter().withBranch("master"),
                Context.NONE);
    }
}
```
