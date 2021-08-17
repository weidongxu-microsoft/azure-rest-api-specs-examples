```java
import com.azure.core.util.Context;

/** Samples for DiskRestorePoint RevokeAccess. */
public final class EndGetAccessDiskRestorePoint {
    /*
     * operationId: DiskRestorePoint_RevokeAccess
     * api-version: 2020-12-01
     * x-ms-examples: Revokes access to a diskRestorePoint.
     */
    /**
     * Sample code: Revokes access to a diskRestorePoint.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void revokesAccessToADiskRestorePoint(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDiskRestorePoints()
            .revokeAccess(
                "myResourceGroup",
                "rpc",
                "vmrp",
                "TestDisk45ceb03433006d1baee0_b70cd924-3362-4a80-93c2-9415eaa12745",
                Context.NONE);
    }
}
```