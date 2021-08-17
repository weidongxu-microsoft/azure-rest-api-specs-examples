```java
import com.azure.core.util.Context;

/** Samples for DiskEncryptionSets Delete. */
public final class DeleteADiskEncryptionSet {
    /*
     * operationId: DiskEncryptionSets_Delete
     * api-version: 2020-12-01
     * x-ms-examples: Delete a disk encryption set.
     */
    /**
     * Sample code: Delete a disk encryption set.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void deleteADiskEncryptionSet(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDiskEncryptionSets()
            .delete("myResourceGroup", "myDiskEncryptionSet", Context.NONE);
    }
}
```