Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.AccessIdName;

/** Samples for TenantAccess Get. */
public final class Main {
    /*
     * operationId: TenantAccess_Get
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementGetTenantGitAccess
     */
    /**
     * Sample code: ApiManagementGetTenantGitAccess.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementGetTenantGitAccess(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.tenantAccess().getWithResponse("rg1", "apimService1", AccessIdName.GIT_ACCESS, Context.NONE);
    }
}
```
