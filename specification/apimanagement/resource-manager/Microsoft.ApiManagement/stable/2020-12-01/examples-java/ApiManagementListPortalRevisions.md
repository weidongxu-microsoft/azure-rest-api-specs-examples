Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for PortalRevision ListByService. */
public final class Main {
    /*
     * operationId: PortalRevision_ListByService
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListPortalRevisions
     */
    /**
     * Sample code: ApiManagementListPortalRevisions.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListPortalRevisions(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.portalRevisions().listByService("rg1", "apimService1", null, null, null, Context.NONE);
    }
}
```
