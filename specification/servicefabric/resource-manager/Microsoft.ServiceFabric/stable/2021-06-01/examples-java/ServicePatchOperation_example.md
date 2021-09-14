Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-servicefabric_1.0.0-beta.2/sdk/servicefabric/azure-resourcemanager-servicefabric/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.servicefabric.models.ServiceResource;

/** Samples for Services Update. */
public final class Main {
    /*
     * operationId: Services_Update
     * api-version: 2021-06-01
     * x-ms-examples: Patch a service
     */
    /**
     * Sample code: Patch a service.
     *
     * @param manager Entry point to ServiceFabricManager.
     */
    public static void patchAService(com.azure.resourcemanager.servicefabric.ServiceFabricManager manager) {
        ServiceResource resource =
            manager.services().getWithResponse("resRg", "myCluster", "myApp", "myService", Context.NONE).getValue();
        resource.update().apply();
    }
}
```
