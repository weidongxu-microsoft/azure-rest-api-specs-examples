```java
import com.azure.core.util.Context;

/** Samples for DiskAccesses DeleteAPrivateEndpointConnection. */
public final
class DeleteAPrivateEndpointConnection {
    /*
     * operationId: DiskAccesses_DeleteAPrivateEndpointConnection
     * api-version: 2020-12-01
     * x-ms-examples: Delete a private endpoint connection under a disk access resource.
     */
    /**
     * Sample code: Delete a private endpoint connection under a disk access resource.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void deleteAPrivateEndpointConnectionUnderADiskAccessResource(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDiskAccesses()
            .deleteAPrivateEndpointConnection(
                "myResourceGroup", "myDiskAccess", "myPrivateEndpointConnection", Context.NONE);
    }
}
```