Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-servicefabric_1.0.0-beta.2/sdk/servicefabric/azure-resourcemanager-servicefabric/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for ClusterVersions Get. */
public final class Main {
    /*
     * operationId: ClusterVersions_Get
     * api-version: 2021-06-01
     * x-ms-examples: Get cluster version
     */
    /**
     * Sample code: Get cluster version.
     *
     * @param manager Entry point to ServiceFabricManager.
     */
    public static void getClusterVersion(com.azure.resourcemanager.servicefabric.ServiceFabricManager manager) {
        manager.clusterVersions().getWithResponse("eastus", "6.1.480.9494", Context.NONE);
    }
}
```
