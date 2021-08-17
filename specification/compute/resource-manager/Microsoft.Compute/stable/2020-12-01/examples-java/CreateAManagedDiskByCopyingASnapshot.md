```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.fluent.models.DiskInner;
import com.azure.resourcemanager.compute.models.CreationData;
import com.azure.resourcemanager.compute.models.DiskCreateOption;

/** Samples for Disks CreateOrUpdate. */
public final class CreateAManagedDiskByCopyingASnapshot {
    /*
     * operationId: Disks_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: Create a managed disk by copying a snapshot.
     */
    /**
     * Sample code: Create a managed disk by copying a snapshot.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createAManagedDiskByCopyingASnapshot(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDisks()
            .createOrUpdate(
                "myResourceGroup",
                "myDisk",
                new DiskInner()
                    .withLocation("West US")
                    .withCreationData(
                        new CreationData()
                            .withCreateOption(DiskCreateOption.COPY)
                            .withSourceResourceId(
                                "subscriptions/{subscriptionId}/resourceGroups/myResourceGroup/providers/Microsoft.Compute/snapshots/mySnapshot")),
                Context.NONE);
    }
}
```