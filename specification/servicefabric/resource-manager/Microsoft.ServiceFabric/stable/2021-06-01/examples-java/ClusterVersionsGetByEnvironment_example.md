Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-servicefabric_1.0.0-beta.2/sdk/servicefabric/azure-resourcemanager-servicefabric/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.servicefabric.models.ClusterVersionsEnvironment;

/** Samples for ClusterVersions GetByEnvironment. */
public final class Main {
    /*
     * operationId: ClusterVersions_GetByEnvironment
     * api-version: 2021-06-01
     * x-ms-examples: Get cluster version by environment
     */
    /**
     * Sample code: Get cluster version by environment.
     *
     * @param manager Entry point to ServiceFabricManager.
     */
    public static void getClusterVersionByEnvironment(
        com.azure.resourcemanager.servicefabric.ServiceFabricManager manager) {
        manager
            .clusterVersions()
            .getByEnvironmentWithResponse("eastus", ClusterVersionsEnvironment.WINDOWS, "6.1.480.9494", Context.NONE);
    }
}
```
