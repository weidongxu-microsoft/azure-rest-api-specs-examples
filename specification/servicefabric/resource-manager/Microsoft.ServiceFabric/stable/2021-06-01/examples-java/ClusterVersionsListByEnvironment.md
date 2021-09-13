Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-servicefabric_1.0.0-beta.2/sdk/servicefabric/azure-resourcemanager-servicefabric/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.servicefabric.models.ClusterVersionsEnvironment;

/** Samples for ClusterVersions ListByEnvironment. */
public final class Main {
    /*
     * operationId: ClusterVersions_ListByEnvironment
     * api-version: 2021-06-01
     * x-ms-examples: List cluster versions by environment
     */
    /**
     * Sample code: List cluster versions by environment.
     *
     * @param manager Entry point to ServiceFabricManager.
     */
    public static void listClusterVersionsByEnvironment(
        com.azure.resourcemanager.servicefabric.ServiceFabricManager manager) {
        manager
            .clusterVersions()
            .listByEnvironmentWithResponse("eastus", ClusterVersionsEnvironment.WINDOWS, Context.NONE);
    }
}
```
