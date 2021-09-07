Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-servicefabric_1.0.0-beta.2/sdk/servicefabric/azure-resourcemanager-servicefabric/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for ClusterVersions List. */
public final class Main {
    /*
     * operationId: ClusterVersions_List
     * api-version: 2021-06-01
     * x-ms-examples: List cluster versions
     */
    /**
     * Sample code: List cluster versions.
     *
     * @param manager Entry point to ServiceFabricManager.
     */
    public static void listClusterVersions(com.azure.resourcemanager.servicefabric.ServiceFabricManager manager) {
        manager.clusterVersions().listWithResponse("eastus", Context.NONE);
    }
}
```
