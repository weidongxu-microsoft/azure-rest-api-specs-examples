```java
import com.azure.core.util.Context;

/** Samples for DiskAccesses GetAPrivateEndpointConnection. */
public final
class GetInformationAboutAPrivateEndpointConnection {
    /*
     * operationId: DiskAccesses_GetAPrivateEndpointConnection
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
            .getAPrivateEndpointConnectionWithResponse(
                "myResourceGroup", "myDiskAccess", "myPrivateEndpointConnection", Context.NONE);
    }
}
```