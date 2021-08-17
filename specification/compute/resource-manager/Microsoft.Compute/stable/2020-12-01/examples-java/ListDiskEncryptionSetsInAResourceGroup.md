```java
import com.azure.core.util.Context;

/** Samples for DiskEncryptionSets ListByResourceGroup. */
public final class ListDiskEncryptionSetsInAResourceGroup {
    /*
     * operationId: DiskEncryptionSets_ListByResourceGroup
     * api-version: 2020-12-01
     * x-ms-examples: List all disk encryption sets in a resource group.
     */
    /**
     * Sample code: List all disk encryption sets in a resource group.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listAllDiskEncryptionSetsInAResourceGroup(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDiskEncryptionSets()
            .listByResourceGroup("myResourceGroup", Context.NONE);
    }
}
```