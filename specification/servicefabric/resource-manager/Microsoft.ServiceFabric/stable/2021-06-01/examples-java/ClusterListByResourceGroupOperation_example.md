Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-servicefabric_1.0.0-beta.2/sdk/servicefabric/azure-resourcemanager-servicefabric/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Clusters ListByResourceGroup. */
public final class Main {
    /*
     * operationId: Clusters_ListByResourceGroup
     * api-version: 2021-06-01
     * x-ms-examples: List cluster by resource group
     */
    /**
     * Sample code: List cluster by resource group.
     *
     * @param manager Entry point to ServiceFabricManager.
     */
    public static void listClusterByResourceGroup(
        com.azure.resourcemanager.servicefabric.ServiceFabricManager manager) {
        manager.clusters().listByResourceGroupWithResponse("resRg", Context.NONE);
    }
}
```
