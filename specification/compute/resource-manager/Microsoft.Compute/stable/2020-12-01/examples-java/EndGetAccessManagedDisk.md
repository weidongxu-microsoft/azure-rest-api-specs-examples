```java
import com.azure.core.util.Context;

/** Samples for Disks RevokeAccess. */
public final class EndGetAccessManagedDisk {
    /*
     * operationId: Disks_RevokeAccess
     * api-version: 2020-12-01
     * x-ms-examples: Revoke access to a managed disk.
     */
    /**
     * Sample code: Revoke access to a managed disk.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void revokeAccessToAManagedDisk(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDisks()
            .revokeAccess("myResourceGroup", "myDisk", Context.NONE);
    }
}
```