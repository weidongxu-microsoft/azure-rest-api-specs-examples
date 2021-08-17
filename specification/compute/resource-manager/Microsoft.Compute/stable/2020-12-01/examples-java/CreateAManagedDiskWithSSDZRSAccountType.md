```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.fluent.models.DiskInner;
import com.azure.resourcemanager.compute.models.CreationData;
import com.azure.resourcemanager.compute.models.DiskCreateOption;
import com.azure.resourcemanager.compute.models.DiskSku;
import com.azure.resourcemanager.compute.models.DiskStorageAccountTypes;

/** Samples for Disks CreateOrUpdate. */
public final class CreateAManagedDiskWithSSDZRSAccountType {
    /*
     * operationId: Disks_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: Create a managed disk with ssd zrs account type.
     */
    /**
     * Sample code: Create a managed disk with ssd zrs account type.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createAManagedDiskWithSsdZrsAccountType(com.azure.resourcemanager.AzureResourceManager azure) {
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
                    .withSku(new DiskSku().withName(DiskStorageAccountTypes.PREMIUM_ZRS))
                    .withCreationData(new CreationData().withCreateOption(DiskCreateOption.EMPTY))
                    .withDiskSizeGB(200),
                Context.NONE);
    }
}
```