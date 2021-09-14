Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.AccessIdName;

/** Samples for TenantAccess RegenerateSecondaryKey. */
public final class Main {
    /*
     * operationId: TenantAccess_RegenerateSecondaryKey
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementTenantAccessRegenerateKey
     */
    /**
     * Sample code: ApiManagementTenantAccessRegenerateKey.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementTenantAccessRegenerateKey(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .tenantAccess()
            .regenerateSecondaryKeyWithResponse("rg1", "apimService1", AccessIdName.ACCESS, Context.NONE);
    }
}
```
