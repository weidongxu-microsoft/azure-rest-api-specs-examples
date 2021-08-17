```java
import com.azure.core.management.SubResource;
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.fluent.models.ImageInner;
import com.azure.resourcemanager.compute.models.DiskEncryptionSetParameters;
import com.azure.resourcemanager.compute.models.ImageOSDisk;
import com.azure.resourcemanager.compute.models.ImageStorageProfile;
import com.azure.resourcemanager.compute.models.OperatingSystemStateTypes;
import com.azure.resourcemanager.compute.models.OperatingSystemTypes;

/** Samples for Images CreateOrUpdate. */
public final class CreateAnImageFromASnapshotWithDiskEncryptionSet {
    /*
     * operationId: Images_CreateOrUpdate
     * api-version: 2021-04-01
     * x-ms-examples: Create a virtual machine image from a snapshot with DiskEncryptionSet resource.
     */
    /**
     * Sample code: Create a virtual machine image from a snapshot with DiskEncryptionSet resource.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createAVirtualMachineImageFromASnapshotWithDiskEncryptionSetResource(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getImages()
            .createOrUpdate(
                "myResourceGroup",
                "myImage",
                new ImageInner()
                    .withLocation("West US")
                    .withStorageProfile(
                        new ImageStorageProfile()
                            .withOsDisk(
                                new ImageOSDisk()
                                    .withSnapshot(
                                        new SubResource()
                                            .withId(
                                                "subscriptions/{subscription-id}/resourceGroups/myResourceGroup/providers/Microsoft.Compute/snapshots/mySnapshot"))
                                    .withDiskEncryptionSet(
                                        new DiskEncryptionSetParameters()
                                            .withId(
                                                "/subscriptions/{subscription-id}/resourceGroups/myResourceGroup/providers/Microsoft.Compute/diskEncryptionSets/{existing-diskEncryptionSet-name}"))
                                    .withOsType(OperatingSystemTypes.LINUX)
                                    .withOsState(OperatingSystemStateTypes.GENERALIZED))),
                Context.NONE);
    }
}
```