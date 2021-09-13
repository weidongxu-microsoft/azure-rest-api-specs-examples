Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.GatewayContract;
import com.azure.resourcemanager.apimanagement.models.ResourceLocationDataContract;

/** Samples for Gateway Update. */
public final class Main {
    /*
     * operationId: Gateway_Update
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementUpdateGateway
     */
    /**
     * Sample code: ApiManagementUpdateGateway.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementUpdateGateway(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        GatewayContract resource =
            manager.gateways().getWithResponse("rg1", "apimService1", "gw1", Context.NONE).getValue();
        resource
            .update()
            .withLocationData(new ResourceLocationDataContract().withName("my location"))
            .withDescription("my gateway 1")
            .withIfMatch("*")
            .apply();
    }
}
```
