Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.resourcemanager.apimanagement.models.AccessIdName;

/** Samples for TenantAccess Create. */
public final class Main {
    /*
     * operationId: TenantAccess_Create
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateTenantAccess
     */
    /**
     * Sample code: ApiManagementCreateTenantAccess.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateTenantAccess(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .tenantAccess()
            .define(AccessIdName.ACCESS)
            .withExistingService("rg1", "apimService1")
            .withEnabled(true)
            .withIfMatch("*")
            .create();
    }
}
```
