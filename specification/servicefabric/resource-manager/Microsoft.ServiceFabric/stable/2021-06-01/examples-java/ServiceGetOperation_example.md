Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-servicefabric_1.0.0-beta.2/sdk/servicefabric/azure-resourcemanager-servicefabric/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for Services Get. */
public final class Main {
    /*
     * operationId: Services_Get
     * api-version: 2021-06-01
     * x-ms-examples: Get a service
     */
    /**
     * Sample code: Get a service.
     *
     * @param manager Entry point to ServiceFabricManager.
     */
    public static void getAService(com.azure.resourcemanager.servicefabric.ServiceFabricManager manager) {
        manager.services().getWithResponse("resRg", "myCluster", "myApp", "myService", Context.NONE);
    }
}
```
