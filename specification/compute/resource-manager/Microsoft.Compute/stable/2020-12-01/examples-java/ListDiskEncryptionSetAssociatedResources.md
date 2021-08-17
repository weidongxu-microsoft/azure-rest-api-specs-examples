```java
import com.azure.core.util.Context;

/** Samples for DiskEncryptionSets ListAssociatedResources. */
public final
class ListDiskEncryptionSetAssociatedResources {
    /*
     * operationId: DiskEncryptionSets_ListAssociatedResources
     * api-version: 2020-12-01
     * x-ms-examples: List all resources that are encrypted with this disk encryption set.
     */
    /**
     * Sample code: List all resources that are encrypted with this disk encryption set.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listAllResourcesThatAreEncryptedWithThisDiskEncryptionSet(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDiskEncryptionSets()
            .listAssociatedResources("myResourceGroup", "myDiskEncryptionSet", Context.NONE);
    }
}
```