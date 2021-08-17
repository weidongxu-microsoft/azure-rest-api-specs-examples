```java
import com.azure.core.util.Context;

/** Samples for Disks ListByResourceGroup. */
public final class ListManagedDisksInAResourceGroup {
    /*
     * operationId: Disks_ListByResourceGroup
     * api-version: 2020-12-01
     * x-ms-examples: List all managed disks in a resource group.
     */
    /**
     * Sample code: List all managed disks in a resource group.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listAllManagedDisksInAResourceGroup(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDisks()
            .listByResourceGroup("myResourceGroup", Context.NONE);
    }
}
```