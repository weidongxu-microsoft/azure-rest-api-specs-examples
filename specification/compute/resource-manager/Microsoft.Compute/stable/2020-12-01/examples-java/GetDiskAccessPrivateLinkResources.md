```java
import com.azure.core.util.Context;

/** Samples for DiskAccesses GetPrivateLinkResources. */
public final
class GetDiskAccessPrivateLinkResources {
    /*
     * operationId: DiskAccesses_GetPrivateLinkResources
     * api-version: 2020-12-01
     * x-ms-examples: List all possible private link resources under disk access resource.
     */
    /**
     * Sample code: List all possible private link resources under disk access resource.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listAllPossiblePrivateLinkResourcesUnderDiskAccessResource(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDiskAccesses()
            .getPrivateLinkResourcesWithResponse("myResourceGroup", "myDiskAccess", Context.NONE);
    }
}
```