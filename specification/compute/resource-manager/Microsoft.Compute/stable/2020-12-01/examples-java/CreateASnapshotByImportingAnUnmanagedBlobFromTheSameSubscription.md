```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.fluent.models.SnapshotInner;
import com.azure.resourcemanager.compute.models.CreationData;
import com.azure.resourcemanager.compute.models.DiskCreateOption;

/** Samples for Snapshots CreateOrUpdate. */
public final class CreateASnapshotByImportingAnUnmanagedBlobFromTheSameSubscription {
    /*
     * operationId: Snapshots_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: Create a snapshot by importing an unmanaged blob from the same subscription.
     */
    /**
     * Sample code: Create a snapshot by importing an unmanaged blob from the same subscription.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createASnapshotByImportingAnUnmanagedBlobFromTheSameSubscription(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getSnapshots()
            .createOrUpdate(
                "myResourceGroup",
                "mySnapshot1",
                new SnapshotInner()
                    .withLocation("West US")
                    .withCreationData(
                        new CreationData()
                            .withCreateOption(DiskCreateOption.IMPORT)
                            .withSourceUri("https://mystorageaccount.blob.core.windows.net/osimages/osimage.vhd")),
                Context.NONE);
    }
}
```