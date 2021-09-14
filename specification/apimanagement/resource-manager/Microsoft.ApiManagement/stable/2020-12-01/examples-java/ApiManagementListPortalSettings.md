Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for PortalSettings ListByService. */
public final class Main {
    /*
     * operationId: PortalSettings_ListByService
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListPortalSettings
     */
    /**
     * Sample code: ApiManagementListPortalSettings.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListPortalSettings(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.portalSettings().listByServiceWithResponse("rg1", "apimService1", Context.NONE);
    }
}
```
