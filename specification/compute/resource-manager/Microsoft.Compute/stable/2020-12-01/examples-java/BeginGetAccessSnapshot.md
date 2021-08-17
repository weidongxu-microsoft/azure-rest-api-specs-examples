```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.AccessLevel;
import com.azure.resourcemanager.compute.models.GrantAccessData;

/** Samples for Snapshots GrantAccess. */
public final class BeginGetAccessSnapshot {
    /*
     * operationId: Snapshots_GrantAccess
     * api-version: 2020-12-01
     * x-ms-examples: Get a sas on a snapshot.
     */
    /**
     * Sample code: Get a sas on a snapshot.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getASasOnASnapshot(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getSnapshots()
            .grantAccess(
                "myResourceGroup",
                "mySnapshot",
                new GrantAccessData().withAccess(AccessLevel.READ).withDurationInSeconds(300),
                Context.NONE);
    }
}
```