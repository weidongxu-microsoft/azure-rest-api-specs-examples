```java
import com.azure.core.util.Context;

/** Samples for DiskAccesses GetByResourceGroup. */
public final class GetInformationAboutADiskAccessWithPrivateEndpoints {
    /*
     * operationId: DiskAccesses_Get
     * api-version: 2020-12-01
     * x-ms-examples: Get information about a disk access resource with private endpoints.
     */
    /**
     * Sample code: Get information about a disk access resource with private endpoints.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getInformationAboutADiskAccessResourceWithPrivateEndpoints(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDiskAccesses()
            .getByResourceGroupWithResponse("myResourceGroup", "myDiskAccess", Context.NONE);
    }
}
```