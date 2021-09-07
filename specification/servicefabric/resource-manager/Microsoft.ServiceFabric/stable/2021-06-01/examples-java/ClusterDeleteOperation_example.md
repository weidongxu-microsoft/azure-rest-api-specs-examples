Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-servicefabric_1.0.0-beta.2/sdk/servicefabric/azure-resourcemanager-servicefabric/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for Clusters Delete. */
public final class Main {
    /*
     * operationId: Clusters_Delete
     * api-version: 2021-06-01
     * x-ms-examples: Delete a cluster
     */
    /**
     * Sample code: Delete a cluster.
     *
     * @param manager Entry point to ServiceFabricManager.
     */
    public static void deleteACluster(com.azure.resourcemanager.servicefabric.ServiceFabricManager manager) {
        manager.clusters().deleteWithResponse("resRg", "myCluster", Context.NONE);
    }
}
```
