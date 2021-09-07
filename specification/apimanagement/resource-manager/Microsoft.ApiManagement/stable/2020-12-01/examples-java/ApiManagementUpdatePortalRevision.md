Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.PortalRevisionContract;

/** Samples for PortalRevision Update. */
public final class Main {
    /*
     * operationId: PortalRevision_Update
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementUpdatePortalRevision
     */
    /**
     * Sample code: ApiManagementUpdatePortalRevision.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementUpdatePortalRevision(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        PortalRevisionContract resource =
            manager.portalRevisions().getWithResponse("rg1", "apimService1", "20201112101010", Context.NONE).getValue();
        resource.update().withDescription("portal revision update").withIsCurrent(true).withIfMatch("*").apply();
    }
}
```
