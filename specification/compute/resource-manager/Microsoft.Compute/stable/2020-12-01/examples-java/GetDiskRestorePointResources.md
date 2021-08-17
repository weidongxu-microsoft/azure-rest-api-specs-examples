```java
import com.azure.core.util.Context;

/** Samples for DiskRestorePoint Get. */
public final class GetDiskRestorePointResources {
    /*
     * operationId: DiskRestorePoint_Get
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
            .getWithResponse(
                "myResourceGroup",
                "rpc",
                "vmrp",
                "TestDisk45ceb03433006d1baee0_b70cd924-3362-4a80-93c2-9415eaa12745",
                Context.NONE);
    }
}
```