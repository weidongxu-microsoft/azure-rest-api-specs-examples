```java
import com.azure.core.util.Context;

/** Samples for Snapshots RevokeAccess. */
public final class EndGetAccessSnapshot {
    /*
     * operationId: Snapshots_RevokeAccess
     * api-version: 2020-12-01
     * x-ms-examples: Revoke access to a snapshot.
     */
    /**
     * Sample code: Revoke access to a snapshot.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void revokeAccessToASnapshot(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getSnapshots()
            .revokeAccess("myResourceGroup", "mySnapshot", Context.NONE);
    }
}
```