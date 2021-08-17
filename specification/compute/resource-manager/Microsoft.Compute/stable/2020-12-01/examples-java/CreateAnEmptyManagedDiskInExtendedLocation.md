```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.fluent.models.DiskInner;
import com.azure.resourcemanager.compute.models.CreationData;
import com.azure.resourcemanager.compute.models.DiskCreateOption;
import com.azure.resourcemanager.compute.models.ExtendedLocation;
import com.azure.resourcemanager.compute.models.ExtendedLocationTypes;

/** Samples for Disks CreateOrUpdate. */
public final class CreateAnEmptyManagedDiskInExtendedLocation {
    /*
     * operationId: Disks_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: Create an empty managed disk in extended location.
     */
    /**
     * Sample code: Create an empty managed disk in extended location.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createAnEmptyManagedDiskInExtendedLocation(
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
                    .withExtendedLocation(
                        new ExtendedLocation().withName("{edge-zone-id}").withType(ExtendedLocationTypes.EDGE_ZONE))
                    .withCreationData(new CreationData().withCreateOption(DiskCreateOption.EMPTY))
                    .withDiskSizeGB(200),
                Context.NONE);
    }
}
```