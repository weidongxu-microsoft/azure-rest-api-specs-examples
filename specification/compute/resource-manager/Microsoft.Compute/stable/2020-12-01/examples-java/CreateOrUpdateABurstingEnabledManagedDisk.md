```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.DiskUpdate;

/** Samples for Disks Update. */
public final class CreateOrUpdateABurstingEnabledManagedDisk {
    /*
     * operationId: Disks_Update
     * api-version: 2020-12-01
     * x-ms-examples: Create or update a bursting enabled managed disk.
     */
    /**
     * Sample code: Create or update a bursting enabled managed disk.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createOrUpdateABurstingEnabledManagedDisk(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDisks()
            .update(
                "myResourceGroup",
                "myDisk",
                new DiskUpdate().withDiskSizeGB(1024).withBurstingEnabled(true),
                Context.NONE);
    }
}
```