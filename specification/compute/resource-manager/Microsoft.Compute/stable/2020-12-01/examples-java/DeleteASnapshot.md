```java
import com.azure.core.util.Context;

/** Samples for Snapshots Delete. */
public final class DeleteASnapshot {
    /*
     * operationId: Snapshots_Delete
     * api-version: 2020-12-01
     * x-ms-examples: Delete a snapshot.
     */
    /**
     * Sample code: Delete a snapshot.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void deleteASnapshot(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getSnapshots()
            .delete("myResourceGroup", "mySnapshot", Context.NONE);
    }
}
```