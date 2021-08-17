```java
import com.azure.core.util.Context;

/** Samples for DiskAccesses Delete. */
public final class DeleteADiskAccess {
    /*
     * operationId: DiskAccesses_Delete
     * api-version: 2020-12-01
     * x-ms-examples: Delete a disk access resource.
     */
    /**
     * Sample code: Delete a disk access resource.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void deleteADiskAccessResource(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDiskAccesses()
            .delete("myResourceGroup", "myDiskAccess", Context.NONE);
    }
}
```