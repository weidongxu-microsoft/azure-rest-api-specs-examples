```java
import com.azure.core.util.Context;

/** Samples for DiskAccesses ListByResourceGroup. */
public final class ListDiskAccessesInAResourceGroup {
    /*
     * operationId: DiskAccesses_ListByResourceGroup
     * api-version: 2020-12-01
     * x-ms-examples: List all disk access resources in a resource group.
     */
    /**
     * Sample code: List all disk access resources in a resource group.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listAllDiskAccessResourcesInAResourceGroup(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDiskAccesses()
            .listByResourceGroup("myResourceGroup", Context.NONE);
    }
}
```