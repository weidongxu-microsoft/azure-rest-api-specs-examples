Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for DelegationSettings Get. */
public final class Main {
    /*
     * operationId: DelegationSettings_Get
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementPortalSettingsGetDelegation
     */
    /**
     * Sample code: ApiManagementPortalSettingsGetDelegation.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementPortalSettingsGetDelegation(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.delegationSettings().getWithResponse("rg1", "apimService1", Context.NONE);
    }
}
```
