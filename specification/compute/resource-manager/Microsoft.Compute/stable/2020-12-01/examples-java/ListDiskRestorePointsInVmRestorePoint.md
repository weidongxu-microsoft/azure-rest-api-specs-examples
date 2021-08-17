```java
import com.azure.core.util.Context;

/** Samples for DiskRestorePoint ListByRestorePoint. */
public final class ListDiskRestorePointsInVmRestorePoint {
    /*
     * operationId: DiskRestorePoint_ListByRestorePoint
     * api-version: 2020-12-01
     * x-ms-examples: Get an incremental disk restorePoint resource.
     */
    /**
     * Sample code: Get an incremental disk restorePoint resource.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getAnIncrementalDiskRestorePointResource(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDiskRestorePoints()
            .listByRestorePoint("myResourceGroup", "rpc", "vmrp", Context.NONE);
    }
}
```