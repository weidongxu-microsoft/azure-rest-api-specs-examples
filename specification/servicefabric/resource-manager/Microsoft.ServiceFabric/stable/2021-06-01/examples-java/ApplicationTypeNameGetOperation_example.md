Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-servicefabric_1.0.0-beta.2/sdk/servicefabric/azure-resourcemanager-servicefabric/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for ApplicationTypes Get. */
public final class Main {
    /*
     * operationId: ApplicationTypes_Get
     * api-version: 2021-06-01
     * x-ms-examples: Get an application type
     */
    /**
     * Sample code: Get an application type.
     *
     * @param manager Entry point to ServiceFabricManager.
     */
    public static void getAnApplicationType(com.azure.resourcemanager.servicefabric.ServiceFabricManager manager) {
        manager.applicationTypes().getWithResponse("resRg", "myCluster", "myAppType", Context.NONE);
    }
}
```
