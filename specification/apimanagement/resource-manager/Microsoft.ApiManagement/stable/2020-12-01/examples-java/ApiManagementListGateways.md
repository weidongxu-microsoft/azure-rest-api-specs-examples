Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for Gateway ListByService. */
public final class Main {
    /*
     * operationId: Gateway_ListByService
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListGateways
     */
    /**
     * Sample code: ApiManagementListGateways.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListGateways(com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.gateways().listByService("rg1", "apimService1", null, null, null, Context.NONE);
    }
}
```
