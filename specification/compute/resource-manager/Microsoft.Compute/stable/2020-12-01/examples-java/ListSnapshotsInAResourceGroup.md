```java
import com.azure.core.util.Context;

/** Samples for Snapshots ListByResourceGroup. */
public final class ListSnapshotsInAResourceGroup {
    /*
     * operationId: Snapshots_ListByResourceGroup
     * api-version: 2020-12-01
     * x-ms-examples: List all snapshots in a resource group.
     */
    /**
     * Sample code: List all snapshots in a resource group.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listAllSnapshotsInAResourceGroup(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getSnapshots()
            .listByResourceGroup("myResourceGroup", Context.NONE);
    }
}
```