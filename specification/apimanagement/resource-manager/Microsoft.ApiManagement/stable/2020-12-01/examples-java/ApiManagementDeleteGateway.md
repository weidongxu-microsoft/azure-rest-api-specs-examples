Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for Gateway Delete. */
public final class Main {
    /*
     * operationId: Gateway_Delete
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementDeleteGateway
     */
    /**
     * Sample code: ApiManagementDeleteGateway.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementDeleteGateway(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.gateways().deleteWithResponse("rg1", "apimService1", "gw1", "*", Context.NONE);
    }
}
```
