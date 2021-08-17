```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.DiskUpdate;

/** Samples for Disks Update. */
public final class UpdateAManagedDiskToChangeTier {
    /*
     * operationId: Disks_Update
     * api-version: 2020-12-01
     * x-ms-examples: Update a managed disk to change tier.
     */
    /**
     * Sample code: Update a managed disk to change tier.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void updateAManagedDiskToChangeTier(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDisks()
            .update("myResourceGroup", "myDisk", new DiskUpdate().withTier("P30"), Context.NONE);
    }
}
```