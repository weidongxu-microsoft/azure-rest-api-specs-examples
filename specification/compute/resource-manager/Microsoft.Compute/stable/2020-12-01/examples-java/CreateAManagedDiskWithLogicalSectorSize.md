```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.fluent.models.DiskInner;
import com.azure.resourcemanager.compute.models.CreationData;
import com.azure.resourcemanager.compute.models.DiskCreateOption;
import com.azure.resourcemanager.compute.models.DiskSku;
import com.azure.resourcemanager.compute.models.DiskStorageAccountTypes;

/** Samples for Disks CreateOrUpdate. */
public final class CreateAManagedDiskWithLogicalSectorSize {
    /*
     * operationId: Disks_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: Create an ultra managed disk with logicalSectorSize 512E
     */
    /**
     * Sample code: Create an ultra managed disk with logicalSectorSize 512E.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createAnUltraManagedDiskWithLogicalSectorSize512E(
        com.azure.resourcemanager.AzureResourceManager azure) {
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
                    .withSku(new DiskSku().withName(DiskStorageAccountTypes.ULTRA_SSD_LRS))
                    .withCreationData(
                        new CreationData().withCreateOption(DiskCreateOption.EMPTY).withLogicalSectorSize(512))
                    .withDiskSizeGB(200),
                Context.NONE);
    }
}
```