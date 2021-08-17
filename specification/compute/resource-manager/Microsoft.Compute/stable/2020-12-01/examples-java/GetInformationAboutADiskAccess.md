```java
import com.azure.core.util.Context;

/** Samples for DiskAccesses GetByResourceGroup. */
public final class GetInformationAboutADiskAccess {
    /*
     * operationId: DiskAccesses_Get
     * api-version: 2020-12-01
     * x-ms-examples: Get information about a disk access resource.
     */
    /**
     * Sample code: Get information about a disk access resource.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getInformationAboutADiskAccessResource(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDiskAccesses()
            .getByResourceGroupWithResponse("myResourceGroup", "myDiskAccess", Context.NONE);
    }
}
```