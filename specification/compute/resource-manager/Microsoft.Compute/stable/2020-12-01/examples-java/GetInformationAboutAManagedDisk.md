```java
import com.azure.core.util.Context;

/** Samples for Disks GetByResourceGroup. */
public final class GetInformationAboutAManagedDisk {
    /*
     * operationId: Disks_Get
     * api-version: 2020-12-01
     * x-ms-examples: Get information about a managed disk.
     */
    /**
     * Sample code: Get information about a managed disk.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getInformationAboutAManagedDisk(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDisks()
            .getByResourceGroupWithResponse("myResourceGroup", "myManagedDisk", Context.NONE);
    }
}
```