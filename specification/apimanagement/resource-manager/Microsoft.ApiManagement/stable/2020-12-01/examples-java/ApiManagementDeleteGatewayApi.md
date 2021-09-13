Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for GatewayApi Delete. */
public final class Main {
    /*
     * operationId: GatewayApi_Delete
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementDeleteGatewayApi
     */
    /**
     * Sample code: ApiManagementDeleteGatewayApi.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementDeleteGatewayApi(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.gatewayApis().deleteWithResponse("rg1", "apimService1", "gw1", "echo-api", Context.NONE);
    }
}
```
