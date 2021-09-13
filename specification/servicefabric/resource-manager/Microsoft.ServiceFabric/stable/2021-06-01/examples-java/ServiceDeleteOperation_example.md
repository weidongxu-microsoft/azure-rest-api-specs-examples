Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-servicefabric_1.0.0-beta.2/sdk/servicefabric/azure-resourcemanager-servicefabric/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Services Delete. */
public final class Main {
    /*
     * operationId: Services_Delete
     * api-version: 2021-06-01
     * x-ms-examples: Delete a service
     */
    /**
     * Sample code: Delete a service.
     *
     * @param manager Entry point to ServiceFabricManager.
     */
    public static void deleteAService(com.azure.resourcemanager.servicefabric.ServiceFabricManager manager) {
        manager.services().delete("resRg", "myCluster", "myApp", "myService", Context.NONE);
    }
}
```
