```java
import com.azure.core.util.Context;

/** Samples for Disks Delete. */
public final class DeleteAManagedDisk {
    /*
     * operationId: Disks_Delete
     * api-version: 2020-12-01
     * x-ms-examples: Delete a managed disk.
     */
    /**
     * Sample code: Delete a managed disk.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void deleteAManagedDisk(com.azure.resourcemanager.AzureResourceManager azure) {
        azure.virtualMachines().manager().serviceClient().getDisks().delete("myResourceGroup", "myDisk", Context.NONE);
    }
}
```