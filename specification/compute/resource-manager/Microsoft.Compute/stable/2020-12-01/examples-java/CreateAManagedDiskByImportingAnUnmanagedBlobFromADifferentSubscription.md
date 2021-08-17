```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.fluent.models.DiskInner;
import com.azure.resourcemanager.compute.models.CreationData;
import com.azure.resourcemanager.compute.models.DiskCreateOption;

/** Samples for Disks CreateOrUpdate. */
public final class CreateAManagedDiskByImportingAnUnmanagedBlobFromADifferentSubscription {
    /*
     * operationId: Disks_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: Create a managed disk by importing an unmanaged blob from a different subscription.
     */
    /**
     * Sample code: Create a managed disk by importing an unmanaged blob from a different subscription.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createAManagedDiskByImportingAnUnmanagedBlobFromADifferentSubscription(
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
                    .withCreationData(
                        new CreationData()
                            .withCreateOption(DiskCreateOption.IMPORT)
                            .withStorageAccountId(
                                "subscriptions/{subscriptionId}/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount")
                            .withSourceUri("https://mystorageaccount.blob.core.windows.net/osimages/osimage.vhd")),
                Context.NONE);
    }
}
```