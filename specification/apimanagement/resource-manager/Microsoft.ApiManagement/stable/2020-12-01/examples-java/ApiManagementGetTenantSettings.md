Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.SettingsTypeName;

/** Samples for TenantSettings Get. */
public final class Main {
    /*
     * operationId: TenantSettings_Get
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementGetTenantSettings
     */
    /**
     * Sample code: ApiManagementGetTenantSettings.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementGetTenantSettings(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.tenantSettings().getWithResponse("rg1", "apimService1", SettingsTypeName.PUBLIC, Context.NONE);
    }
}
```
