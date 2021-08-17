```java
import com.azure.core.util.Context;

/** Samples for DiskEncryptionSets GetByResourceGroup. */
public final class GetInformationAboutADiskEncryptionSet {
    /*
     * operationId: DiskEncryptionSets_Get
     * api-version: 2020-12-01
     * x-ms-examples: Get information about a disk encryption set.
     */
    /**
     * Sample code: Get information about a disk encryption set.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getInformationAboutADiskEncryptionSet(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDiskEncryptionSets()
            .getByResourceGroupWithResponse("myResourceGroup", "myDiskEncryptionSet", Context.NONE);
    }
}
```