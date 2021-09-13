Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.ConfigurationIdName;

/** Samples for TenantConfiguration GetSyncState. */
public final class Main {
    /*
     * operationId: TenantConfiguration_GetSyncState
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementTenantAccessSyncState
     */
    /**
     * Sample code: ApiManagementTenantAccessSyncState.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementTenantAccessSyncState(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .tenantConfigurations()
            .getSyncStateWithResponse("rg1", "apimService1", ConfigurationIdName.CONFIGURATION, Context.NONE);
    }
}
```
