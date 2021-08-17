```java
import com.azure.core.util.Context;

/** Samples for DiskAccesses ListPrivateEndpointConnections. */
public final
class ListPrivateEndpointConnectionsInADiskAccess {
    /*
     * operationId: DiskAccesses_ListPrivateEndpointConnections
     * api-version: 2020-12-01
     * x-ms-examples: Get information about a private endpoint connection under a disk access resource.
     */
    /**
     * Sample code: Get information about a private endpoint connection under a disk access resource.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getInformationAboutAPrivateEndpointConnectionUnderADiskAccessResource(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDiskAccesses()
            .listPrivateEndpointConnections("myResourceGroup", "myDiskAccess", Context.NONE);
    }
}
```