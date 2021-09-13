Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Gateway Get. */
public final class Main {
    /*
     * operationId: Gateway_Get
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementGetGateway
     */
    /**
     * Sample code: ApiManagementGetGateway.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementGetGateway(com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.gateways().getWithResponse("rg1", "apimService1", "gw1", Context.NONE);
    }
}
```
