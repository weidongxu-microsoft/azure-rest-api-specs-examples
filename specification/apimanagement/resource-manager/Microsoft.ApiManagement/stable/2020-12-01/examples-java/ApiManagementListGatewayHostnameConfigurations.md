Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for GatewayHostnameConfiguration ListByService. */
public final class Main {
    /*
     * operationId: GatewayHostnameConfiguration_ListByService
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListGatewayHostnameConfigurations
     */
    /**
     * Sample code: ApiManagementListGatewayHostnameConfigurations.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListGatewayHostnameConfigurations(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .gatewayHostnameConfigurations()
            .listByService("rg1", "apimService1", "gw1", null, null, null, Context.NONE);
    }
}
```
